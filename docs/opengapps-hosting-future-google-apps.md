# [更新:转移到 SourceForge] OpenGapps 团队解释了他们的 Google apps 托管情况的未来

> 原文：<https://www.xda-developers.com/opengapps-hosting-future-google-apps/>

**更新(美国东部时间 2019 年 8 月 23 日下午 2:30):**OpenGApps 团队正在将其主机从 GitHub 转移到 SourceForge。

虽然 Android 是开源的，但大多数用户很难忍受使用没有 Google Play 应用和服务的 Android 设备。像 OpenGApps 这样的项目使得用户在定制的 rom 上轻松获得他们喜欢的谷歌应用成为可能。OpenGApps 甚至有不同大小的捆绑包，每个捆绑包都由 Google Play 服务和谷歌 Play 商店以及其他一些 Google 应用组成。

OpenGApps 有一个网站，可以很容易地选择您想要的 GApps 软件包，但您可能已经注意到几天前他们所有的下载突然停止工作了几个小时。事实证明，该项目因违反 GitHub 的[服务条款](https://help.github.com/articles/github-terms-of-service/#c-acceptable-use)而受到 GitHub 管理层的抨击，正如该团队在[最近的博客帖子](https://opengapps.org/blog/post/2019/02/17/github-situation/)中解释的那样。

## OpenGApps 的 APK 存储库正在改变位置

在 GitHub 上托管项目的各方必须"*同意，未经 GitHub 的明确书面许可，不得复制、复印、拷贝、销售、转售或利用服务的任何部分、服务的使用或服务的访问。*“GitHub 不喜欢 OpenGapps 在他们的仓库里存储这么多巨大的 apk。原因是这是对 Git 的低效使用，因为当存储库变得太大时，服务的性能会很差。很长一段时间以来，OpenGapps 将 apk 存储在 GitHub 库中，然后他们的构建脚本使用这些 apk 来编译 flashable 包，但这将很快发生变化。

为了回应 GitHub 的担忧，OpenGApps 团队决定他们的最佳行动方案是用 [GitLab Community Edition](https://www.xda-developers.com/gitlab-ultimate-gitlab-gold-free-open-source-projects-education/) 自托管他们的 APK 存储库。主要的脚本库仍将托管在 GitHub 上，但团队将很快更新构建脚本，以重定向到 GitLab 上的新 APK repos。至于 OpenGApps flashable 版本，你可以在该项目的 [GitHub 发布页面](https://github.com/opengapps/opengapps/releases)上找到。

## 为 Android Q 做好准备

OpenGApps 团队正在为第一个正式发布的 Android Q 开发者预览版做准备，这样他们就可以提取为 Android 10 构建的 GApps 了。虽然该团队有信心及时完成构建，但它正在通过 PayPal 寻求捐赠形式的支持。这将有助于团队应对托管成本的增加，并激励他们继续进一步发展。

**[支持 OpenGApps (PayPal)](https://www.paypal.com/donate/?token=mijlwcllYNkT3lJnOxOmAXq-IgOrXimaDXdUlQThpFvMxzduA64NJd8rSPNnBOhrWrNGtm&country.x=US&locale.x=US)**

* * *

## 更新:转移到 SourceForge

OpenGApps 团队已经宣布他们将把主机从 GitHub 转移到 SourceForge。他们之前将他们的 APK 库转移到了 Gitlab，然后 GitHub 给了他们一个新的限制，强迫他们从发行版中删除 ZIP 包。在权衡了几种不同的选择后，团队决定迁移到 SourceForge。现在可以在[sourceforge.net/projects/opengapps/files](https://sourceforge.net/projects/opengapps/files)找到新版本。

**来源:[OpenGApps](https://opengapps.org/blog/post/2019/08/23/sourceforge-migration/)**