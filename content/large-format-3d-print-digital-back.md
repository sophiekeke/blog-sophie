Title: 一些关于3D打印大画幅数码接片后背的实验
Date: 2019-08-26 22:53
Category: Life
Slug: large-format-3d-print-digital-back
Tags: Large Format, 3D Print, Photography, DIY

周六早上，一个60斤的包裹放在了我家门口。我满脑子都是，我是谁，我在哪，我为什么买了个这。。

![3D printer](/images/large-format-back-3d-printer.jpg)

启迪3D打印机。液晶屏上的宋体英文真是非常亲切了。

说来惭愧，我有个graflex crown graphics，直到上周四才搞清楚怎么把graflock后背拆下来，直接卸掉毛玻璃露出皮腔。做到这一点以后感觉发现了新天地，似乎可以把数码相机弄上去直接拍摄的样子。这样就不用alpa，cambo等异常昂贵的机身也可以用数码版技术相机了。但显然这样的转接后背是不会有官方支持的，只能用第三方的（印象里申豪有转尼康佳能的后背）。于是就在想，有没有可能自己3D打印一个这样的后背呢？

其实有这样的想法有一段时间了，主要想着1) 用现有的大画幅设备给数码相机加上技术动作；2) 如果再加入一些简单的机械设计的话，可能可以给大画幅相机装一个滑动接片的数码后背，实现比如6x9的数码相机；3) 现在的graflex毕竟是金属的，带起来非常麻烦。我又有一个229mm成像圈的Super Angulon XL大广角。如果可以全3D打印一个塑料的6x12甚至6x17胶卷相机，携带就非常方便。因为之前点过各种奇怪的电子技能点，所以还可以加入各种魔改，比如自动对焦的6x12之类。

所以我就花了一些时间做了一些计算和调研3D打印。3D打印从原来上来说基本上分成两类技术，FDM塑料打印和SLA松香打印。具体原理和子类暂且不谈，总之二者的区别就是一个便宜（1000刀可以买到一个相当好的）一个死贵（同样大小的需要10000刀，还是预售，明年发货）。计算了一下，决定需要购买至少能打印250mm的机器。上亚麻价格从低到高排序以后，就你了启迪！（此处应有广告费

决定3D打印以后，最关键的就是建模了。这里有几个挑战，第一是我不会建模。。第二是我的数码相机是Leica L卡口，就是马徕松那个L卡口。这货傻逼的地方在于它的物理标准根本没有公布，网上根本找不到现成的模型或者数据（只有wiki上有个外径51.6mm）。第三是关于如何实现滑动接片的机械设计我也是两眼一抹黑。只能走一步算一步了。

关于建模，上网找到一个很好用的工具叫OpenSCAD。总之就是一个码农写的工具，写代码来建模。看教程上来先跟你讲什么叫变量，什么叫函数，如何用递归（？？？）来画一颗3D的树，然后学list comprehension。。雾草，建模建得爽到飞起。还可以git, vim, 库依赖管理，#include甚至python生成代码来建模，各种骚。。额扯远了。总之就是很容易就把后背设计好了：

![3D model](/images/large-format-back-3d-model.jpg)

大括号不能换行，不然打你

建模的问题解决以后，下一步就是逆向徕卡的卡口了。不要跟我说什么倒角，强度，公差，就是卷尺量一把梭。能用矩形描述的东西就不要用多边形，3D打印有误差塞不进去就用砂纸磨。迭代了5轮以后终于暴力塞进去了。。

![Leica L Adapter](/images/large-format-back-adapter.jpg)

然后下面就是把背板和数码相机接合起来的机械结构了。这个比较简单，只需要支持左右滑动。那就搞个槽往里面插呗。里面有个坑是3D打印不是万能的，他没有办法在空中打印出东西。所以在打印槽的时候大多数情况下下面需要打印一些支撑部件，然后成品以后把支撑剪掉/磨掉。这个非常麻烦。所以我把槽改成了斜的，就是dovetail（鸠尾榫？）。这样就不用打印支撑部件了。此外还踩了一些公差的坑，细节不表。最终打印出来打两个部件组合起来长这样：

![Final result](/images/large-format-back-result.jpg)

然后这里还有个问题是，我的相机手柄太长，会直接打到大画幅机身上。。导致这个滑板到一个位置就被卡住了。。只好把滑板后面的部分拉长。这样问题倒是能解决，但也导致没办法用广角镜头，只能用标准头或者长焦。那么装上机器试试看，诶，能成像。

![Put camera on](/images/large-format-back-with-camera.jpg)

不要在意机身歪了的细节。量角度的时候量少了几度。。

![Technical movement](/images/large-format-back-front.jpg)

做技术动作也没有压力

那么拿来拍个照呢？我比较担心的是大画幅的镜头分辨率不如全画幅，不过想想接片应该可以克服这个问题。

![Color sample photo](/images/large-format-back-sample-photo.jpg)

彩色，这张120MP

![Color sample photo 2](/images/large-format-back-sample-photo-2.jpg)

黑白，这张60MP（a7r4默默微笑

操作也比较顺滑，感觉比较实用了。拍一张照片大约需要20张接片，3分钟左右。考虑到大画幅拍照普遍比较慢，这个overhead也算可以忍。而且分辨率比胶片还是要高很多的，也省掉了冲洗，扫描，去色罩的麻烦。不过当然胶片更好玩。

整个过程还是很有意思的。从周四晚上有这样的想法，到调研购买3D打印机，包括砂纸游标卡尺等配件，学习建模，逆向卡口，学习3D打印比如支撑的设计，打印迭代，到周日晚上完成。很有成就感。而且还不是全速进行，周末还在肝AAAI（？？？），总之就是想装个逼就是了。另外也逆向出了graflex的镜头板，网上二手的卖30，算了一下打印成本一毛钱。。可以说是非常划算了。

下一个目标就是612全塑料胶片机啦，毕竟比接片灵活也好玩一些。目前想的是冷靴插个黄斑测距，螺纹套筒非联动对焦，镜间快门，眼平取景（自己糊一个或者用iphone也行，顺带也能测光了）。如果能学习一下弄成旁轴联动对焦就爽了，612那么长的机身不用来做黄斑测距真是可惜了。先学学紧固件的打印，过段时间攒够知识了再肝吧。
