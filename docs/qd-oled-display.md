# 什么是 QD-有机发光二极管法案？看看下一代电视和显示器技术

> 原文：<https://www.xda-developers.com/qd-oled-display/>

当谈到纯粹的画质时，没有什么比得上安装在灯光昏暗的陈列室中的 OLED 电视的脆深黑色。“光线昏暗”这个描述很重要，因为在客厅里把它拿出来，有机发光二极管的恒星对比度会被反射淹没。在这些条件下，有机发光二极管可以说是胜过竞争的显示器类型变得更亮。也就是说，有机发光二极管电视并不是在所有方面都绝对优越——这项技术有它的缺点，而且它在不断迭代以克服它的缺点。

席卷 CES 2022 的下一件大事是三星显示所说的*QD-有机发光二极管*，或者量子点有机发光二极管。显示器公司声称，使用这种技术的新电视将比传统的有机发光二极管电视更亮、更多彩、视角更好。另一个令人兴奋的进展是，这项技术不仅仅局限于电视，它还将向个人电脑显示器发展——这是第一个为*实际*桌子设计的消费级 OLEDs。

这种有机发光二极管的新变体在显示堆栈中添加了一个量子点层，这种技术以前只在 LCD 面板上使用(通过 QLED)。这些量子点的目的是在不使用相同颜色的有机高纯度光源的情况下产生高度饱和的子像素，这通常是昂贵或低效的。另一种方法是使用彩色滤光片，这是有机发光二极管电视一直使用到现在。

 <picture>![Sony A95K QD-OLED TV](img/eabd072c4e156838806e8a91c4bf165f.png)</picture> 

Image: Sony

## QD-有机发光二极管和老有机发光二极管有什么不同？

为了解释这一点，我们首先必须了解以前的有机发光二极管电视是如何构成的。有机发光二极管是一个总括术语，可以包含各种技术子集。但是当营销部门用“有机发光二极管”这个词来形容电视时，他们通常指的是 W-有机发光二极管。

过去 10 年，LG Display 一直垄断着用于有机发光二极管电视机的面板。这些面板都是使用 RGBW 像素结构的 W-有机发光二极管显示器，这意味着每个像素由四种不同颜色的子像素组成:红色、绿色、蓝色和白色。然而，在其核心，每个子像素实际上是一个白色子像素(因此称为 W-有机发光二极管)，彩色子像素是通过滤色器实现的，滤色器阻挡了部分白光光谱，产生红色、绿色或蓝色。因为对于三种颜色的子像素，光从光源中被减去，所以这种像素结构不是最有效的，这就是为什么需要额外的白色子像素的原因。第四个白色子像素没有任何滤色器，其目的是提高效率和亮度。

而量子点则是*将*一个光源从一种颜色转换成另一种颜色，在这种转换中几乎没有浪费一点原始光源。QD-有机发光二极管不是从每个子像素的宽白色光谱开始，然后用彩色滤光片剥离部分光谱，而是从一个简单的蓝色光源开始，将其转换为高纯度的红色和绿色子像素，同时保持蓝色子像素不变。

 <picture>![](img/eaad2200017fa2987ef99f5bf2617c7e.png)</picture> 

*Top:* Breakdown of QD layers (source: Samsung Display). *Bottom:* Light spectrum of QD-LCD vs W-OLED when displaying white. Quantum dots allow for narrower light spectra, which produces higher color saturation. The green and red peaks are derived from passing high-energy blue light through a quantum dot layer, and each peak is associated with its own colored subpixel.

利用这种有效的方法，不需要第四个白色子像素，并且 QD-有机发光二极管可以利用正常的 RGB 像素结构。当前 W-有机发光二极管电视的缺点之一是，当显示器接近其峰值亮度时，依赖额外的白色子像素来获得额外的亮度会降低最大色彩饱和度；由于滤色器在高亮度下失效，颜色体积进一步减小。另一方面，QD-有机发光二极管可以保持完全饱和，直到显示器的最大白色水平。此外，如果没有第四个子像素，RGB 子像素可以做得更大以填充额外的空间，从而增加它们的光输出。

### 为什么要用蓝色光源？

在可见光光谱中，蓝光在红光、绿光和蓝光中波长最短；因此它具有最高的归一化能量。量子点层基本上可以将蓝光的较高能量限制在红光或绿光，但反过来是不可能的——你不能使用较低能量的红光或绿光来产生蓝光。

### 为什么不使用真正的红色、绿色和蓝色光源呢？为什么要经历这么多麻烦？

最大的原因是增加显示面板的寿命。当你花大价钱买一台电视时，你可能希望它能用很长时间。有机光源不可避免地会随着时间的推移而变暗，不同的材料会以不同的速度衰减。当使用光源的组合时，例如使用单独的红/绿/蓝发射器的有机发光二极管，发射器衰减的变化速率最终导致显示器的彩色再现漂移。例如，随着时间的推移，许多显示器将开始显示逐渐变黄的白色。有机发光二极管 W 酒店和 QD 有机发光二极管酒店的展示设计都是为了尽量减少这种影响。

如果我们深入研究现有的 W-OLED 面板，我们会发现白色子像素实际上是由多个光源组成的。最初，这些子像素由蓝色 led 和黄色磷光体组成，但 LG Display 继续使用红色、绿色和蓝色发射器的组合来创建白色子像素。这些不同的发射体按比例混合和调整大小，以确保它们都以接近恒定的速率衰减，从而使颜色随时间推移的变化最小。

### 有机发光二极管老化呢？

对于 QD-有机发光二极管，所有的子像素都由同一个蓝色光源支持，因此颜色偏移应该几乎不存在。然而，与红色和绿色材料相比，蓝色有机材料的寿命通常较短，因此在 time✝.上方，QD-OLED 中的子像素实际上可能比 W-OLED 更快变暗这也可能意味着 QD-有机发光二极管更容易老化，当显示器的部件明显比周围老化更多(或更少)时，就会发生老化。当然，我们只能等着看这是否会成为一个问题。

*✝这里的一个细微差别是 QD-OLED 的 RGB 子像素可以做得比 W-OLED 的 RGBW 结构更大。较大的子像素区域延长了发射器的寿命。*

另一个基本的有机发光二极管设计是智能手机显示屏中最常见的 PenTile 子像素矩阵。原则上，它的工作原理类似于 W-有机发光二极管包装白色子像素的方式:用不同数量和大小的红色、绿色和蓝色发射器组合，以便它们更均匀地衰减。更具体地说，PenTile 设计更丰富，具有较小的绿色子像素，因为它们是最有效的，而蓝色子像素被制作得更大，以延长它们较短的寿命。

## 那么，QD-有机发光二极管比 W-有机发光二极管更好吗？

既然我们已经讨论了一些基础知识，我们可以挑战一个显而易见的问题:

QD-有机发光二极管会比我们现有的 W-OLEDs 更好吗？

答案是...**极有可能！**不仅仅是重复三星显示发布的营销材料，我们发现 QD-有机发光二极管在光效方面明显优于 W-有机发光二极管，其支持的标准像素结构允许 HDR 和高亮度用户使用更高的色彩量。与使用彩色滤光片相比，量子点的精度还允许更饱和的颜色，从而提高 Rec.2020 色域的覆盖率。

此外，QD-有机发光二极管省略了偏振层，偏振层通常用于减少反射，代价是阻挡显示器自身的一些光。三星显示告诉我们，其 QD-有机发光二极管的面板结构在处理反射方面具有内在优势，因此它有信心可以去除偏振器，这应该会产生一些额外的显示亮度。

三星显示还告诉我们，他们的量子点转换可以全方位发光，从而在某个角度观看电视时降低亮度损失。现有的 W-有机发光二极管面板已经具有令人惊讶的统一视角，但显示器公司正在宣传其 QD-有机发光二极管性能更好

## 好吧，我想要一个。我现在可以买什么样的 QD-有机发光二极管展览？

目前，只有三星、索尼和外星人能展示这项新技术。在 CES 2022 上，索尼发布了其 [Bravia XR A95K](https://www.xda-developers.com/sony-2022-bravia-xr-tv-mini-led-tv-qd-oled-tv/) ，这是一款 4K QD OLED 电视，最初将在 2022 年底推出 55 英寸和 65 英寸尺寸。对于电脑游戏玩家来说，外星人推出了首款消费级有机发光二极管游戏显示器——我指的不是伪装成显示器的电视。这款 34 英寸的超宽显示屏是一个期待已久的展示，最终将有机发光二极管技术以一个流行、实用的尺寸带到了 PC 世界。这两种屏幕都将使用三星显示提供的 QD-有机发光二极管，这应该会让 LG Display 的资金有所增加。

 <picture>![Alienware 34-inch QD-OLED Ultrawide Gaming Monitor](img/8587765ec98a3ba497b2b29a3f962b36.png)</picture> 

Image: Dell

最重要的是，引领这项新技术的三星显示将该公司引入有机发光二极管市场，成为 LG Display 的主要竞争对手。最初，QD-有机发光二极管不会便宜——这些新的显示器可能会比 W-有机发光二极管贵得多。但希望在技术开始成熟后，我们应该会看到这种竞争推动有机发光二极管价格全面下降。我们还可能看到 QD-有机发光二极管在未来变得比 W-有机发光二极管更便宜，因为它只依赖蓝色有机材料，而不是 LG Display 为其 W-有机发光二极管采购的无数材料。

展望未来，有机发光二极管的下一个自然发展是完全去除有机材料，给我们留下一个不同类型的 LED 显示屏。有机发光二极管受到蓝色有机材料有效性的严重限制，因此合成一种替代光源打开了新一代屏幕的大门。在可见地平线之外，三星显示一直在研究另一种叫做 QNED 的显示技术，它代表量子纳米发光二极管。这种设计类似于 QD-有机发光二极管，但 QNED 没有使用有机蓝色材料，而是使用氮化镓纳米棒 LED 作为光源，同时仍然使用量子点来塑造它。一旦有了结果，我们也会有一个解释者。