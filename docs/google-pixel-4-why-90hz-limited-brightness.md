# 为什么谷歌将 Pixel 4 的 90Hz 限制在高亮度

> 原文：<https://www.xda-developers.com/google-pixel-4-why-90hz-limited-brightness/>

就在最近，一位[敏锐的 Reddit 用户](https://www.reddit.com/r/GooglePixel/comments/dlt375/does_it_look_like_smooth_display_is_turning_off/)发现，[谷歌 Pixel 4 上的 90Hz *【平滑显示】*仅在高亮度水平期间保持在 90Hz。](https://www.xda-developers.com/google-pixel-4-90hz-display-only-works-at-high-brightnesses/)许多早期 Pixel 4 采用者能够注意到显示器似乎并不经常坚持 90Hz，这种系统行为似乎就是原因。自然，一些用户对此事感到愤怒，一些用户好奇为什么谷歌会以这种奇怪的方式实现他们产品的最大功能之一。许多人认为原因与电池寿命有关，但这真的没有任何意义——当电池消耗是一个更大的问题时，为什么 90Hz 会被限制在更高的亮度？在 Pixel 4 发布之际，XDA 的主编米沙·拉赫曼发现了一个解释谷歌支持这一行为的官方原因的承诺:

谷歌表示，他们将 90Hz 限制在 Pixel 4 的更高亮度的原因是，随着刷新率的变化，屏幕可能会出现闪烁，特别是当显示器亮度和环境亮度较低时。这是因为显示器不支持真正的动态/自适应刷新率，不同的刷新率需要不同的显示器伽马曲线(校准)。不同的伽马曲线很难完美匹配，因此在两种刷新率之间切换时可能会注意到差异。

谷歌的*平滑显示*系统在屏幕空闲或显示 60fps 或更低的动画/视频时将显示屏保持在 60Hz，只要你触摸显示屏或屏幕上的动画(如通知)出现，就会立即切换回 90Hz，因此它经常在 90Hz 和 60Hz 之间切换——每次切换时轻微的闪烁可能确实会变得令人讨厌。此外，谷歌表示，在较暗的观看环境中，我们对闪烁更敏感。这是因为对于较暗的阴影，校准的差异更明显，在较暗的观看环境下更明显。

谷歌向《The Verge》发布了一份声明，称该公司“不断评估这些参数是否会带来最佳的整体用户体验”，他们“之前计划在未来几周推出更新，包括在更高亮度的条件下启用 90hz。”目前，用户可以通过在开发者选项中启用该设置来一直强制 90Hz。强制 90Hz 使显示保持在 90Hz，所以没有屏幕闪烁，因为它不会从 60Hz 切换。然而，这会对手机电池造成损害。希望谷歌可以改进调谐，也许可以提供一个选项来完全禁用亮度调节，这样我们仍然可以享受一些电池节省，尽管潜在的屏幕闪烁。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)