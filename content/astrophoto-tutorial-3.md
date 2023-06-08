Title: 深空摄影器材从观望到破产（三）——天文相机的选购
Date: 2023-04-28 20:30
Category: Life
Tags: astrophotography
Slug: astrophoto-tutorial-3

这篇文章主要介绍深空摄影器材中非常核心的一个部分，相机。请注意，这篇文章包含了我的很多主观看法，所以请大家谨慎鉴别，带着批判的态度去看待。

## 信噪比

相机在深空摄影器材中的作用主要是进行光电转换，把望远镜收集到的光子转化成电子，这样才能方便我们进行后期处理。

相机的一个核心指标是噪点，但严格来说，噪点取决于信号强度和噪声强度。一般来说，大家并不仅仅关注噪声本身的绝对数值，而是更关注信号和噪声之间的比值，也就是信噪比。信噪比越高，图像看起来就更干净。

这里涉及到一个归一化的概念，尤其在相机的相关分析中尤其常见。在衡量相机噪声时，大家会把不同相机的信号强度换算成一样，然后在这个前提下比较不同相机的噪声大小，这个过程就叫做归一化。而信噪比就是这个过程的产物。

## 重要的指标

选购和分析相机指标是一个相对复杂的过程。我认为相机有八个相对重要的指标和三个相对不重要的指标。了解这些指标后，我们在看待各个厂商的宣传时就会更加明确，知道哪些是商业化的话术，哪些是真正的技术。首先，我们来看相机的一些相对重要的指标。

1. 量子效率：第一个是量子效率，也就是QE。QE的严格定义比较复杂，但直观地说，QE可以看做是一个光子打到传感器上能产生多少个电子。QE越高，相机的效率越高。这意味着高效率的相机拍摄一张照片可能相当于效率一般的相机拍摄两张或一点几张照片。因此，它对于我们快速积累图像和高质量图像有直接帮助。

2. 频率响应：然而，QE并不仅仅是一个数值。尽管各个厂商在标注QE时往往只标最大值，但在购买时我们需要留意并结合频率响应来看。频率响应是指相机对不同频率或不同波长的光的QE值。如果我们将其绘制在一张图上，横坐标为波长，纵坐标为QE或响应，就会形成一个曲线。这个曲线可以反映相机对不同光的敏感程度或效率大小。  
  厂商标注的QE通常是曲线中的最大值。但是，如果要仔细研究，我们不仅要看最大值有多少，还要看它随着波长的变化，相对于最佳波长的效率如何变化。这样综合衡量出来的指标就更加准确。

3. 热噪声：为了理解热噪声的重要性，我们需要先了解相机噪声的主要来源。一般来说，相机的噪声有三个来源：读出噪声、热噪声和量子噪声。这些信息在网上都有很多资料可以查阅。  
  读出噪声是指每次相机进行读出量化时产生的噪声；热噪声是指相机在曝光过程中每个像素都会产生的噪声；量子噪声（或光噪声）是由于物体接收到的光具有一定的随机性而产生的噪声。在这三种噪声中，读出噪声和热噪声是和相机有关的。读出噪声只和读出动作有关，而热噪声和时间有关。  
  在深空曝光过程中，每一帧都需要几分钟甚至几十分钟的曝光时间。在这么长的时间里，热噪声会不断积累，而读出噪声只会发生一次。因此，在深空摄影中，热噪声是主导噪声，而读出噪声相对不那么重要。但在行星摄影中，情况恰好相反。每一帧的曝光时间只有几毫秒或几十毫秒，因此会有很多读出动作，使得读出噪声成为主要噪声，而热噪声相对不那么重要。一个热噪声更低的相机，在深空摄影中就可以支持更高的信噪比。

4. 制冷：这引出了第四个重要因素：相机的制冷。热噪声通常与传感器的温度呈指数关系。传感器温度越高，热噪声会急剧增加；相应地，降低传感器温度，热噪声会急剧减少。但对于现代CMOS来说，这种降低是有限度的。当温度降低到一定程度后，再降低温度对噪声的减少意义不大。例如，噪声可能已经低于天光或月光的影响。  
  经验上来看，对于现代CMOS，制冷到零下10度以下就没有太大意义了。具体的计算可以参考镜子的速度、当地的光污染以及相机型号的热噪声来进行定量计算。

5. 辉光：第五个需要注意的参数是辉光。由于前几代传感器技术的限制，有些相机在成像时会出现辉光，即相机边缘的一角有一个像放射状的亮光。这并非漏光，而是相机在成像过程中产生的杂讯。辉光可以通过后处理解决，如通过严格时间匹配的暗场来去除。但无论如何，它都会影响信噪比。最新的传感器通常没有辉光问题，这些传感器在后处理和校准时会省很多事，如可以利用暗场的自动优化，而不用每个亮场都要拍严格等时的暗场。同时，信噪比也会有所提高。

6. 后截距：相机的后截距主要是指相机用来连接的组件，如螺纹或螺丝孔与传感器之间的距离，这个概念与摄影中相机的法兰距意义一致。后截距越短，意味着在望远镜的后截距上能利用的空间就越大，它们之间是此消彼长的关系。因此，低后截距的相机在灵活性方面往往更好。

7. 稳定性：这个不言而喻，如果相机卡顿或需要频繁重启，或者漏油、不能制冷，这些都是非常糟糕的情况，会直接干扰我们对相机的使用，浪费宝贵的时间。

8. 最后一个重要指标是固定模式噪声（FPN）。当相机在拍摄亮场、暗场或偏置时，如果校准帧非常随机，那么这是一种好现象，因为随着多帧叠加，这种噪声往往会自我消除。但如果在偏置或暗场中有固定模式的噪声，它往往无法通过多帧叠加来消除。例如，佳能相机的彩色条纹就是这种情况，对后期处理非常不利。因此，固定模式噪声也是相机的一个非常重要因素。

## 不重要的指标

除此之外，还有一些不太重要的指标，其中一个是温飘。温飘是指在相机进行冷却拍摄过程中，如快速拍摄多帧时，相机的冷却可能跟不上拍摄过程中的发热，导致温度出现波动。我个人认为温飘并不是一个重要因素，有三点原因：

第一，拍摄偏置在现代CMOS相机中应该是非常罕见的。这是因为与传统的CCD不同，现在的CMOS相机的偏置可以建库重用，没有必要每次开机都重新拍摄。这可以通过实验验证，例如在CMOS的相机如6200或268上开机拍摄一组偏置，合成一个主偏置，然后关机再开机拍摄一组偏置，合成一组主偏置。将这两个主偏置在PixelMath中相减再取绝对值，可以看出它们之间的差异非常小。因此，对于现代CMOS相机来说，偏置是完全可以重用的，所以温飘问题最多一年也就影响一两次。

第二，温飘本身对偏置的影响也非常小。这也可以通过实验验证，例如在零下10度拍一个偏置，零下5度拍一个偏置，合成后用pixel math相减，会发现它们之间的差别几乎没有。因此，温飘更多的是一个强迫症的行为，并不是真正会对拍摄带来影响的事情。

第三，如果你真的有强迫症，温飘问题也很容易解决。在拍摄偏置时，可以适当拉长每两帧之间的间隔，例如在拍摄一帧偏置后停5秒钟，再拍摄下一帧偏置，给冷却算法和冷却硬件一个反应时间，这样就可以很好地遏制温飘问题。

综上所述，温飘影响的环节是一个非常罕见的现象，其影响也非常小，而且很容易解决。因此，完全没有必要花大量精力来解决温飘问题，所以我认为温飘并不是相机的一个重要指标。

第二个不太重要的指标是缓存。通常，体育摄影非常重视缓存，因为它意味着我们可以连续拍摄，在写入内存卡的过程中，将这些拍好的照片先放在缓存里，然后等到有时间再慢慢写入卡中。对于行星摄影也是类似，缓存可以让我们用空间换时间，在短时间内拍摄很多帧。但是对于深空摄影来说，因为每一帧曝光都需要五分钟或十分钟，即使是慢速的内存卡也足够将照片写入，所以缓存对于深空拍摄来说并不重要，大小和速度都不关键。但这也不是绝对的，比如在拍摄偏置和平场的时候，一个更大的缓存可能会给我们略微更好的体验。为什么说略微更好，这是因为前面提到偏置不经常拍，而平场一帧经常要一秒甚至好几秒，这时候写卡的压力也不是很大。

第三个不太重要的指标是相机的读出速度。例如，最新的传感器系列，如455、268、6200、2600等，它们的读出速度都很慢。这在日常摄影中可能会有问题，比如Sigma的FP L或Leica的M11在使用电子快门时，果冻效应非常明显。但是对于深空摄影来说，因为天体本身是静止的，不需要考虑果冻效应，所以读出速度对于深空摄影并不重要。然而，对于行星摄影来说，读出速度非常重要，因为行星摄影的效率很大程度上取决于帧率。帧率越高意味着在单位时间内，在曝光允许的前提下，能够拍摄更多的帧数，更早地完成拍摄任务，例如在木星自转一定角度之前完成拍摄。所以，对于行星摄影来说，读出速度非常重要，只是对于深空摄影来说不太重要。

## 黑白与彩色相机

接下来，我们来讨论一个常见问题：在天文摄影中，应该选择黑白相机还是彩色相机？这个问题需要从多个方面来判断。首先，我们来看一下黑白相机和彩色相机的主要差别：黑白相机没有拜耳滤镜，因此拍摄的图片只有亮度而没有色彩。相反，彩色相机有拜耳滤镜，所以在解析图片时需要进行拆色或去拜耳的步骤，因此其空间分辨率比不上黑白相机。不过，无论是黑白相机还是彩色相机，在天文摄影领域中，它们都没有UVIR滤镜，所以它们的频率响应都比较全面。唯一的区别就是彩色相机有一个拜耳滤镜。

接下来，我们从五个方面来判断它们的优劣：

1. 拍摄的繁琐性：彩色相机和普通摄影相机一样，只需接到望远镜上就可以拍摄。而黑白相机需要配置RGB滤镜或SHO滤镜以及相关的滤镜轮和滤镜抽屉等配件，前期难度更高，投入也更大。

2. 效率：黑白相机通常采用LRGB四种波段拍摄，而彩色相机根据拜耳阵列采用RGGB排布拍摄。人眼对明度细节敏感，对彩色细节不太敏感。因此，黑白相机通过合理安排LRGB通道的时间，可以获得比彩色相机更高的效率。此外，黑白相机的L通道光损失更小，也是其效率更高的原因。

3. 分辨率：彩色相机因为有拆色过程，分辨率比不上黑白相机。但在后期处理中，可以采用CFA Drizzle方法来提高分辨率。这种方法效果是有的，但也有一定的局限性，但总体来说，黑白相机的分辨率还是要比彩色相机高一些。

4. 灵活性：彩色相机的拜耳滤镜主要是RGGB排布，这对天文摄影来说并不友好。这是因为除了彗星等少数天体以外，天体没有呈绿色的。因而安排两个G通道非常不划算。黑白相机可以灵活调整RGB三个通道之间的比值来适应天体的光谱，而彩色相机无法做到这一点。

5. 成本：黑白相机的价格通常比彩色相机高很多，这可能是因为黑白相机的产量较低，固定成本无法有效分摊。此外，滤镜成本也是一个重要因素。一般来说，滤镜是一个深空摄影系统中最贵的组件。总体来说，如果加上滤镜的价格，黑白相机的价格可能是彩色相机的2到3倍。

总结以上几点，我们可以根据自己的需求和预算来选择黑白相机或彩色相机。

## 数码相机与改机

我们在讨论相机时，经常听到一个问题：我有一个数码相机，能否直接用它作为天文相机拍摄？答案是肯定的。数码相机和彩色天文相机非常相似，主要有两个区别。首先，数码相机有自己的UVIR滤镜，它会过滤掉紫外线和红外线，相当于彩色相机加了一个L滤镜。其次，数码相机通常没有恒温设计，而彩色天文相机有半导体制冷和风扇散热的恒温设计。

这两个区别导致了一些技术上的不同。数码相机因为UVIR滤镜的存在，对红外和紫外等波段的量子效率特别低，有时会影响到一些接近红外端的深红色光，如氢发射谱线。这对拍摄发射星云非常不利，也是为什么用数码相机拍摄调色盘等对象时很难把红色的星云拍出来。但如果用天文相机拍摄，红色很容易出现。另一个恒温功能对于热噪声的控制非常重要。它不仅可以输出更纯净的画面，另一方面，如果要通过暗场矫正相机的热噪声，暗场和温度密切相关。因此，提供恒温功能后，我们可以严格按照拍摄亮场时的温度来拍摄暗场，从而最大程度地校准热噪声。数码相机在这方面的校准精度会受到很大影响。

所以，传统数码相机具有更低的量子效率、更高的热噪声和更不精确的校准，总体性能比天文相机要低一个档次。有一种方法可以在一定程度上解决这个问题，那就是改机。改机是指去掉数码相机CMOS上的UVIR滤镜，从而提高数码相机在紫外和红外波段的量子效率。这样在拍摄调色盘等发射星云等含有发射星云的天体时就会少一个劣势。

但是，改机看似好，实际操作有三个问题。首先，因为相机可以感知到更多的红外光，日常生活摄影中的白平衡会出现问题，颜色会偏红。这可以通过在日常摄影时额外插入一个UVIR滤镜解决。其次，改机会改变光程，导致镜头的像差劣化，拍摄时星点不如原来好。这主要是因为相机的镜头和都是针对一定的法兰距和光程设计的，改机时移除了UVIR滤镜，破坏了这些光学设计的前提，就会造成星点的劣化。因此，日常拍摄时如果要加入UVIR滤镜，应尽可能使用Clip-in滤镜，加在镜头和CMOS之间，以尽可能还原改机前的滤镜情况。第三个问题是改机后可能出现眩光和辉光，其中具体原因尚有争议，但总的来说，改机后可能出现一些难以修复的问题。

因此，对于刚入门的新手，如果手头有数码相机，建议先用手机的数码相机拍摄，不要急于投入大量资金。等确定自己真的感兴趣以后再升级。如果有闲置的相机，而且觉得有拍摄发射星云的需求，可以进行改机。但没有必要为了改机而单独购买一个数码相机。相反，可以考虑直接购买一个彩色天文相机或黑白相机，从长期来看可能具有更好的经济性。

## 从校准帧看相机好坏

最后我想稍微谈一谈校准帧。在这里，校准帧主要指的是偏置和暗场。我们假设大家已经了解偏置和暗场的拍摄目的、校准方法和拍摄方法。我们主要讨论如何评价一个相机的校准帧。我个人认为，通过校准帧来看一个相机的好坏主要有两个方面：一个是FPN（固定模式噪声），另一个是MAD（校准帧空间上不同像素的起伏）。

之前已经解释过FPN，如果FPN比较明显，在后期处理时无法通过叠加来去除，会给后期制作带来很大困扰。而MAD主要是一种衡量噪声大小的方法。在校准帧的拍摄中，尤其是偏置和暗场的拍摄中，没有任何信号，我们拍摄的就是一个纯噪声场。因此，在这个过程中，我们只需要定量地衡量噪声的绝对值，而不用考虑信噪比。在这种情况下，可以非常简单地用MAD或类似的标准差来衡量校准针的噪声尺度。

因此，如果一个相机没有很固定的噪声模式，也就是没有FPN，且它的校准帧像素值分布非常集中，像素值的分布基本上为零，那么这个相机就是一个好相机，它会给我们的后期制作带来很大优势。

总的来说，这篇文章主要介绍了相机的用途、评价的核心指标、八个重要的指标、三个不重要的指标、黑白与彩色相机的差异，数码相机改机，以及如何利用校准帧来辅助评价一个相机。希望这些内容能给大家在选购相机时，抵抗厂商的推销话术带来一定的启发。