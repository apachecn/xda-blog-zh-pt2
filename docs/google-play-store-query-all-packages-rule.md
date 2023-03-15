# 如果没有充分的理由，Play Store 不会允许应用程序扫描其他应用程序

> 原文：<https://www.xda-developers.com/google-play-store-query-all-packages-rule/>

# 没有充分的理由，谷歌 Play 商店不会允许应用程序扫描其他应用程序

谷歌将从 6 月 1 日开始从 Play Store 中移除使用 QUERY_ALL_PACKAGES 而没有合理理由的应用。

Android 应用程序可以使用 QUERY_ALL_PACKAGES 权限检查安装了哪些其他应用程序，但鉴于安全和隐私风险，该功能仅适用于*实际上*需要它的应用程序(如应用程序启动器或备份工具)。谷歌去年表示，它将开始从 Play Store 中删除没有合理理由使用许可的应用程序，现在这条规则已经生效。

据报道，谷歌已经向使用 QUERY_ALL_PACKAGES 权限发布应用的开发者发送了一封电子邮件，通知他们需要在 Play 控制台中填写相关的权限声明。声明包括解释为什么“你的应用中的核心功能”需要许可，包括书面描述和简短的视频演示。从 2022 年 6 月 1 日开始，没有声明的应用程序有被从谷歌 Play 商店移除的风险。

Android 10 和更早的版本允许任何应用程序获得已安装应用程序的完整列表，没有任何权限提示或障碍。这对隐私和安全来说是一个重大问题(例如，应用程序可以根据安装的应用程序来定向广告)，所以从 Android 11 开始，[应用程序列表默认被过滤](https://medium.com/androiddevelopers/package-visibility-in-android-11-cc857f221cd9)。应用程序仍然可以通过 QUERY_ALL_PACKAGES 权限绕过新的过滤器，但[谷歌去年表示](https://www.xda-developers.com/google-is-restricting-which-apps-can-see-the-other-installed-apps-on-your-device/)它不会允许 Play Store 上的应用程序使用非必要功能的权限。

Play Store 政策变化的原定日期是 2021 年 5 月 5 日，首批不符合规定的应用程序将于 2021 年 11 月开始下架。出于“新冠肺炎相关的考虑”，谷歌后来推迟了开始日期

谷歌为使用辅助服务的[应用程序创建了类似的规则，因为它试图平衡应用程序的要求与安全措施。如果应用程序开发人员能够解释为什么他们的应用程序没有 QUERY_ALL_PACKAGES 就无法运行，他们就可以留在 Play Store 上——假设谷歌的支持人员反应灵敏、乐于助人，而](https://www.xda-developers.com/google-trying-limit-apps-accessibility-service/)[并不总是这样](https://www.xda-developers.com/google-developer-account-ban-raya-games/)。

**来源:** [Reddit](https://www.reddit.com/r/android_devs/comments/tw0pbc/query_all_packages_permission_declaration/)