Title: 如何拍摄银河 
Date: 2018-07-08 12:49
Category: Life
Tags: Photography, Astrophotography
Slug: milky-way-photo

没想到在西雅图的郊区也能看到壮美的银河。

![Milky Way 1](/images/milky-way-1.jpg)

![Milky Way 2](/images/milky-way-2.jpg)

![Milky Way 3](/images/milky-way-3.jpg)

在做任何事情以前，都要想清楚目标是什么，或者说做成什么样算是“好”的。对拍照这种事来说，当然没有一个“正确”的目标，或者说什么照片就是“好”的。对我而言，因为没什么文化，我在看到银河的时候只有连呼卧槽。所以我在照片里也想把这种卧槽的思想感情表达出来，希望也能感染观众。让看到的人也说一句卧槽，这个照片就成功了。作为一个理工男，我也希望在技术上这个照片是没有错误的，或者说照片的瑕疵要少，经得起放大：星星没有拖尾，整个幅面的星星看起来都是一个个点而不是糊成一坨，照片干净没有噪点没有杂色。此外，我也希望这个照片有点意思，最好是一组组图，从不同的角度表达卧槽的思想感情。比如不要只是单纯一个星空，最好有点有意思的前景，或者有银心特写等等。

定义好了想要实现的目标以后，下面就是具体实施了。因为这个目标比较宽泛复杂，我们需要进行一定程度的分解。具体地说，我们可以把目标分成三个阶段：

* 要把银河拍出来
* 把银河拍清楚
* 把银河拍的有意思

下面我们一个一个分析怎么实现。

要把银河拍出来，基本有天时地利即可。所谓天时是晴天，新月，银心足够高，大气宁度高。地利是光污染小，视野开阔。天气月相和银心位置在一些摄影app或者网站上都能查到，我用的是PhotoPills，安利一发。光污染有专门的地图，直接bing上搜light pollution map就有。视野可以用卫星图和街景来看。大气宁度主要受大气对流的影响，大概的说是晴天高温对流大，水陆交界对流大。尽量避开这两种条件。满足天时地利以后，随便找个入门相机，放三脚架上长曝一把，基本都能拍出来银河。

把银河拍清楚需要一点技术。首先我们要理解为什么会拍不清楚。这主要有三方面的原因：第一，地球在自转，星星在跑。曝光时间一长星星就拖尾了；第二，暗光下曝光信噪比有限，同时长曝会引入热噪音；第三，镜头有慧差（入射光角度与光轴角度偏差过大时成像的不完美，PSF类似彗星所以叫慧差）。这三个问题的解决是彼此矛盾的。要解决第一个问题往往需要降低曝光时间，但降低曝光时间又会降低信噪比增强噪点和偏色。要解决第三个问题往往要降低光圈，但降低光圈又会降低信噪比。一般来说，工程上有两种解决方法，一种暴力简单效果好，一种复杂且效果略差：

* 方法一：堆器材，买买买。买赤道仪/星野赤道仪/极轴镜解决长曝，买冷却大幅面CCD解决信噪比，买牛逼镜头在大光圈的同时解决慧差。效果立竿见影，"只"要几万美元，不需要什么额外操作就可以出技术上完美的片子。
* 方法二：基本上是拍深空的那一套，向右曝光爆ISO，平场暗场亮场拍起来，n张合成以实现信噪比sqrt(n)级别的提升。搜索关键字是深空天体摄影或者DeepSkyStacker。适当缩小光圈把慧差控制在可接受范围。几个小坑要注意：第一，500 rule或者600 rule是胶卷时代的东西了，不适用于现代高密度数码相机。感兴趣的话可以用像素密度，焦距和赤纬自己算曝光时间，懒人可以直接上网用app算。再安利一发PhotoPills。第二，有防抖的镜头或机身上三角架的时候记得关防抖。第三，对焦和曝光都需要长曝确认，不要拍了一晚上回来发现星星都是一团就傻逼了。

关于慧差多说两句，它的本质是镜头的成像面是曲面。当我们用一个平面的CCD去截取的时候，边缘部分自然就糊了。如图所示。

![Coma](/images/milky-way-4.png)

另外，下面是一个合成降噪的例子。第一是向右曝光的原片：

![Original photo](/images/milky-way-5.jpg)

这样可以让传感器搜集尽可能多的光，降低shot noise。因为我打开了相机内置降噪，所以相机自动帮我拍了暗场并修正了，这里基本没有热噪声(thermal noise)。在Lightroom中修正曝光并裁剪以后可以得到下图：

![Revised1](/images/milky-way-6.jpg)

可以看到颜色和纹理都出来了。但总体噪音还是很大。什么叫噪音大呢，就是整体泛白，纹理不显著。要是强行升高对比度，你希望它黑的地方反而会更亮，而不是变黑。因此我拍了16张图，用DeepSkyStacker进行了叠加：

![Revised2](/images/milky-way-7.jpg)

可以看到明显更清澈了，该黑的地方黑，该亮的地方亮。但因为长曝的原因，对齐了星空之后树木产生了拖影（这也是为什么开始要把下面的前景裁掉的原因，为了避免干扰对齐）。所以在Photoshop中再重新加入前景，得到最终成图：

![Revised3](/images/milky-way-8.jpg)

把银河拍得有意思就更属于创意方面的范畴了。这里只是提出几个问题，抛砖引玉。

* 为什么网上很多教程说要用广角？这是技术的考量还是美学的考量？如果是技术，广角是必须的吗？如果是美学，有其他途径吗？
* 拍银河要想表达卧槽的思想感情，直接拍银心或者银河都是合理的。如果有其他想法想表达呢？前景应该如何选择？可能有哪些方式？
* 夜晚有哪些其他的玩法？光绘，LED动画光棒能否加入？
* 能不能把照片拓展到视频呢？
