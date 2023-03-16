# 谷歌宣布网络生命倡议，为网站性能提供统一的指导

> 原文：<https://www.xda-developers.com/google-announces-web-vitals-initiative/>

在去年的 Chrome 开发者峰会上，谷歌[宣布了新的 Chrome 开发者工具](https://www.xda-developers.com/google-announces-chrome-developer-tools-reduce-page-loads-native-app-experiences/)，以减少页面加载时间并构建类似原生应用的体验。当时，该公司还讨论了一项倡议，为开发者提供一套统一的衡量标准，在建立网站时考虑用户体验和性能。在最初想法的基础上，谷歌现在宣布了 Web Vitals 计划，旨在提供“质量信号的统一指导，这些信号对于在网络上提供良好的用户体验至关重要”。

多年来，Google 提供了一些工具来帮助网站开发者测量和报告网站性能。其中包括 Lighthouse、 [Chrome DevTools](https://www.xda-developers.com/tag/google-chrome-dev/) 、PageSpeed Insights 和搜索控制台的速度报告。但谷歌指出，虽然一些开发人员非常擅长使用这些工具，但其他人发现各种工具和指标有点难以跟上。通过新的举措，该公司旨在简化景观，以便开发人员可以专注于最重要的指标，即核心网站活力。

核心网站生命体征是适用于所有网页的所有网站生命体征的子集，应该由所有网站所有者来衡量，并将在所有谷歌工具中出现。目前，这些核心 Web 要素关注用户体验的三个方面——加载、交互性和视觉稳定性——并包括以下指标(及其各自的阈值):

*   **最大含量油漆(LCP):** 测量装载性能。为了提供良好的用户体验，LCP 应该在页面首次开始加载后的 2.5 秒内发生。
*   **第一输入延迟(FID):** 测量交互性。为了提供良好的用户体验，页面的 FID 应该小于 100 毫秒。
*   **累积布局偏移(CLS):** 测量视觉稳定性。为了提供良好的用户体验，页面应该保持小于 0.1 的 CLS

为了帮助开发者测量和报告这些核心的网络要素，谷歌致力于在其工具中展现这些指标。下面的图表详细说明了哪些工具支持核心网络要素:

开发人员还将能够使用标准 web APIs 用 JavaScript 测量每个核心 web 生命，并使用 [Web Vitals Chrome 扩展](https://github.com/GoogleChrome/web-vitals-extension)报告每个核心 Web 生命，而无需编写任何代码。该扩展利用 web-vitals 库来测量这些指标，并在用户浏览 web 时向他们显示。这个扩展也有助于理解你的网站、你的竞争对手的网站以及整个网络的表现。或者，希望使用底层 web APIs 来度量这些指标的开发人员可以参考下面链接的网站上的指标指南，以了解实现细节。

除了核心网络指标，谷歌还谈到了其他网络指标，这些指标将作为核心指标的代理或补充指标。这些指标包括第一字节时间(TTFB)、第一次内容丰富的绘制(FCP)、总阻塞时间(TBT)和交互时间(TTI)，这些指标可以帮助开发人员获取更大部分的体验或帮助诊断特定问题。

值得注意的是，这些网站生命和核心网站生命将随着时间的推移而演变，开发者应该期待未来的改进或补充。然而，由于核心 Web 生命指标与所有网页相关，并且在几个 Google 工具中有所体现，因此对这些指标的任何更改都不会改变它们的定义和阈值。对于任何即将到来的变化和可预测的年度模式，开发人员也将得到事先通知。由于其他 Web 生命周期是特定于上下文或工具的，它们的定义和阈值可能会在不事先通知的情况下频繁更改。对所有网络重要信息所做的任何更改都将记录在此[公共变更日志](http://bit.ly/chrome-speed-metrics-changelog)中。

* * *

**来源:[web . dev](https://web.dev/vitals/)**