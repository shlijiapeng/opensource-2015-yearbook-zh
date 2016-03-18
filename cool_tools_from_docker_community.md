#10个来自 Docker 社区的酷炫工具 

## 摘要：
本文系[Opensource.com](https://opensource.com/)所发布的《开源2015年鉴》的其中一篇，来自Docker公司的高管回顾了2015年由社区所主导和开发的几个非常好的工具。

--------------------------------------------------

![cool tools](https://opensource.com/sites/default/files/styles/image-full-size/public/images/life/osdc-open-source-yearbook-lead7.png?itok=33kcxpmm)

回顾过去的2015年，拥有先进的开发经验的 Docker 社区创建了很多个项目。我们知道从如此之多的贡献中挑选出来自认为优秀的是非常困难的一件事，这里我们尽可能的选出大伙公认的 “10个酷炫的工具”，这些工具在你使用 Docker 和欲扩展你的知识时应该能够用得到。

## 1.[容器迁移工具(CMT)](https://github.com/marcosnils/cmt)

作为 Docker 全球黑客日第三天的[大赢家](https://www.youtube.com/watch?v=pwf0-_cs6U4)，[容器迁移团队](http://blog.mantika.io/GHD/)称其灵感来自于 Michael Crosby（[@crosbymichael](https://twitter.com/crosbymichael)）和 Arnaud Porterie （[@icecrime](https://twitter.com/icecrime)）在 DockerCon 大会面向全世界展示的 Quake 3 的容器化迁移，并且看到了在维护 TCP 连接的时候作容器迁移。 CMT 项目创建了一个外置的命令行工具，可以让 Docker 和 [runC](https://runc.io/)在不同的主机上作“在线迁移”，且能够做到迁移前验证以及自动发现最适合迁移的目标主机。

## 2.[Dockercraft](https://github.com/docker/dockercraft)

我们做了一个非常有趣的补充！ 很多 Docker 用户均在容器中运行自我定制过的 [Minecraft](https://minecraft.net/) 服务，但是此 Dockercraft 只是 Minecraft 的一个客户端，用来可视化以及管理 Docker 容器。可以轻轻的动一下开关，就可以打开和关闭一个容器，甚至是按住一个按钮就可以销毁一个容器。Dockercraft 是一个蛮有趣的项目－它竟然能够让人上瘾－包括来自 Docker 公司的工程师 Adrien Duermael 和 Gaetan de Villele。

## 3.[Docker标签注入](https://github.com/garethr/docker-label-inspector)

Docker 标签注入工具可以保证开发者们所提供的基于元数据容器的 Docker 镜像在互联网上分发的完整性。尤其是此工具可让开发者们使用 [Docker 标签](https://docs.docker.com/engine/userguide/labels-custom-metadata/)来创建基于容器域技术的元数据，从而对比检查其标签和官方标签 schema 以及验证所提供的 JSON schema。

## 4.[dvol](https://github.com/ClusterHQ/dvol)

Dvol 为运行在 Docker 中的开发数据库提供了版本控制功能，其可以让用户对容器化的数据库进行提交、重置、乃至切换分支，即是这个数据库是运行在用户的笔记本中，所以用户可以非常轻松的保存特定的状态并在以后根据需要来恢复，Dvol 还整合了 Docker Compose ，这样还能够在用户的笔记本电脑中将可重用的微服务环境运行起来。

## 5.IPVS 守护进程 [GORB](https://github.com/kobolog/gorb)

Docker 容器下的 IP 虚拟服务（IPVS），是在 DockerCon EU 上提出来的，其是使用已经在 Linux 内核中存在了十几年的开源服务－IPVS－来实现生产环境级别的负载均衡和路由请求。IPVS 支持 TCP、SCTP、以及 UDP，且能达到快速的效果，常常相比于直接连接的损失在5%之内。其它的特性包括 NAT、隧道、和直接路由。为了使 IPVS 更加的容易使用，Go 路由和均衡 （GORB）守护进程在 Docker 容器内部创建了服务并以 REST API的方式呈现，从而为 Docker 提供 IPVS 的路由服务。

## 6.[libnetwork](https://github.com/docker/libnetwork)

libnetwork 是混合了来自 libcontainer 和 Docker engine 的关于网络的代码，意图构建一个针对于容器联网的多平台的程序库。libnetwork 的目标是交付一个健壮的容器网络模式，提供一致的编程接口，为应用程序提供所需要的网络抽象。有太多的网络解决方案可用来适配很多的用例。libnetwork 使用 驱动／插件的模式来支持所有的这些解决方案，同时通过抛出简单、一致的网络模式给用户从而将复杂的驱动实现抽象化。

## 7.[树莓派挑战者](https://github.com/hypriot/rpi-kernel)

在 [Docker 闭幕演讲](http://blog.docker.com/2015/07/dockercon-2015-videos-day-2-closing-keynote/)，来自 Hypriot 的 Dieter Reuter 演示了在一个树莓派2的设备中运行500个 Docker 容器的场景，Dieter 相信这个数字至少还可以翻番，所以他向社区提出了挑战，希望打破他的个人记录。作为项目的一部分，Dieter 还对在树莓派中如何运行 Docker 进行了入门演示，而且也描述了在单个的树莓派2中如何扩展运行 web 服务的容器数量。目前的纪录保持是在单个的树莓派2中运行超过2500个 web 服务的容器。

## 8.基于[Zoe](https://github.com/DistributedSystemsGroup/zoe-docker-images)分析的 Spark 扩展

这是一个将大数据计算的数据密集型框架 [Spark](http://spark.apache.org/)和 [Docker Swarm](https://docs.docker.com/swarm/) 紧密的捆绑在一起的面向用户的工具.Zoe 可以执行长期运行的 Spark 任务，也可以执行如 Scala 或 iPython 的交互 或者是流的应用程序，覆盖到 Sparek 开发的全部周期。当计算结束之后，资源会自动回收，同时也可用作其它用途，因为所有的进程都运行在 Docker 容器中。此工具在 Swarm 之上对应用进行调度，以及优化容器的位置。

## 9.[Unikernel 源码演示](http://unikernel.org/blog/2015/contain-your-unikernels/)

Unikernel 首次亮相是在 DockerCon EU([Unikernel，遇见 Docker](http://unikernel.org/blog/2015/unikernels-meet-docker/))，绝对是非常酷的 Hack，其中[演示](http://unikernel.org/blog/2015/unikernels-meet-docker/)则充分展示了 unikernel 可以被当作任何的其它容器。在此演示中，Docker 被用于构建一个 unikernel 的微服务，然后接着部署了完整的 Web 应用，包括数据库、web 服务器、以及 PHP 代码，所有所运行的都被当作不同当 unikernel 微服务构建使用[Rump 内核](http://rumpkernel.org/) 。Docker 管理 unikernel一如 Linux 容器，但是毋需部署传统的操作系统。在演示中还有组成 Nibbleblog 应用的使用 unikernel所分离的 MySQL、NGINX、PHP，以及一些其它服务的示例入门。

## 10.Swarm 的 DNS 发现服务－[Wagl](https://github.com/ahmetalpbalkan/wagl)

wagl 是一个 DNS 服务，是为运行在分布式 [Docker Swarm](https://docs.docker.com/swarm/)集群中的微服务容器提供彼此之间的发现和通信的。wagl 是极为简单的，在集群中以可随时丢弃的容器的形式运行着，提供基于 DNS 的服务发现，且能够通过对 DNS 记录中的 IP 地址列表的轮询实现简单的负载均衡。

## 关于作者
![Image of author 1](https://opensource.com/sites/default/files/styles/profile_pictures/public/pictures/manomarks.jpg?itok=_eAqEjs_)Mano Marks 是 Docker 公司的主管开发者关系的总监。

本文由作者[Mano Marks](https://opensource.com/users/spanoplos) 发表在Opensource.com上：[10 cool tools from the Docker community](https://opensource.com/business/15/12/10-cool-tools-docker-community)。经授权，在InfoQ中文站翻译共享。本文在[Creative Commons BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)许可证下发布。


