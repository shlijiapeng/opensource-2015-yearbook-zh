# Facebook在2015年的5大开源项目

Facebook相信开源的巨大力量。当整个社区能够共同致力于编码工作时，所产生的益处是不可估量的。人们会用新的眼光指出我们的问题，让我们能够更快地找出解决方案。我们将一起克服所面对的挑战、加速创新过程。社区的力量能够让我们冲破现有技术的种种限制。

当然，成功的开源项目离不开一个健壮的、通力协作的社区。在年终即将来临之际，我们将按照社区的活跃度与影响力排名，选出Facebook在2015年的5大开源项目。

### [HipHop虚拟机][1]（HHVM） ###

HHVM是我们开发的一套虚拟机与web服务器系统，并于2013年实现了开源，它是基于我们在2010年发布的HPHPc编译器开发的。仅在过去一年间，代码提交次数就上升了29%，而fork的数量则上升了30%。

HHVM最常见的用途是作为单台服务器使用，它的目标是取代Apache与mod_php，运行由Hack和PHP编写的程序。通过JIT编译方式，HHVM能够实现更好的性能，同时保留了PHP开发者已习惯的各种灵活性。我们在今年实现了几个重要的里程碑：

>  1. 新的[Async特性][2]默认可用，包括对[AsyncMySQL][3]与[MCRouter][4]（memcached）的支持。
>  2. 当PHP 7语言本身于12月推出的同时，我们就[宣布][5]了对PHP 7所有主要特性的支持，并且发布了新一版的用户文档。
>  3. Box[宣布][6]将使用HHVM作为运行其PHP代码的唯一引擎。
>  4. Etsy在4月份将业务迁移至HHVM平台，帮助该公司克服了在创建大规模移动产品时所遇到的各种挑战。

### [React][7] ###

Facebook在2013年5月开源了React，而在过去一年间，我们仍然获得了来自社区的极大支持，代码提交的数量提高了75%，而fork的数量更是提高了198%。React是由Facebook所设计的一种用于构建用户界面的JavaScript库，目前已在许多公司得到应用。React使用了一种全新的方式构建应用：它允许开发者将应用分解为相互解耦的组件，因此每个组件都可进行独立的维护与迭代。

今年，我们为React推出了两个重要的发布：一是React Native，二是新的[开发者工具][8]。我们也看到越来越多的公司开始使用React构建他们的产品，包括[Netflix][9]与[WordPress][10]。


### [Presto][11] ###

Presto是由我们设计的新型分布式SQL引擎，它能够对各种大小（从GB级至PB级）的数据源进行交互式的分析查询。我们设计Presto的目标是帮助我们更快地进行数据分析，以配合我们不断增长的数据量与持续加速的产品周期。

自从我们于2013年11月开源了Presto之后，它的发展、接受度以及对它的支持都得到了全面的提高。在去年一年的时间内，它的代码提交数量提高了48%，而fork的数量则提高了99%。[Airbnb][12]、[Dropbox][13]以及[Netflix][14]等各大公司都开始使用Presto作为他们的交互式查询引擎。Presto在全球范围内的接受度也在逐步提高，包括来自日本的社交媒体游戏开发公司[Gree][15]，以及来自中国的电子商务公司京东[JD.com][16]。

同样在今年，Teradata也[宣布][17]了加入Presto社区的计划，专注于企业级特性的改善并提供相应的支持。这也展现了整个社区对于Presto成为数据基础设施方面一个重要组成部分的信心。此外，Amazon Web Services（AWS）也在其[EMR服务][18]中将Presto作为一线功能提供支持，已有诸多用户在生产环境中使用该功能，包括Nasdaq。而在业界处于领先地位的商业智能工具开发商MicroStrategy也在其旗舰产品MicroStrategy 10中提供了对Presto的支持。

### [RocksDB][19] ###

我们在2013年11月开源了RocksDB，这是一个嵌入式的持久化键值数据库，支持高速的数据存储。在过去一年间，该项目的代码提交数量提高了52%，而fork的数量则提高了57%。除了这些令人印象深刻的数据之外，该项目引起了整个社区强烈共鸣的原因在于该嵌入式数据库能够为由网络延迟引起的响应缓慢问题提供一种临时方案，并且它提供了充分的灵活性，可通过自定义的方式应对不断发展的硬件趋势。

RocksDB为LinkedIn与Yahoo等公司提供了各种关键性的服务。我们今年的主要目标之一是将RocksDB这个存储引擎的特性迁移至通用目的的数据库上，以MongoDB作为起点。与Teradata宣布提供对Presto的商业性支持类似，RocksDB今年的另一个里程碑是来自[Percona][20]的数据性能专家宣布将为其提供企业级的支持。

### [React Native][21] ###

React Native是我们最新推出的开源项目之一，它在今年3月实现了开源。React Native让工程师能够使用与React相同的方法与工具为移动设备快速地创建原生应用。Facebook不仅在内部持续开发这些工具，并且致力于通过与开源社区的协作改善全球开发者的体验。在React Native诞生的第一个年头，它就在Facebook的开源项目流行度排名中攀升到第二的位置，在GitHub上已有超过23000位关注者。Facebook Ads的iOS与Android应用内部正是使用React Native所开发的，对于那些以JavaScript为核心能力的开发者来说，代码的重用率达到了85%。React Native为移动开发的观念带来了重要的改变，这也是我们本年度最关键的成就之一。

总的来说，我们仍有许多要完善的地方，但作为整个社区的一份子，我们对于目前的成就深感自豪。对于那些在百忙之中仍乐于为这些项目贡献力量、使我们在这一年中达成如此成就的人们，我们深表谢意！


  [1]: https://github.com/facebook/hhvm
  [2]: https://docs.hhvm.com/hack/async/introduction
  [3]: http://docs.hhvm.com/manual/en/book.hack.async.mysql.php
  [4]: http://docs.hhvm.com/manual/en/book.hack.mcrouter.php
  [5]: http://hhvm.com/blog/10925/improved-user-documentation
  [6]: https://code.facebook.com/posts/1607907626123431/under-the-hood-box-s-hhvm-migration/
  [7]: https://github.com/facebook/react
  [8]: https://facebook.github.io/react/blog/2015/09/02/new-react-developer-tools.html
  [9]: http://techblog.netflix.com/2015/01/netflix-likes-react.html
  [10]: https://developer.wordpress.com/2015/11/23/the-story-behind-the-new-wordpress-com/
  [11]: https://github.com/facebook/presto
  [12]: http://nerds.airbnb.com/airpal/
  [13]: https://prestodb.io/
  [14]: http://techblog.netflix.com/2014/10/using-presto-in-our-big-data-platform.html
  [15]: http://labs.gree.jp/blog/2014/12/12838/
  [16]: http://jd.com/
  [17]: http://blogs.teradata.com/data-points/bringing-open-source-presto-enterprise/
  [18]: https://aws.amazon.com/elasticmapreduce/details/presto/
  [19]: http://github.com/facebook/rocksdb
  [20]: https://www.percona.com/
  [21]: https://github.com/facebook/react-native
