# H.264、H.265、VP8、VP9相关

## H.265

H.265是ITU-T VCEG继H.264之后所制定的新的视频编码标准。

H.265视频格式标准在2013年1月25日由国际电信联盟（ITU）正式宣布,最高分辨率可达 8192×4320。 

H.265可以实现利用1~2Mbps的传输速度传送720P（分辨率1280*720）普通高清音视频传送。

H.265旨在在有限带宽下传输更高质量的网络视频，仅需原先的一半带宽即可播放相同质量的视频。

H.265标准也同时支持4K（4096×2160）和8K（8192×4320）超高清视频。

H.265/HEVC的编码架构大致上和H.264/AVC的架构相似，主要也包含，帧内预测（intra prediction）、帧间预测（inter prediction）、转换（transform）、量化（quantization）、去区块滤波器（deblocking filter）、熵编码（entropy coding）等模块，但在HEVC编码架构中，整体被分为了三个基本单位，分别是编码单位（coding unit, CU）、预测单位（predict unit, PU）和转换单位（transform unit, TU）。

## H.264

H.264/MPEG-4第10部分，或称AVC（Advanced Video Coding，高级视频编码），是一种视频压缩标准，一种被广泛使用的高精度视频的录制、压缩和发布格式。第一版标准的最终草案于2003年5月完成。H.264/MPEG-4 AVC是一种面向块的基于运动补偿的编解码器标准。由ITU-T视频编码专家组与ISO/IEC联合工作组——即动态图像专家组（MPEG）——联合组成的联合视频组（JVT，Joint Video Team）开发。因ITU-T H.264标准和 ISO/IEC MPEG-4 AVC标准（正式名称是ISO/IEC 14496-10 — MPEG-4第十部分，高级视频编码）有相同的技术内容，故被共同管理。H.264因其是蓝光盘的一种编解码标准而著名，所有蓝光盘(blue-ray)播放器都必须能解码H.264。它也被广泛用于网络流媒体数据如Vimeo、YouTube、以及Apple的iTunes Store，网络软件如Adobe Flash Player和Microsoft Silverlight，以及各种高清晰度电视陆地广播（ATSC，ISDB-T，DVB-T或DVB-T2），线缆（DVB-C）以及卫星（DVB-S和DVB-S2）。

H.264可以低于1Mbps的速度实现标清（分辨率在1280P*720以下）数字图像传送；

## H.264/MPEG-4 AVC SVC

可伸缩视频编码（Scalable Video Coding, SVC）是传统H.264/MPEG-4 AVC编码的改进，可提升更大的编码弹性，并具有时间可伸缩（Temporal Scalability）、空间可伸缩（Spatial Scalability）及信噪比可伸缩（SNR Scalability）三大特性，使视频传输更能适应在异质的网络带宽。SVC的目标在于标准化已使编码的高品质的视频码流，其中包含一个或多个子位流（subset bitstream）进行解码，可以自己用一个复杂和重建质量达到类似的利用现有的H.264/MPEG- 4 AVC的设计与相同数量的数据码流中的一个子集。

## VP8

VP8 是一个开放的图像压缩格式，最早由 On2 Technologiesis 开发，随后由 Google 发布。同时 Google 也发布了 VP8编码的实做库：libvpx，以BSD授权条款的方式发布，随后也附加了专利使用权。而在经过一些争论之后，最终 VP8 的授权确认为一个开放源代码授权。VP8编码的开发从2008年9月13日开始，目的是要取代旧有的 VP7 编码格式。Google 在2010年收购了 On2 之后，各界便呼吁 Google发布 VP8的源代码，在2010年3月12日，自由软件基金会发表了一个公开信，希望 Google 能够逐渐的以 HTML5 和开放的 VP8，取代 Youtube 目前使用的 Adobe Flash Player 和 H.264。
2010年5月19日，Google在 Google I/O年会上，以BSD授权条款的发布了 VP8 编码软件，VP8的比特流格式则是以不可撤回的免费专利使用权发布。VP8也成为第二个 On2 Technologies以开放源代码方式发布的编码产品，前一个是捐赠给Xiph.Org基金会 的VP3，随后成为了图像编码格式 Theora。
编码
目前 VP8只能通过 libvpx来进行编码，而 Google聘用了 FFmpeg 的开发者 Ronald Bultje 来开发基于 x264 架构的 VP8 编码器，称为 xvp8，将来发布后会集成在 x264中。而芬兰的 WebM硬件开发团队则是发布了暂存器转换层次结构（Register transfer level）的 VP8硬件编码器，提供给半导体制造商免费使用。
解码
libvpx可以解码 VP8的图像，在2010年7月23日，FFmpeg 的开发者Jason Garrett-Glaser、Ronald Bultje和 David Conrad发布了名为 ffvp8的 VP8解码器，测试结果显示 ffvp8比 Google自己的 libvpx解码器性能更佳。另外 WebM专案的硬件团队也有发布暂存器转换层次结构（Register transfer level）的硬件解码器，同样是免费使用。

## VP8和H.264的比较

H.264是目前使用最多的网络图像编码格式，因此最常拿来和 VP8做比较。

H.264 的编码技术包含专利（由 MPEG-LA 提供授权），而且在硬件上使用需要取得授权，VP8则不需要。即使有Google的背书，但VP8仍然很难避过所有的专利，其下场可能跟VC-1如出一辙。管理H.264专利池的MPEG LA声称有12家公司持有Google VP8的专利。美国MPEG LA表示："创建VP8专利池的相关准备正在进行"。

根据 MSU Graphics & Media Lab在2011年5月的测试，VP8需要约213%的数据量，才能达到和 H.264相同的图像品质。

x264 的开发者之一：Jason Garrett-Glaser，给了一些针对 VP8的评论，他认为 VP8目前并没有实现真正的比特流规范，而且在一些编码的技术上有所欠缺。

VP8的subblock预测和H.264的4×4模式一致，但VP8不支持 H.264 High profile的8×8模式，会影响对细节的保持。VP8缺少 B frame是另一个大问题。H.264已有大量的硬件支持，但VP8仍需要依靠软件解码。VP8的标准文档过于简陋可能是最让人诟病的问题，大部分是直接贴C language code，而不是文字表述，许多细节没有交待清楚。

## VP9

VP9 是Google提供的开源的免费视频codec，是VP8的后续版本，初始开发时命名为下一代开源视频或者VP-NEXT. VP9的开发始于2011年Q3，试图降低VP8的50%的码率而保持相同的质量，另外希望VP9比H.265（ High Efficiency Video Coding）有更好的编码效率。 2012年底，VP9的解码器被加入Chrome浏览器，2013年2月发布正式版本的chrome浏览器。VP9支持超宏块大小到32x32，也采用了四叉树的宏块分解结构。


## H.265和VP9比较

目前下一代主流的视频编码标准有 ITU-T VCEG 推出来的 H.265 和 Google 推出 VP9 。
H.265 在 H.264 的基础上保留其中的部分技术，并对相关技术加以改进研发而成。新技术主要通过提升压缩效率、鲁棒性，提高错误恢复能力，减少实时时延、减少信道获取时间等方面，让视频编码达到效率更高。同时 H.265 可以实现利用 1~2Mbps 传输速度传送 720P 普通高清音视频。
VP9 是由 Google 开发的开放式、无版权费的视频编码标准，在开发初期曾经被命名为 Next Gen Open Video，VP9 也被视为是 VP8 的下一代视频编码标准。
H.265、VP9 与上一代视频编码标准相比在编码效率上均提升了 50% 左右。那么它们两者之间孰优孰劣呢？下文对两者的性能做下详细的对比，通过数据，我们来了解哪个才是下一代视频编码标准的王道。

### H.265、VP9 性能对比

**编码质量：**

 ![图片: ](http://images-cdn.shimo.im/buhamWQpEDEqhznG/1.jpg)

上图为 H.265 与 VP9 编码质量的对比测试，数值越小，则表示编码质量越好。从对比中我们发现 H.265、VP9 两者的差别并不大，整体平均分只差了 0.001，在实际应用中几乎不存在差异。

**编码时间:**

![图片: ](http://images-cdn.shimo.im/fh6wTtzWTY8RPDy9/2.jpg)

在编码时间对比中，VP9 完胜 H.265，无论是 4K 视频还是 1920、1280 分辨率的视频，VP9 的编码耗时都比 H.265 短很多。

**CPU 消耗：**

![图片: ](http://images-cdn.shimo.im/F4QUiL3ak8ULsHaL/3.jpg)

上图是 H.265 和 VP9 在 Dell Precision 390 工作站上播放 CPU 消耗测试，VP9 在 Firefox 上 CPU 解码效率比 Chrome 更高效。而 H.265 在 DivX 上远远比 VLC Player 高效。将两个编码标准的数据进行对比之后，H.265 的解码效率略高于 VP9 。

### 样例

不论是 H.265 还是 VP9，都有着其优势领域，用户可以根据实际的应用场景选择使用的格式。
目前，又拍云的媒体处理已同时支持 H.265 和 VP9 视频编码标准。客户在进行音视频处理时，只需要把视频编码格式设置成 libx265 或 libvpx-vp9，即可实现视频编码成 H.265 或 VP9。

![图片: ](http://images-cdn.shimo.im/PNQd02RwrnYWITEM/4.png)


## 参考资料

http://en.wikipedia.org/wiki/High_Efficiency_Video_Coding
http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC
http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC_products_and_implementations
http://en.wikipedia.org/wiki/Scalable_Video_Coding
http://en.wikipedia.org/wiki/VP8
http://en.wikipedia.org/wiki/VP9
