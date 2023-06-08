Title: 深空摄影器材从观望到破产（二）——赤道仪的选购
Date: 2023-04-26 23:30
Category: Life
Tags: astrophotography
Slug: astrophoto-tutorial-2

从这篇文章开始，我们将详细介绍每个深空摄影组件。这个介绍的目的是清晰地梳理器材的关键参数，以及厂家为了实现和改进这些参数所做的努力。在这个过程中，我们可以了解哪些特性值得投资，哪些特性相对过时且不必花钱。我写作的目标是做一个较为全面的介绍，所以如果读者对这些话题感兴趣，可以阅读；如果不感兴趣，也可以将其作为搜索参考。

这篇文章主要介绍赤道仪的用途和发展。赤道仪有两个主要功能：一是提供指向功能，大多数赤道仪都具有goto功能，可以帮助我们轻松地找到想要拍摄的目标；二是跟踪功能，让我们在拍摄过程中始终锁定目标，避免星点出现拖线。赤道仪的核心指标包括精度、载重、重量和价格。其中，载重、重量和价格都是比较直观的参数。在这篇文章中，我们特别关注赤道仪精度在多年发展中的逐步提升，以及在提升过程中遇到的困难和采用的解决方案。

## 赤道仪的结构

赤道仪的结构相对简单，基本上包括三个组件来完成其核心任务。首先，它有一个电机来提供动力；其次，有一个减速机构，使电机的转速经过大比例减速后能够与天空的转速相匹配；最后，它还有一定的平衡机构，以防止电机过载。此外，还有一些其他支撑结构，如经纬度调节和极轴镜等，但这些与赤道仪的核心功能和指标关系不大，所以不再详述。

电机和减速结构是直接决定赤道仪性能的关键环节。由于天空旋转速度非常缓慢，每24小时才旋转一圈，而一般的电机转速是以每分钟转多少圈来衡量的，二者之间存在巨大的差异。所以赤道仪需要一个非常大的减速比的减速结构，这是它与一般电机的主要区别。

为了实现很大的减速比，市场上主要有两种常见方法：一种是基于涡轮涡杆的减速结构，另一种是基于谐波减速机的减速结构。涡轮涡杆可以看作是两个互相咬合的齿轮经过变形后得到的机械结构，它可以提供比传统齿轮咬合更大的减速比，因此广泛应用在赤道仪上。谐波减速机则是在工业机器人上广泛使用的一种减速机构。关于这两者的优劣，我们会在下面关于精度的具体分析中详细介绍。但由于赤道仪所需的减速比实在太大，所以一般还会有一个二级减速结构，比如齿轮或者皮带。

## 赤道仪的误差来源

在了解赤道仪的基本结构之后，我们可以分析赤道仪跟踪的误差来源。换句话说，只有了解误差来源，我们才能知道如何进一步提高赤道仪的精度。

赤道仪的根本误差来源于加工制造的不完美造成的转速不均匀。由于涡轮涡杆和谐波减速机本质上都是周期性运转的组件，这个转速的误差又叫周期性误差。对于涡轮涡杆减速机来说，周期误差很容易建模和测量，因为蜗杆转一圈就是一个周期（蜗轮一个周期是24小时）。然而，谐波减速机的原理相对复杂，它是一个柔轮在类似齿轮的结构中不断旋转，利用两者周期之间的差异来实现减速。由于涉及到两个不同的周期，谐波减速机的周期误差非常复杂，在实际应用中，可以认为它的误差是没有明显规律的。

对于涡轮涡杆减速机来说，有一种简单的对抗周期误差的方法叫做周期误差纠正（PEC，Periodical Error Correction）。其基本思路非常简单，就是记录下涡轮涡杆的周期误差，并将其反向播放来对抗。在一些软件如pempro中，可以利用类似的PEC方法有效降低周期误差。然而，对于谐波减速机来说，这通常不是一个可选项。

从控制论的角度来看，PEC是一种开环控制，就像开车时把油门始终固定在一个角度。这样可以在某种程度上实现定速，但当汽车上下坡时，由于没有相关信息，无法根据实际情况进行调整，修正效果不够好。相对应的更好方法是闭环控制，类似于开车时的定速巡航。行车电脑会不断检查汽车实际速度与规定速度之间的差异，并根据一定算法调节油门大小，实现汽车以一定速度行驶。

对于赤道仪来说，我们想实现的目标也是一样的——希望赤道仪以固定的角速度，即天球转动速度进行定速巡航。PEC就像是一个埋头拉车、固定油门的纠正方式。如果想要效果更好的纠正方式，我们可以给望远镜装上一个“眼睛”，换句话说，从控制论的角度来看，就是进入闭环控制。

闭环控制的方法有两种：一种是导星，一种是码盘。当然，小孩才做选择题，大人都是全都要。实际应用的过程中很多时候是两个都用的。

导星的基本思想很简单：除了主镜和主相机，我们还有一个导星镜和导星相机。它们以比主相机更高的频率比如每秒一张对天球进行成像。在这个过程中，电脑会比较最新的照片和之前的照片，如果发现有位移，就说明赤道仪的跟踪有问题。通过一些算法，电脑可以生成修正信号，让赤道仪速度加快或减慢，从而实现跟踪速率的修正。因为整个系统有传感器来直接测量修正的结果，所以这个过程叫做闭环控制算法。

码盘的原理和导星类似，也是闭环控制算法。但它不需要额外的光学组件，而是在赤道仪内部有一个精密测量角速度的码盘。需要注意的是，码盘必须放在减速机后面，因为大多数周期误差来自减速机。虽然将马盘放在减速机前面看似精度会提高，但实际上效果并不好。为了实现好的纠正效果，码盘需要有很高的分辨率，这导致了含有码盘的赤道仪价格很高，通常在一万美元以上。

当然，码盘这么贵，肯定有自己的独特优点，除了高分辨率外，它对导星系统没有要求，可以实现所谓的盲跟。在焦距很长、拍摄天区很暗、没有亮星的情况下，这是一个非常有用的特性。

## 导星系统

由于成本控制等原因，大多数系统中仍然使用导星系统。因此，很多精力被投入到提高导星系统精度的研究上。导星系统是一个控制系统，其精度主要取决于控制算法以及影响控制算法工作的一些特性，如回差、转动惯量、大气扰动和蒙气差等因素。

导星过程需要对赤经和赤纬两个维度进行分别控制。但这两个维度赤道仪所面临的情况是不一样的。在赤经（东西方向）上，赤道仪需要不断运动；而在赤纬方向上，赤道仪本质上是静止的，只需要偶尔纠正过大的偏差。因此，赤经和赤纬方向往往使用不同的控制算法。

回差在摄影社区中也被称作旷量，它是由于齿轮没有完全啮合等原因造成的一种现象。当一个齿轮转动时，另一个齿轮并没有跟着转动，通常是因为齿轮之间啮合的齿的个数不够，或者加工精度不足导致的。回差往往只在切换运动方向（回头）的时候才出现，因此叫做回差。回差会影响控制算法，因为当控制算法发送一个控制信号后，它实际上对系统并没有造成任何改变，这会给控制算法带来额外的不确定性。解决方法通常是精确测量回差，并在发送信号时加上提前量。例如，在改变修正方向时，将回差加到修正量里，从而实现合理的控制。

一个非常重要的控制系统特性是整个系统的惯性，它决定了系统对扰动的稳定程度。这会直接影响控制算法的参数设置。因此，转动惯量作为导星系统的“惯性”非常重要。通常，我们希望尽可能减小转动惯量以提高系统的稳定性。例如，在能够平衡赤道仪的前提下，我们更愿意使用多一点的重锤并将其放在离传动轴较近的地方（比如10kg的重锤放在0.5m处），而不是使用较少的重锤并将其放在离传动轴较远的地方（比如5kg的重锤放在1m处）。这是因为尽管两者的力矩相同，但后者的转动惯量更大，会影响导星系统的稳定性。

除此之外，大气对整个导星过程也会产生影响。大气的扰动主要是指在非常局部范围内，大气密度会有一些随机变化。这种变化会导致光线发生偏折，从而给导星系统传递一个错误的信息，使其误认为星星的位置发生了变动。实际上，这仅仅是由于大气折射引起的。这对导星系统是一个不良影响，而且非常难以消除。要想彻底消除这个因素，必须使用专业级别且极其昂贵的自适应光学设备。但对于民用器材和爱好者来说，这并不现实。

类似的因素还有蒙气差，它是当天体的高度角较低时，穿过的大气形成一个楔形，从而也会导致一定程度的折射。在导星算法中，应适当为这个因素进行补偿。

## 中天翻转和极轴

除此之外，赤道仪还有一些与实际使用体验相关的特性和操作，例如中天翻转。中天翻转是某些赤道仪设计中的一个特点。它指的是当待拍摄的天体过中天时，如果继续让赤道仪拍摄，某些赤道仪设计中的相机可能会撞到三脚架或赤道仪的其他突出部位。但在有些设计中，尤其是赤道仪向前突出且相机和主镜较短的情况下，相机可能不会撞到赤道仪的其他部分或三脚架，这时就可以不进行中天翻转而继续拍摄。例如，阿瓦隆和派拉蒙的金牛座赤道仪都有类似的设计。这种设计可以一定程度上节约拍摄时间，但也带来一些刚度和成本问题。在选购赤道仪时，我们可以考虑自己的器材是否适合这样的设计，是否可以通过选购类似的器材来避免中天翻转。

中天翻转一般来说不是什么大问题，但在某些控制系统下，它可能会导致一些奇怪的不稳定问题。例如，判断一个天体是否过中天的算法依赖于当地的时间，但有些地方会有夏令时和冬令时，这就会造成额外的不确定性。如果相关设置没有正确设置，就可能导致拍摄时间的浪费，甚至打腿。

在赤道仪拍摄过程中，还有一个重要的操作是抖动。抖动是指在拍摄一张或几张图片之后，赤道仪进行一个微小的角度调整。这样可以确保，即使在使用高精度导星的情况下，每颗星星落在相机上也会落在不同的像素上。这样就可以避免一个亮点或者坏点导致整个画面受影响的情况。在后期处理时，可以轻松地通过排异等算法将相机的固定模式噪声消除。

要让赤道仪工作得很好，一个关键步骤是对准极轴。极轴对准的主要目标是将赤道仪的传动轴与天球的转动轴完全对齐。这样，在赤道仪进行跟踪时，只需使用赤经轴的转动来进行跟踪，可以大大降低或消除场旋等导星无法修正的偏移因素。

具体来说，场旋是指拍摄的照片中，以图片中心为原点，星星呈圆周式拉线。当导星有问题时，星星会呈平行拉线。通过判断星星拉线的模式，可以判断是场旋还是导星的问题。当拍摄的照片出现场旋时，通常说明极轴校准有问题。

极轴对准通常有两种方法。一种方法是使用光学极轴镜。它的原理是在赤道仪的传动轴上嵌入一个与传动轴同轴的光学望远镜。只要将这个望远镜对准北天极，就可以实现极轴校准。但是，因为北天极和北极星之间存在一定程度的位置差异，所以我们通常不是将北极星放在望远镜视野或十字丝的中心，而是通过app查询当前地点和时间的北极星对应位置，然后将北极星放在规定的刻度上。

光学极轴镜的优点是对准速度很快，但缺点是精度可能不如其他方法高，同时对同轴的要求非常高。而且，在对准极轴的过程中，通常需要人蹲在地上操作，对体力要求较高。

另一种对极轴校准的方法是利用电脑拍照，然后通过算法和一些预定的动作来计算极轴，并指导用户进行校准过程。常见的方法有电子极轴镜和用主镜来对极轴，例如ZWO的盒子和电脑上的sharpcap都支持类似的功能。其基本原理是在某个位置拍一张照片，然后旋转赤经例如60度，再拍一张照片。通过比对和解析这两张照片，可以定位出旋转轴。在理想情况下，旋转轴的赤纬应该是90度。我们可以通过对比计算出的旋转轴和赤纬90度的北天极之间的位置差异，来指导用户逐渐调整经度纬度调节装置，使二者重合。

这种方法更加灵活，因为它不需要极轴镜或主镜与赤道仪的同轴。甚至可以实现全天对极轴的校准。通过更复杂的算法，我们可以拍摄多于三张的图片，从而进行更精确的计算，指导用户一步一步将图像旋转的位置迭代到北天极上。

我个人认为电子极轴镜的精度不如主镜的精度。原因是主镜，无论是相机还是光学器件，其分辨率都比电子极轴镜的入门相机和短焦镜头要高。（此处存在争议，我还在进一步学习）

## 小结

总的来说，赤道仪是深空摄影的一个核心组件，其关键指标是精度。为了提高精度，厂家一方面需要提高加工精度，对于涡轮涡杆减速机，还可以采用PEC等技术进行开环控制。同时，可以利用导星和马盘等方法进行闭环控制，以增加精度。我们还介绍了导星的基本思路，影响导星精度的因素，以及赤道仪在使用过程中的中天翻转、抖动和极轴校准等常见操作和注意事项。希望这篇文章能对你选购赤道仪有所启发。

感谢仓鼠，国宝和dede对本文的指正！