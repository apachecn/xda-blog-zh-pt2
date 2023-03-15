# Chrome 接收对 EAC-3(杜比数字增强版)直通的支持

> 原文：<https://www.xda-developers.com/chrome-eac-3-dolby-digital-plus/>

# Chrome 接收对 EAC-3(杜比数字增强版)直通的支持

Chrome 现在获得了对 EAC-3 或杜比数字增强版的支持。这将特别有利于 Android 电视用户，提供更高质量的音频。请继续阅读！

Chrome 将在即将到来的更新中获得对杜比数字加(也称为增强型 AC-3)直通的支持，这可以在 chrome Gerrit 上看到。对于那些使用安卓电视的人来说，这是一个巨大的增加，安卓电视的声音系统使用[杜比数字加](https://www.xda-developers.com/xda-external-link/google-play-movies-receives-dolby-digital-plus-support/)。Dolby Digital Plus 是一种先进的环绕声音频技术，已应用于许多家庭设备，包括家庭影院和汽车音响系统。

提交描述如下:

> 当连接的 HDMI 接收器支持(E)AC3 直通时，我们可以直接将原始压缩(E)AC3 比特流传输到 AudioTrack。

这一增加对音频爱好者有利，因为这意味着你不再需要依赖运行 Chrome 的设备来解码它。相反，您可以让您的首选音频系统完成所有需要的音频数据解码和渲染工作。这通常会提高音频质量，因为制造商会对设备进行优化，以在 Dolby Digital Plus 设备上获得最佳音频质量。这一升级对 Android 电视尤其重要，因为它们最有可能输出到条形音箱或其他支持这一功能的高保真设备。

原始音频部分是指处理前的音频。当系统处理音频时，有时它可能会在某些频率下应用均衡、压缩或响度增强。这些是为了提供“更好的音频体验”，但实际上可能会损害拥有可以自行解码和处理的高端系统的人的享受。向启用 EAC-3 的设备提供已经处理过的音频将会破坏这种设备的目的。例如，Dolby Digitial Plus 支持多达 5 个 640kbps 的音频通道，而 Android TV 如果从旧版本的 Chrome 播放，将在单个音频通道中向设备提供 320kbps，因为设备将进行处理并**然后**输出到声音系统。对于音频爱好者来说，这是一个巨大的增加，也意味着任何使用 Chrome 定制标签的东西都将得到同样的待遇。

* * *

[**来源:铬捷利**](https://chromium-review.googlesource.com/c/596720)