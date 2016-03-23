#10个须要添加到系统管理员工具箱中的利器

## 摘要：
本文系Opensouce.com所发布的《开源2015年鉴》的其中一篇，介绍了2015年系统管理员们的工具箱中增添了哪些很有特色的工具。众所周知，系统管理员的知识g更迭在加快，工具又该有何变化了呢？

--------------------------------------------------
![image of yearbook](https://opensource.com/sites/default/files/styles/image-full-size/public/images/life/osdc-open-source-yearbook-lead6.png?itok=6iBX0DP8)

身为系统管理员，不管是基于何种平台的，手持强大的开源工具是必须的。在本文中，就重点介绍一下著名的或者不怎么有名的在2015年新释出的工具！

## BlockBox

管理机密是困难的，尤其是最终在服务器上的机密。而这也是 [Stack Exchange](http://stackexchange.com/) 开发 [BlockBox](https://github.com/StackExchange/blackbox) 套件的主要原因。BlockBox 使用 [GNU 隐私卫士](https://www.gnupg.org/) ［GPG］来加密机密达到安全的目的，比如密码、私钥等，且将它们存放在一个版本控制系统中。BlockBox 还提供了对配置管理工具的支持(尤其是 [Puppet](https://puppetlabs.com/))，这样在需要的时候可以提取相应的机密。

基于插件机制的 BlockBox 使其对它的扩展变得非常的容易。尽管 BlockBox 最初的设计是和 [git](https://git-scm.com/)仓库一起工作的，但是目前对 [mercurial](https://www.mercurial-scm.org/)、[Subversion](http://svnbook.red-bean.com/)、[perforce](https://www.perforce.com/)等都增加了支持。BlockBox 支持 Linux、OS X、以及 Windows （通过 [Cygwin](https://www.cygwin.com/)），所以它可以在混合环境中使用起来游刃有余。

## KeePass

其实若是不去任何地方都话，管理机密颇是一件容易的事情。几年前，我开始使用 [KeePass](http://keepass.info/) 的原因是因为它被移植到了 [Maemo] 平台。如果一些已经被遗弃的移动操作系统不是你的菜的话，KeePass 是不错的选择，它支持的操作系统平台有：Linux、OS X、Windows、Android、以及 iOS。

当我还是一名系统管理员的菜鸟的时候，我有一个记满了很少使用的密码的笔记本，然后我将这个笔记本放在了保险柜中保存。其实 KeePass 就是类似这样的做法，而且更加的容易备份和跨地域的进行同步。KeePass 保存的条目有 URL、用户名、密码、以及纯文本。条目可以分组，并可以自定义图标，从而达到更加易于使用的目的。最近发布的版本则聚焦于性能和用户体验的改进。

## ownCloud

需要一个同步你的 KeePass 数据库的新的方法？[ownCloud](https://owncloud.org/) 最新发布的8.2版本带来了改进的设计和易管理。对于那些无法使用或根本就是不想使用第三方服务的用户来说，ownCloud 所提供的共享文档、照片、日历和其它安全数据的功能是最佳的选择。这是一款由社区开发的应用程序，允许管理员们使用各种方法来扩展的软件，甚至包括从 Android 手机上接受短信。如果你需要为你的用户（或者是你自己）进行合作并同时可以控制数据的话，ownCloud 绝对是你的不二选择。

## WireShark

若是那一天我在截取网络包来分析的话，这一天一定是糟糕的一天，但是有了 [WireShark](https://www.wireshark.org/) 会让人稍好过一点。尽管这是一个17、8年的老项目了，但是在2015年11月的时候还是发布了[版本2.0](https://www.wireshark.org/news/20151118.html)，官方对于2.0的主要变动是轻描淡写的：整个 UI 界面用 [Qt](http://www.qt.io/)重写了，以及简化了很多交互方面的内容。虽然新的版本带来很多新的改进，但它仍然是人们多年以来所熟悉的那个 WireShark。

## VirtualBox

在今天，桌面虚拟化已经有太多的选择了，但是体验过所有的，最终我总是回到甲骨文的 [VirtualBox](https://www.virtualbox.org/)。在工作中，能够配置和用户一样的操作系统，运行同样版本的软件，是非常有价值的，它能够快速而轻松的驾驭虚拟机，节省了我大量的时间。在2015年7月，VirtualBox 发布了5.0版本，新增了让虚拟机以 “headless” 模式启动，它对于我来说非常的实用，因为在虚拟机中生成 SSH 秘钥后就可以直接交互了。5.0还引入了半虚拟化技术，这为客户操作系统的性能有了更大的改进，以及磁盘加密、USB 3.0的支持等。

## Visual Studio Code

计算机历史上编辑器的争论已久，好不容易彼此之间进入了一个相对缓和的阶段，但是2015年有加入了一个新的编辑器，又引起了纷争。这就是微软释出的 [Visual Studio Code](https://code.visualstudio.com/)，可以在 Windows 、Linux、Mac OS X 下运行的新的编辑器，遵循 MIT 许可证。这绝对是一件大事件，因为微软一直是开源软件的敌人！尽管 Visual Studio Code 是作为一个代码编辑器而设计的，但是这并不意味着对于系统管理员就没什么用处（毕竟，每个系统管理员都还是要写一些代码的）。顺便值得一提的是，Visual Studio Code 内置了对 ```git``` 和 ``` Docker``` 的支持。


## RRDtool

即使你没有直接和 [RRDtool](http://oss.oetiker.ch/rrdtool/) 打过交道，也有可能和内嵌它的程序有过交集，因为其实在是太过于广泛了。RRDtool 是一款对于存储和将时间序列图形化非常出色的工具，这也是它在性能监控系统中被大量采用的缘由，例如 [Cacti](http://www.cacti.net/) 和 [Xymon](http://xymon.sourceforge.net/)。若你不想使用静态的 PNG 图片，Tobi Oetiker 还开发了一套用于生成 RRD 图形的 [JavaScript 库](https://github.com/oetiker/RrdGraphJS)。

## Mosh

系统管理员离开自己的办公区域是很正常的，但是这并不能阻止他们在移动中仍然能够工作。但是，令人闹心的地方在于，并非所有的网络都是靠谱的，作为系统管理员的你一定有在手机上或者是在网络负荷非常中的研讨会议上尝试 SSH 连接远端的服务器的体验，那一定深刻感受过痛苦是何滋味，幸好 [Mosh](https://mosh.mit.edu/) 及时的出现了，帮助你减轻那些痛苦。Mosh 允许漫游的网络连接，通过响应本地的用户输入来缓减你对慢速网络对容忍，并持续的重连到网络。经过了差不多两年的沉寂之后，Mosh 在2015年7月发布了1.2.5版本，此版本除了平常的 Bug 修复之外，对平台的支持进行了改进，且增加了对 IPv6 的支持。

## RackTables

在小型的环境中，系统管理员对于自己的每个机器都是心中有数的，甚至能够做到不假思索的说出那个服务器在哪里、跑的是何种服务、IP地址是多少、连接了哪些网络和存储。就拿我个人的经历来说吧，我的第一份工作，整个部门也就半个机柜的机器，小菜一碟！但是当我到大公司工作时，管理的机器竟然有4000台之多，我哪里分得清哪是哪啊！在这样的规模下，类似于[RackTables](http://racktables.org/)这样的工具就显示出它的作用来了。RackTables 是一款纪录硬件信息、机架空间、网络配置等的工具。想一下将这些信息使用电子表格是多么可怕的事，RackTables 可以帮到你！

## Docker

在当今这个时代，若你没有听说过[Docker](https://opensource.com/resources/what-docker)，你都不好意思说你是在程序界混的。在 DevOps 的世界里容器是重中之重，而 Docker 又是一个容器的平台。在2015年的11月初发布了1.9版本，增加了很多新的特性。多主机网路能够将虚拟网络分配给主机，这给了系统管理员们在他们的网络拓扑中带来更大的灵活。对于持久的存储支持也做了改进。Docker 将基础设施的灵活性和健壮性带高了一个级别，将会在接下来的一年会对系统管理员和用户产生更大的影响。

上述所列出来的开源工具有作为系统管理员的你较喜欢的吗？请留言告诉我们。

## 关于作者
![Image of author 1](https://opensource.com/sites/default/files/styles/profile_pictures/public/benc_cropped-2.jpg?itok=kFWI1b8R)Ben Cotton 是一名受过训练的气象学家，其职业是一名高性能计算机工程师。Ben 在 [Cycle Computing](http://www.cyclecomputing.com/)，带领着一个支撑工程师团队。他是 Fedora 的用户和贡献者，也是本地开源小型聚会的联合创始人。且是开源促进会的成员，同时也是自由软件保护的支持者。可以关注他的Twitter[@funnelfiasco](https://twitter.com/funnelfiasco)，或者直接访问[funnelfiasco.com](http://www.funnelfiasco.com/)。

本文由作者[Ben Cotton](https://opensource.com/users/bcotton) 发表在Opensource.com上：[10 helpful tools for a sys admin's toolbox](https://opensource.com/business/15/12/10-sysadmin-tools)。经授权，在InfoQ中文站翻译共享。本文在[Creative Commons BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)许可证下发布。
