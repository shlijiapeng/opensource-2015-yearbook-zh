# OwnCloud 的六种创意玩法


![image](https://opensource.com/sites/default/files/styles/image-full-size/public/images/business/osdc-open-source-yearbook-lead1-inc0335020sw-201511-01.png?itok=qHwtS6bs)

[OwnCloud](https://owncloud.com/)是一款可自托管的开源文件同步和分享服务。与很多大公司例如 Dropbox、Goolge Drive、Box 等等一样，OwnCloud 允许你访问你得文件、日历、联系人和其他数据。你可以在你的设备之间同步任何东西（或者其中一些）并与其他人分享。然而 OwnCloud 比那些[托管在别人电脑](https://blogs.fsfe.org/mk/new-stickers-and-leaflets-no-cloud-and-e-mail-self-defense/)的私有软件要强很多。

让我们看看看使用 OwnCloud 可以做的六种创意玩法。其中这些之所以可以这么做，是因为 OwnCloud 是开源的，而其他利用了它提供的特殊功能。

## 1. 可扩展的 OwnCloud Pi 集群

因为 OwnCloud 是开源的，你可以选择将其托管在自己的电脑上或你信得过的提供商——没必要将自己的数据放到不知道存在哪的大公司那里。可以找到一些 [Owncloud 提供商](https://owncloud.org/providers) 或者下载包到自己的虚拟机或[服务器上](https://owncloud.org/install/#instructions-server)。

![](https://opensource.com/sites/default/files/images/life-uploads/banana-pi-owncloud-cluster.jpg)

Photo by Jörn Friedrich Dreyer. CC BY-SA 4.0.

而我们看到最具创造性的玩法则是 [Banana Pi 集群](http://www.owncluster.de/) 和 [树莓派集群](https://christopherjcoleman.wordpress.com/2013/01/05/host-your-owncloud-on-a-raspberry-pi-cluster/)。可以利用 Owncloud 的可扩展性来服务上千用户，不过有些人则反其道而行之，将很多小型系统组合在一起变成超快的 OwnCloud 服务。妙哉！

## 2. 同步你的密码

为了让 OwnCloud 更易于扩展，我们让其更加模块化并推出了 [OwnCloud 应用商店](https://apps.owncloud.com/)。这里你可以找到音乐和视频播放器、日历、联系人、生产力工具、游戏、一个素描应用和更多。

要从 200 多个应用中选一个代表是很困难的，不过管理密码也许是很特别的一个功能。有不只三个应用提供了这个功能：[Passwords](https://apps.owncloud.com/content/show.php/Passwords?content=170480)、[Secure Container](https://apps.owncloud.com/content/show.php/Secure+Container?content=167268) 和 [Passman](https://apps.owncloud.com/content/show.php/Passman?content=166285)。

![](https://opensource.com/sites/default/files/images/life-uploads/password.png)

## 3. 管理数据存储的位置

外部存储可以让你将已存在的数据挂到 OwnCloud 上，可以让你使用同一个界面直接访问 FTP、WebDAV、Amazon S3 甚至包括 Dropbox 和 Google Drive 上的文件。

视频演示：<https://www.youtube.com/watch?v=uezzFDRnoPY>

大公司会创建他们自己的壁垒——Box 只允许与其他 Box 用户协作；如果你要通过 Google Drive 分享文件，你的朋友也需要有 Google 帐号才行。而对 OwnCloud 的外部存储来说，你可以打破这些壁垒。

一个很赞的做法是将 Google Drive 和 Dropbox 加到外部存储里。这样你可以无缝使用这些文件，并将其通过简单的链接分享——不需要额外的帐号了。

## 4. 获取已上传的文件

因为 OwnCloud 是开源的，人们可以贡献自己想要的特性而不用拘泥于大公司的需求。我们的贡献者一直很关注安全和隐私，因此 OwnCloud 推出了很多特性比如[多年前就推出](https://owncloud.com/owncloud45-community/)的用秘密保护公开的链接，并设立一个过期日期。

现在，OwnCloud 的共享链接可以设置成可读可写的，这意味着用户可以编辑你分享给他们的文件（无论是否使用密码保护），或者上传一个新文件到你的服务器而不需要被迫注册一个可能会盗取他们隐私信息的另一个互联网服务。

视频演示：<https://www.youtube.com/watch?v=3GSppxEhmZY>

这可以极大方便那些想分享给你一个大文件的人。与其将文件上传到第三方平台，发送给你一个链接并让你去那里下载（常常需要登录），还不如直接上传到你提供的共享文件夹，你可以直接下载下来。

## 5. 获取免费的安全存储

我们一直在反复强调，贡献者都很注重安全性和隐私。这就是为什么 OwnCloud 有一个可以对已存储数据加密解密的应用。

使用 Owncloud 来管理存储在 Dropox 和 Google Drive 上的文件，并不能保证自由和控制数据和隐私。这款加密应用可以改变这一切。发送到那些提供商之前先加密一下，而获取的时候再解密，这样你的数据既安全又方便。

## 6. 分享文件并保持控制

作为一个开源项目，OwnCloud 没有必要去构筑壁垒。联合云分享（Federated Cloud Sharing）是一个[由 OwnCloud 开发并推出](http://karlitschek.de/2015/08/announcing-the-draft-federated-cloud-sharing-api/)的协议，旨在让不同的文件分享和同步服务器之间可以互相通信并安全的交换文件。联合云分享协议有一段有趣的历史。[二十二所德国大学](https://owncloud.com/customer/sciebo/)决定创建一个巨大的云来服务其 500000 位学生，需要一个创新的解决方案：联合云分享应运而生。该解决方案可以让这些大学里的学生无缝连接在一起。同时，每个大学的系统管理员也可以控制所辖学校的学生使用文件的情况和相应的政策，比如存储限制或限制谁、与何人、如何分享文件。

视频演示：<https://www.youtube.com/watch?v=9-JEmlH2DEg>

而这个特性并不局限在德国高校：每个 OwnCloud 用户都可以在其用户设置里找到一个[联合云 ID](https://owncloud.org/federation/)，并可以将其与他人分享。

这就是 OwnCloud 带给人们的六种不同凡响的特性，所有这些都是因为它是开源的并为解放你的数据而设计。

