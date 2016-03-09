#2015最佳搭档：tar和ssh

最佳搭档彼此相互补充，对于整体而言，搭档的每个成员具有独特和不可替代的作用。但是有些搭档非常奇怪。下面要介绍的这对就是今年最佳搭档的典范：**`tar`**和**`ssh`**指令。

等等－什么？！

是的，没错，`tar`和`ssh`命令以十分有趣的方式协作，尤其是用于Standard I/O（STDIO），即[标准流](https://en.wikipedia.org/wiki/Standard_streams)时。

##ssh

`ssh`指令是一种通过终端模拟器允许用户登录到远程计算机进行shell会话并运行指令的安全而复杂的方式。因此我可以登录到远程计算机，在远程计算机上运行**`ls`**指令。结果显示在本地主机的ssh终端模拟器窗口。指令的标准输出（STDOUT）显示在终端窗口，但是数据还在远程主机上，因此不能被本地主机直接使用。

这些都不足为奇，每个人都这样使用。但是接下来的会更有趣。我可以像下面这样，在远程计算机上只运行一条指令并且结果显示在本地主机，而不需要在远程计算机上维护一个终端会话同时运行多条指令。这里假设SSH公钥和私钥（PPKP）已经在使用，我不需要每在远程主机上发布一条指令就输入一次密码：

`ssh remotehost ls`

因此现在我可以使用本地主机上指令执行的结果，因为标准输出数据流通过SSH通道传输到了本地主机。好，但是这意味着什么呢？

回答这个问题之前，让我们先看看`tar`指令。

##tar

`tar`指令用于备份。`tar`是Tape Archive（磁盘归档）的缩写，但是这个指令能被用于任何类型的记录介质如磁带、硬盘和优盘等。下面这条指令可以在本地主机上创建/home目录的备份：

`tar -cvf /tmp/home.tar /home`

这条指令在`/tmp`目录下创建了一个名称为`home.tar`的压缩文件。这个文件是`home`目录下所有文件的备份。很好，但是这些也不是很有趣，因为很常用。

虽然很多人没有意识到，但是有趣的是，如果不使用**`-f`**选项指定目标输出文件，`tar`指令的输出直接传输到STDOUT：

`tar -cv /home`

这意味着，`tar`指令的完整输出，即备份好的文件被传输给终端，这开创了一些有趣的可能性，例如重定向STDOUT数据流到备份文件。看起来像下面这条指令：

`tar -cv /home &gt; /tmp/home.tar`

这条指令和第一条`tar`指令具有相同的功能，只是用了一种有点不同且更有意思的方式。

##神奇的搭档

我们可以使用类似如下指令备份远程主机的`home`目录到远程主机的`/tmp`目录：

`ssh remotehost “tar -cvf /tmp/home.tar /home"`

注意在远程主机执行的指令用引号引起来，确保正确的指令在远端执行；这样做对于shell终端和人类来说都很明朗。对这条指令稍做修改，我们将`tar`指令的输出重定向到远程主机的/tmp目录：

`ssh remotehost “tar -cv /home &gt; /tmp/home.tar"`

这条指令和上一条指令作用一样。这种情况下，`tar`指令的STDOUT数据流完全在远程主机维护，然后重定向到备份文件。然而下面这条指令开创了很多新的可能性。你知道它都干了什么吗？

`ssh remotehost “tar -cv /home” &gt; /tmp/home.tar`

这种情况下，`tar`指令的STDOUT数据流通过SSH连接发送到本地主机。然后数据流重定向到本地主机的`/tmp/home.tar`备份文件。仅仅将引号移到左边，新的指令就可以备份远程主机的文件到本地主机。

我每天都使用这对年度搭档完成备份。我写了一个用`ssh`和`tar`指令，还有SSH公钥加密的脚本，来完成远程主机到本地外部USB硬盘的备份操作。这两个指令简化了很多必不可少的操作，更为重要的是，它们是免费的开源软件。

所以让我们用掌声欢迎今年的开源社区最佳搭档：tar和ssh。

##关于作者

![Image of author](https://opensource.com/sites/default/files/styles/profile_pictures/public/david-crop.jpg?itok=oePpOpyV)

Raleigh, North Carolina    
[http://www.databook.bz](http://www.databook.bz)

David Both是一位居住在Raleigh, North Carolina的Linux和开源倡导者。他在IT行业超过40年，曾经在IBM教授OS/2课程20多年。1981年，在IBM工作期间，他写了第一个IBM个人计算机的培训课程。此外他还为Red Hat教过RHCE课程，也曾在MCI Worldcom、Cisco和北卡罗莱纳州工作。致力于Linux和开源软件15年有余。在OS/2 Magazine、Linux Magazine、Linux Journal和OpenSource.com这些期刊也发表过文章。他和思科的一位同事共同发表的文章“Complete Kickstart”在2008年十大最佳系统管理文章中排名第9。