# Android 上的 Gmail 关闭后可能会继续使用收件箱[Root]

> 原文：<https://www.xda-developers.com/use-inbox-by-gmail-android-after-shutdown/>

明天标志着谷歌广受欢迎的电子邮件客户端 Gmail 收件箱的死亡。自从谷歌宣布停止收件箱以来，该公司已经[重新设计了 Gmail 应用](https://www.xda-developers.com/gmail-android-material-theme-redesign/)，推出了[智能撰写功能](https://www.xda-developers.com/smart-compose-gmail-android-more-users/)，并宣布计划推出[电子邮件日程安排功能](https://www.xda-developers.com/google-gmail-dynamic-email-scheduling-smart-compose-inbox/)。两个尚未进入 Gmail 应用程序的功能包括“[保存到收件箱](https://www.xda-developers.com/google-inbox-inboxit-share-content-to-email/)功能的等效功能、捆绑、提醒和固定项目，尽管据报道最后三个功能正在测试中。对于许多用户来说，从收件箱过渡到 Gmail [是痛苦的](https://www.reddit.com/r/Android/search?q=inbox)，但如果你有一部安卓智能手机，或许可以继续使用收件箱一段时间。

当我在 APK 挖掘的时候，我学到了一点关于 Android 应用程序是如何把你锁在外面的。事实证明，它所做的只是将当前系统时间与明天格林威治时间午夜进行比较。如果明天已经过了午夜，那么收件箱应用程序将不再让你选择按下“不是现在”并继续使用该应用程序。

不过，这很容易绕过。一种方法是在“设置”中更改日期和时间，但我不建议这样做，因为这会干扰大量依赖时间的应用程序(如天气应用程序、日历应用程序和收件箱本身)。相反，你所要做的就是启动收件箱应用程序，用一个标志告诉它倒计时定时器仍然活跃，即使它并不活跃。这绕过了应用程序用来判断时间是否到了的检查，因此应用程序将总是向您显示“不是现在”选项。为了测试这一点，我将系统时钟更改为更晚的日期，导致收件箱告诉我，如果正常启动，“此应用程序不再可用”，但仍然允许我在使用这一技巧启动应用程序时使用它。我不能保证这将永远有效，也不能保证收件箱的所有最佳功能将长期有效，但这可能会让你坚持到 Gmail 应用程序获得承诺的收件箱功能。

### 如何在 Android 上继续使用 Gmail 收件箱

**要求:**

*   你需要 Gmail 应用程序收件箱的最新版本。
*   你需要一个有根的 Android 设备，因为你启动的活动是未报告的。修改收件箱应用程序是可能的，但我不认为很多人会想安装一个电子邮件客户端的改装 APK。

要在启动收件箱时绕过检查，只需运行以下 shell 命令:

```
 su
am start -n "com.google.android.apps.inbox/com.google.android.apps.bigtop.activities.SwitchActivity" --ez "countDown" true 
```

然后按下“现在不行”后，就可以正常打开收件箱 app 继续使用了。如果收件箱还在内存中，你就不需要重新输入这个命令，但是如果你要干净地启动应用程序，你就必须重新输入。如果你不想一遍又一遍地运行这个命令，我用 Tasker 做了一个快速的应用程序，它会为你发送这个命令。你可以从这里下载。安装完成后，只需点击“启动收件箱”应用程序即可运行。它会要求您授予它 root 访问权限，以便它可以运行该命令。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*