# 联发科提醒我们为什么高通骁龙在 XDA 更受欢迎

> 原文：<https://www.xda-developers.com/mediatek-source-code-release-no-plans/>

在选择新的智能手机时，大多数消费者会考虑价格、设计、摄像头和软件功能等方面。很少有用户真正关心他们的新智能手机采用什么样的片上系统，但对于 XDA 社区来说，这是一个非常重要的考虑因素。海思、三星电子、高通和联发科是智能手机芯片组最成功的硅供应商，尽管海思只为华为和 Honor 设备生产芯片组，而三星的 Exynos 芯片很少出现在三星 Galaxy 设备之外。另一方面，高通骁龙和联发科芯片出现在一系列设备中，从最低端的 Android Go 设备到最高端的游戏手机。对于对自己的设备感兴趣的 XDA 用户来说，使用骁龙芯片是显而易见的。原因？高通比联发科对开发者更友好，而且这看起来不会很快改变。

我们的大多数读者可能都知道 Android 开源项目(AOSP ),所有 Android 软件都是从这个项目中派生出来的。我们的读者也知道这样一个事实，Android 设备附带了一个修改过的 Linux 内核。就像设备制造商(OEM)一样，芯片组供应商必须根据请求提供他们产品上提供的任何 Linux 内核二进制文件的内核源代码。然而，芯片组供应商不需要提供他们开发的其他软件(如 HALs 或框架分支)的源代码。当开发一款新的智能手机时，原始设备制造商通常不会从 AOSP 开始。相反，他们依靠芯片供应商来使 AOSP 与他们的芯片组兼容，然后将所有这些代码作为主板支持包(BSP)的一部分分发给原始设备制造商。原始设备制造商可以获得他们需要的代码，在他们的设备上启动一个工作的 Android 版本，然后他们可以定制这些代码以满足客户的需求。但是我们论坛上的独立定制 AOSP ROM 开发人员没有这种级别的访问权限，所以他们必须从零开始，尝试将纯 AOSP 与从设备中提取的预编译二进制文件拼凑在一起——没有任何文档帮助。幸运的是，与联发科不同，高通通过 CodeAurora Forums(CAF)让开发者的生活稍微轻松了一些。

CAF 是高通上传其芯片组[的内核源代码的地方，如骁龙 845](https://www.xda-developers.com/qualcomm-snapdragon-845-kernel-source-code/) 以及其芯片组特定代码的[部分](https://source.codeaurora.org/quic/la/)，这使得开发者在不知道底层芯片组功能如何工作的情况下更容易为平台构建。CAF 是高通为社区提供的一项服务，开发者很欣赏这项服务，因为它使 AOSP ROM 开发对他们来说变得更加容易。然而，CAF 的存在并不能解决开发者的所有问题，因为 OEM 仍然可以添加 CAF 版本不支持的非标准硬件——在这种情况下，开发者不得不求助于[肮脏的手段](https://www.xda-developers.com/cameras-custom-roms-developers-make-hardware-work-without-source-code/)。不幸的是，联发科芯片组没有 CAF 等价物，这导致了定制 ROM 社区的巨大差异，正如在[联发科](https://forum.xda-developers.com/redmi-note-3/xiaomi-redmi-note-3-mediatek-roms-kernels-recoveries--other-development)与[骁龙](https://forum.xda-developers.com/redmi-note-3/development)红米 Note 3 论坛中看到的那样。

当被问及发布其产品源代码的可能性时，联发科移动业务部门总经理 TL Lee 告诉 [*AndroidAuthority*](https://www.androidauthority.com/mediatek-updates-source-code-924160/) ，该公司没有“在近期”向公众发布源代码的计划。“到目前为止，我们还没有那种程序。我们只是向客户发布我们的源代码，”李开复告诉*安卓权威*。联发科告诉 AndroidAuthority ，该公司仍在努力改进他们的 [GMS Express](https://www.xda-developers.com/google-mediatek-announce-gms-express/) 项目，这有助于加快新设备的认证过程。虽然这给了原始设备制造商更多的时间在他们的设备上开发软件，但它对定制 ROM 社区没有帮助，一些用户依赖定制 ROM 社区来提供远远超出设备制造商所提供的软件支持。如果你计划使用定制的 rom 来保持你的设备在寿命结束后相对最新，那么在可预见的未来坚持使用高通骁龙设备。