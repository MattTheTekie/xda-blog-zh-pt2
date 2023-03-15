# 谷歌澄清 Play 商店 30%的费用，Android 12 上 3P 商店的变化

> 原文：<https://www.xda-developers.com/google-play-store-in-app-billing-clarity-android-12-third-party-app-stores/>

**更新 1(****2020 年 10 月 05 日****@****01:59AM****ET):**谷歌将在印度实施 Play 计费的截止日期延长至 2022 年 3 月 31 日。滚动到底部了解更多信息。下面保留了 2020 年 9 月 28 日发表的文章。

上周，我们了解到[谷歌正准备用新的语言更新其 Play Store 指南](https://www.xda-developers.com/google-double-down-30-in-app-fee/),阐明围绕应用内购买使用 Google Play 应用内计费服务的要求。该报告暗示，谷歌希望打击不使用谷歌支付服务而提供应用内支付的应用，这是谷歌从 Play Store 购买中获得 30%收入的方式。今天，谷歌正式做出了这些改变。

## 明确 Google Play 应用内计费的使用

在今天之前，谷歌要求 Play Store 上所有销售完全在应用内消费的数字商品(如手机游戏中的皮肤)的应用使用 [Google Play 的计费系统](https://developer.android.com/google/play/billing)。这是 Google Play 的长期政策，但该公司表示，他们“听到的反馈是，关于哪些类型的交易需要使用 Google Play 的计费系统，他们的政策语言可以更加明确。”因此，该公司已经更新了其[支付政策](https://support.google.com/googleplay/android-developer/answer/9858738)页面上的语言，更加明确地要求所有数字商品通过 Google Play 的计费系统销售。(值得一提的是，我使用 Wayback 机器对旧的支付政策页面和更新后的页面进行了比较，看起来确实是只更新了语言，而没有更新实际的政策。)

谷歌表示，“在过去 12 个月里，使用 Play 应用的开发者中，只有不到 3%销售了数字产品”，而且“在这 3%中，绝大多数(近 97%)已经使用了 Google Play 的付费服务。”不过，将这些数字放在上下文中很重要。Play Store 上有[近 300 万个 app](https://www.statista.com/statistics/266210/number-of-available-applications-in-the-google-play-store/)；这些应用程序中的绝大多数都是免费的，因此不需要 Google Play 的计费系统。无论如何，对于那些将受到这一变化影响的*现有的*应用程序，谷歌将在 2021 年 9 月 30 日之前实施他们的计费系统。然而，任何在 2021 年 1 月 20 日之后提交到 Play Store 的*新*应用都需要符合更新后的指南。最后，对于那些从提供实物商品过渡到数字商品的应用程序(因为来自新冠肺炎疫情的挑战)，谷歌表示，在未来 12 个月，“这些企业将不需要遵守(他们的)支付政策”。

谷歌 Play Store 指南的其他方面没有变化。例如，开发者仍然不允许在应用程序本身内告知客户更好的价格、优惠和其他支付方式。然而，他们*被允许通过其他渠道直接与客户沟通，比如通过电子邮件。此外，谷歌表示，他们的政策“同样适用于 Google Play 上发布的所有应用”，包括他们自己的应用，他们的算法“使用与谷歌自己的应用相同的标准对第三方应用和游戏进行排名。”当然，谷歌对其专有的搜索和排名算法并不透明，因此这些声明很可能是为了回应媒体和监管机构加强的审查。*

## 在 Android 12 上使用第三方应用更加容易

当 Epic Games 对谷歌(和苹果)提起诉讼时，该公司质疑他们认为谷歌采用的恐吓策略，以降低人们使用第三方应用商店的意愿。例如，Epic 抱怨说，用户必须授予的权限包含劝阻性语言，并且无法静默安装和更新应用程序使第三方应用程序商店处于固有的劣势。最后，Epic 还声称谷歌竭力阻止 Epic 游戏商店预装在一加和 LG 的手机上。

在今天的博客文章中，谷歌重申，消费者一直可以选择从多个应用商店获得应用，但每个应用商店“能够决定自己的商业模式和消费者特征。”作为一个例子，谷歌直接引用了堡垒之夜仍然适用于下载 Epic 游戏商店或访问三星 Galaxy 应用商店的安卓用户。然而，该公司将“在 [Android 12](https://www.xda-developers.com/android-12/) 中做出改变”...让人们更容易在他们的设备上使用其他应用商店，同时注意不要损害 Android 已经到位的安全措施。”谷歌还没有透露他们对 Android 做了哪些改变，但我们猜测这将涉及一系列新的权限和 API。

## 关于 Google Play 计费的常见问题

除了详细介绍更新后的政策语言的主要博客帖子外，谷歌还发布了一个关于使用 Google Play 计费的常见问题。以下是谷歌准备的问答:

### Google Play 账单常见问题

*   问:我可以通过其他 Android 应用商店或我的网站分发我的应用吗？
    *   答:是的，你可以随心所欲地发布你的应用程序！作为一个开放的生态系统，大多数 Android 设备预装了不止一个商店，用户可以安装其他商店。Android 为开发人员提供了通过其他 Android 应用商店、直接通过网站或设备预加载分发应用的自由和灵活性，而无需使用 Google Play 的计费系统。
*   问:哪些应用需要使用 Google Play 的计费系统？
    *   答:Google Play 上发布的所有提供应用内购买数字商品的应用都需要使用 Google Play 的计费系统。我们的支付政策一直要求这样做。在过去的 12 个月里，只有不到 3%的使用 Play 应用程序的开发者销售了数字产品，而在这 3%中，绝大多数(近 97%)已经使用了 Google Play 的计费功能。对于那些需要更新应用程序的少数开发者来说，他们将在 2021 年 9 月 30 日之前做出这些改变。2021 年 1 月 20 日之后提交的新应用需要合规。
*   问:许多企业需要将以前的实体服务转移到网上(例如数字直播活动)。这些应用需要使用 Google Play 的计费吗？
    *   答:我们认识到，全球疫情导致许多企业不得不应对挑战，将实体业务转移到数字领域，并以新的方式吸引受众客户，例如，将面对面的体验和课程转移到网上。在接下来的 12 个月中，这些企业不需要遵守我们的支付政策，我们将在下一年继续重新评估情况。对于正在经历这些变化的开发人员，我们渴望听到您的意见并与您合作，帮助您接触新用户并发展您的在线业务，同时实现一致且安全的在线用户体验。
*   问:谷歌的应用程序也必须遵循这项政策吗？
    *   答:是的。Google Play 的开发者政策适用于 Play 上的所有应用，包括谷歌自己的应用，这些政策包括应用程序使用 Google Play 的计费系统购买数字产品的要求。
*   问:我可以和我的用户交流其他支付方式吗？
    *   答:是的。在你的应用之外，你可以自由地与他们交流其他购买选择。你可以使用电子邮件营销和应用程序之外的其他渠道来提供订阅优惠甚至特价。
*   问:我可以与我的用户就其他平台的促销活动进行沟通吗？
    *   答:当然可以。我们也是应用开发者，我们知道不限制你与用户交流的能力有多重要。您可以向他们发送电子邮件，或者在应用程序之外交流您的产品信息，即使它们在 Google Play 上与在其他地方不同。
*   问:我可以根据平台拥有不同的应用功能、价格和体验吗？
    *   答:是的。这是你的服务和业务，由你决定。我们不需要跨平台的奇偶校验。您可以创建不同版本的应用程序，以支持不同的平台、功能和定价模式。
*   问:我能在 Play 上提供一个只消费(阅读器)的应用吗？
    *   答:是的。Google Play 允许任何应用程序只能消费，即使它是付费服务的一部分。例如，当应用程序打开时，用户可以登录，用户可以在其他地方访问付费内容。
*   问:你的计费政策会根据我的应用的类别而改变吗？
    *   答:不会。商业或消费应用，以及音乐或电子邮件等垂直领域在 Google Play 上都是一样的。
*   问:我可以直接向顾客退款吗？
    *   答:是的。我们理解维护与客户关系的重要性。您可以继续直接向您的客户和其他客户支持人员退款。
*   问:Google Play 会允许云游戏应用吗？
    *   答:是的。Google Play 欢迎任何开发者提供的符合 Play 政策的云游戏流媒体应用。

* * *

## 更新:谷歌将印度的播放计费截止日期推迟至 2022 年 3 月 31 日

谷歌曾提到在现有应用中实施 Google Play 计费的最后期限是 2021 年 9 月 30 日。鉴于最近收到的来自印度开发者的反馈，谷歌将印度的截止日期延长至 2022 年 3 月 31 日。这也应该给那些为订阅付费选项(将在 Google Play 上提供)实现特定于印度的 UPI 的开发者足够的时间来实现。

正如《经济时报》报道的那样，谷歌表示，在政策生效前给予较长时间的想法是为了确保企业不会受到过度的压力。然而，谷歌还没有讨论改变其全球商业模式本身。这些声明、澄清和延期是在谷歌因其在应用商店的主导地位而受到批评的情况下做出的，印度 50 多名科技企业家联手向印度政府请愿，要求支持创建一个支配性的印度数字应用生态系统作为反制措施。