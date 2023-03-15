# 使用 ZShaolin 将您的 Android 设备转换为强大的 Linux 机器

> 原文：<https://www.xda-developers.com/transform-your-android-device-into-a-powerful-linux-machine-with-zshaolin/>

众所周知，Android 是建立在 Linux 内核之上的。这意味着 Linux 中的大多数命令都可以在终端模拟器或 adb shell 中使用。然而，这是一个有限的列表，因为 Linux 提供了更广泛的命令集以及容易添加的外部模块。

不幸的是，Android 不支持这么多命令，但这可以很容易地改变，感谢 XDA 论坛成员 [jaromil.rojo](http://forum.xda-developers.com/member.php?u=4184274) ，他将 ZSh 移植到 Android。ZSh 是一个为交互使用而设计的 shell，尽管它也是一种强大的脚本语言。它提供了在我们的设备上使用大量外部命令的能力。到目前为止，ZShaolin 支持以下项目:

*   [FFMpeg](http://ffmpeg.org/) 对音频和视频文件进行转换、解码和编码
*   [ImageMagick](http://www.imagemagick.org/) 转换和操作所有图像格式
*   [Sox](http://sox.sourceforge.net/) 操纵和转换音频文件
*   [OggZ](http://xiph.org/oggz/) 用于操作 DRM 免费音频/视频(Ogg/Vorbis/Theora)
*   [LUA](http://www.lua.org/) 脚本语言
*   Awk、Sed、Grep 和令人敬畏的 Z-Shell

以及更小的工具，如:

*   [Vim](http://www.vim.org/) 和 [Emacs](http://www.gnu.org/software/emacs/) 高级文本编辑器，具有语法高亮等功能
*   用于跟踪文档的分布式版本控制
*   [Rsync](http://rsync.samba.org/) 通过网络可靠地移动大文件
*   SSh 安全外壳远程登录在线服务器
*   午夜指挥官文件管理器和 Lynx 文本网络浏览器
*   GnuPG 对文件和消息进行加密、解密和签名
*   [Lighttpd](http://www.lighttpd.net/) 从您的设备上提供文件和 HTML 页面

正如你所看到的，这是一个强大的工具，允许你做一些事情，如将你的回购推至 Github，甚至在 Android 上解码电影。一切都可以在非根设备上完成，这使得这个应用程序更加酷。Jaromil.rojo 使用自己的工具链编译了这款应用，但该项目是开源的，因此每个人都可以构建它并添加自己的代码贡献。大多数功能都可以在免费版本中获得，该版本缺少 ImageMagick、FFmpeg、Vim fully featured、Emacs、RSync 和更多 ASCII 游戏的二进制文件。如果您想将 ZShaolin 用于这些服务，请考虑使用高级版本来支持开发人员。

ZShaolin 是一个小而强大的应用程序。因此，如果你正在寻找一种工具来让你访问你的 Android 设备上的许多服务，那么就进入[应用线程](http://forum.xda-developers.com/showthread.php?t=2558481)并获得最新的 APK。