# Micromax 在设备上远程安装不需要的应用程序

> 原文：<https://www.xda-developers.com/micromax-remotely-installing-unwanted-apps-on-devices/>

在最近的过去，我们目睹了相当多的原始设备制造商为了实现各种目标(如提高基准测试结果)而篡改设备的行为。我们还听说制造商和运营商在他们的设备中添加了跟踪软件，以收集有关设备性能的数据、有关设备和无线电发射塔之间语音和数据连接的统计数据，甚至是电池运行时间数据( [CarrierIQ 你在听吗？](http://www.xda-developers.com/the-rootkit-of-all-evil-ciq/))。然而，今天[传来](http://www.reddit.com/r/india/comments/2s4aak/micromax_is_highjacking_my_phone_installing_apps/)报道称，印度手机制造商 Micromax 的某些设备的用户注意到应用程序在未经他们同意或许可的情况下被悄悄安装。

似乎即使卸载这些应用程序也无济于事，因为不久之后，它们就会再次出现。显然，这在很多层面上都是错误的，但我还是想在这里指出几个关键问题:

*   无法控制哪些应用程序安装在您的设备上会带来巨大的安全风险，因为您无法检查应用程序的权限，也不知道这些应用程序是否确实是原始应用程序(或者可能被恶意修改)
*   Micromax 设备往往不是你能找到的最高端设备，所以存储空间仍然被认为是一种奢侈品(总共 4GB)，让设备的存储空间充满随机应用程序肯定不是对宝贵空间的最佳利用
*   当使用移动网络时，下载也会发生，所以如果你的手机不断试图下载你甚至不想要的应用程序，你昂贵的全速数据将会显著减少

虽然这些做法本身听起来就非常错误，但不幸的是，事情并没有就此结束。除了下载应用程序，这些设备似乎还会不时在通知栏中显示广告。一名 reddit 用户报告说，一次显示 8-10 个广告，在查找这些令人不安的通知的负责应用程序时，他看到了一个名为“软件更新”的系统应用程序。

所以在这一点上，它听起来肯定像 Micromax 添加了定制软件，可以远程安装应用程序，并将广告推送到用户的设备上。但是如果我们停止假设事情，简单地告诉你有人在互联网上声称事情的故事，我们就不会在 XDA Developers 这里。因此，我们决定拆掉这个应用程序，看看里面有什么。

## **证据**

当开始拆除应用程序(在您的文件系统上实际上称为 FWUpgrade.apk)时，您注意到的第一件事是它是一个第三方应用程序。一家名为 Adups 的中国公司开发了它，作为谷歌 OTA 服务的替代品。显然，Micromax 决定用它而不是库存的。进一步分析需要克服的第一个障碍是字节码级混淆，大多数源代码读起来并不愉快。然而，如果你知道你在找什么，这个应用程序就不能隐藏它的本质。这里展示的证据以一小段代码开始，向您展示了这个应用程序的潜在能力，并以一些更有趣的东西结束。

让我们从静默安装的应用程序开始。要在另一个应用程序中完成这项工作，您要么需要直接使用 Android PackageManager API，要么从 shell 中发出安装命令。第二种情况在这里是真实的，如下面的代码所示(注意:这是简化的 java 代码，由于混淆，实际代码看起来有点不同):

*StringBuilder sb = new StringBuilder(" pm install-r ")；*sb . append(S2)；string cmd = sb . tostring()；

在这里，您可以看到一个新创建的 StringBuilder，它包含命令 *pm install* ，后跟 *s2* ，在本例中，它是一个字符串变量，包含下载的 apk 文件的文件系统路径。然后，完成的字符串被传递给一个新方法，执行如下操作:

*process builder process builder = new process builder(cmd)；process process = process builder . start()；*

在这里，您可以看到带有 shell 命令的字符串用于启动一个进程，该进程执行所述命令，并且实际上静默安装 apk 文件。在这一点上，我们可以相当肯定的是，Micromax ROMs 中的 OTA check 服务不仅可以下载和闪存系统 OTA，还可以静默安装应用程序。这本身并不意味着太多，因为它不一定是一件坏事，但还有更多。

在应用程序中，我找到了一些该公司网站的参考资料，其中一个[有一个广泛的功能列表](http://mg.adups.cn/adups/features_en.html)。我们看一下最有趣的部分好吗？

用公司自己的话说，就是这样。App 推送服务。设备数据挖掘。移动广告。这与 reddit 上的最初报道非常吻合，你不觉得吗？所以，这里的坏人实际上是 Micromax，因为这些是 Adups 的官方应用功能，Micromax 更有可能从强制应用安装和通知广告中获得收入。他们还选择了这家提供商，而不是将自己的服务器与谷歌的 OTA 服务一起使用，因此他们完全清楚这会对他们的用户产生什么影响。

## **临时解决方案**

那么既然我们知道这些不幸的报道是真的，那我们就来谈谈如何摆脱这种“功能性”。禁用上述功能的第一步是进入设备的应用程序设置，禁用无管理系统应用程序。然而，在这种情况下这是不可能的，因为 Android 允许 OEM 厂商禁用某些应用程序的禁用按钮。但是不要害怕，我们有现成的解决方案，会告诉你如何禁用恶意代码。

### **1。为您的设备建立根**

第一步也是最重要的一步是为您的设备建立根。一个根设备允许你做比你的普通手机更多的事情，并且是所有系统修改的关键一步。由于有相当多不同的 Micromax 设备，我不会在本文中链接到任何特定的 root 漏洞。相反，前往 [XDA:印度](http://forum.xda-developers.com/india)为你的设备搜索一个根漏洞或指南。请务必通读所有内容，并严格按照说明操作，以免在此过程中损坏您的设备。还要注意，这很可能会使您的保修失效。

### **2。建立亚行**

为了继续，您需要与您的设备建立有效的 ADB 连接。XDA 上有许多指南详细介绍了如何实现这一点，但对于初学者来说，[这里有一个相当最新的指南](http://forum.xda-developers.com/showthread.php?t=2141817)介绍如何下载必要的二进制文件以及如何建立与设备的连接。

### **3。禁用软件更新应用程序**

现在您已经获得了 root 访问权限，ADB 已经启动并运行，您可以继续禁用导致静默安装和不需要的广告的可怕应用程序。现在您需要做的就是启动一个命令提示符，确保该提示符位于 ADB 二进制文件的目录下，并执行以下命令:

*ADB shell pm disable com . adups . fota*

你可以在本[教程中了解更多关于使用 root 访问权限](http://forum.xda-developers.com/showthread.php?t=1151150)禁用应用程序的用法。请注意，此过程将删除您的设备搜索软件更新的功能，并可能在尝试打开设置中的手机更新部分时生成错误。如果您需要恢复应用程序(例如，当新的更新准备就绪时)，您可以使用以下命令轻松地再次启用它:

*ADB shell pm enable com . adups . fota*

## **总结会**

不幸的是，得知 Micromax 确实要对不想要的应用程序安装负责。我们希望上面关于禁用可疑应用程序的教程能让你在处理随机应用程序和广告时少一些头痛。显然，所有这些都不会阻止 Micromax 继续这些见不得人的做法，但也许你会考虑为你的下一次设备购买另一家 OEM。