# DontKillMyApp 是测试手机后台应用查杀的基准

> 原文：<https://www.xda-developers.com/dontkillmyapp-benchmark-test-background-app-killing/>

智能手机公司对每一款新设备的长效电池都提出了更高的要求。无可争议的是，智能手机的电池容量在过去几年里大幅增加——这就是为什么像 [Greenify](https://www.xda-developers.com/greenify-keeps-your-android-running-smoothly/) 这样的工具的受欢迎程度在过去几年里有所下降。然而，为了延长电池备份，制造商们还[调整他们定制的基于 Android 的软件](https://www.xda-developers.com/hmd-global-stop-evenwell-app-killing-nokia-phones/)来杀死或让后台应用程序休眠，其中一些制造商[非常积极地这样做](https://www.xda-developers.com/huawei-cant-download-vlc-play-store/)。这个令人烦恼的问题的受害者之一是 urban droid,[Sleep as Android](https://play.google.com/store/apps/details?id=com.urbandroid.sleep&hl=en_US)的开发者，这是一款智能闹钟应用。同一位开发者正在推出一款名为“DontKillMyApp”的新应用，它将帮助你衡量后台应用在手机上的生存能力。

该应用以 Urbandroid 的早期项目命名—[一个同名网站](https://www.xda-developers.com/phone-software-killing-apps-background/)旨在强调不同制造商如何积极冻结后台应用。虽然[网站](https://dontkillmyapp.com/)提供了一个更全面的定制 Android 皮肤中激进应用程序杀戮的概述，但该应用程序应该提供一个更具体的背景图片，说明手机——更重要的是，你的手机——处理后台应用程序的情况。

要运行基准测试，你需要让手机闲置一段时间，让应用程序测试后台任务的处理情况。它可以让你选择一个小时到八个小时的测试时间，并警告你在此期间不要使用手机或给手机充电。该应用程序显示一个持久的通知，如果你需要使用手机，你可以停止使用相同的基准。

为了测试这一点，该应用程序在持久通知的帮助下在前台运行一个服务，为其添加唤醒锁，并以 10 秒的间隔在主线程上执行一些重复的任务。此外，该应用程序每 8 分钟安排和提醒一次。在测试结束时，它会看到这些命令中有多少已经被执行，并用一个可视化的图表显示出来。

DontKillMyApp 应用程序目前已进入早期访问阶段，你可以试用看看你的手机如何处理后台应用程序。在未来，我们还可以期待在应用程序中看到一些关于如何使应用程序免于被杀死并保持它们在后台运行的建议。

在下面的评论中分享你的成果吧！与此同时，这里有一篇扣人心弦的社论，讲述了应用程序开发人员如何因这些激进的电池优化而遭受损失。

* * *

**Via: [安卓警察](https://www.androidpolice.com/2020/06/24/dontkillmyapp-is-a-new-benchmark-for-how-aggressively-your-phone-kills-background-apps/)**