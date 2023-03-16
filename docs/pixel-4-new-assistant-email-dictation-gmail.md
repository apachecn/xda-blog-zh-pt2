# Pixel 4 的新助手准备在 Gmail 中添加更好的电子邮件听写功能

> 原文：<https://www.xda-developers.com/pixel-4-new-assistant-email-dictation-gmail/>

# Pixel 4 的新助手准备在 Gmail 中添加更好的电子邮件听写功能

谷歌 Pixel 4 上的新谷歌助手更快更智能，但谷歌在 I/O 上展示的一个功能却不见了:Gmail 中更好的电子邮件听写功能。

在今年早些时候的 Google I/O 上，Google [展示了其 Google Assistant 服务的更快版本](https://www.xda-developers.com/google-pixel-4-faster-google-assistant/)。在演示过程中，演示者让助手给一个名为“Jessica”的联系人发送一封电子邮件，启动 Gmail，联系人“Jessica Kulla”预填在“收件人”栏中。由于持续的对话支持，演示者可以完全通过助手口述电子邮件的“主题”和“正文”字段。新的谷歌助手[上个月推出了带有 Pixel 4 的](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/)，但这种新的、更好的电子邮件听写流程还没有推出。然而，我们发现有证据表明它仍在开发中，可能会出现在谷歌助手的未来更新中。

**[谷歌 Pixel 4 论坛](https://forum.xda-developers.com/pixel-4)**| |**|[谷歌 Pixel 4 XL 论坛](https://forum.xda-developers.com/pixel-4-xl)**

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

如果你现在要求 Pixel 4 上的谷歌助手(或任何其他设备)发送一封电子邮件，你会看到一个如下所示的对话框:

Google Assistant 会引导你通过语音发送电子邮件，让你说出你的信息和主题。这种电子邮件听写流程感觉不如其他新的助手操作集成得好。事实上，发送电子邮件甚至没有被列为新的谷歌助手在 Pixel 4 上可以做什么的例子。稍加修改，我就能让新的谷歌助手启动 Gmail 应用程序，在“收件人”栏中预先填入了我的一个联系人马克斯·温巴赫(Max Weinbach)。

然而，我无法指定实际的邮件主题或正文。查看谷歌应用程序 APK，有一个被禁用和导出的服务叫做`com.google.android.apps.gsa.nga.engine.keyboard.KeyboardService`，它可能为新的谷歌助手启用键盘听写。一旦这项功能准备就绪，你将能够直接从谷歌助手而不是 Gboard 或其他键盘应用程序听写键盘输入。

* * *

*感谢 PNF 软件为我们提供了使用 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) 的许可，这是一款用于 Android 应用的专业级 rever* *se 工程工具。*