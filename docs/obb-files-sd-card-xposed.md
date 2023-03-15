# 将您的 Obb 文件保存在 SD 卡上，并暴露

> 原文：<https://www.xda-developers.com/obb-files-sd-card-xposed/>

# 不要浪费内部存储；将 Obb 文件保存在 SD 卡上并曝光

Obb 文件自动下载到内部存储器。通过允许游戏使用外置 SD 卡和这个方便的暴露模块来使用您的 SD 卡

Obb 是由多个游戏开发者使用的数据文件格式。以这种格式存储的数据通常包含音乐、视频和其他在安装 APK 后下载的大文件。这使得 APK 更小，开发人员更容易维护。(想象一下每次 app 更新时上传 2 GB 文件！)

额外的数据文件存储在内部存储器中，这不是一个完美的情况——特别是对于拥有外部 SD 卡支持的设备的用户。内部存储在很短的时间内就会满，即使它很大，所以使用外部 SD 卡来保存这些 obb 文件是一个好习惯。XDA 认识到开发人员 [moneytoo](http://forum.xda-developers.com/member.php?u=426237) 提出了一个有趣的解决方案，并创建了一个 Xposed 模块来自动处理 obb 文件。将 android/obb 文件夹移动到外置 SD 卡后，那些文件对游戏来说就是“可见”的了。没必要拿它开玩笑。只需安装模块，移动您的文件，不要浪费您的内部存储。

因为这个模块使用 Xposed 框架运行，所以在尝试之前，请确保您的设备是 root 的并且 Xposed 正在工作。如果你正在使用艺术，你会想回到达尔维克，以使这项工作。

你是游戏玩家吗？如果是这样，请前往 SD Xposed 模块线程上的 [Obb 并尝试一下。](http://forum.xda-developers.com/xposed/modules/mod-obb-sd-v0-1-t2884004)