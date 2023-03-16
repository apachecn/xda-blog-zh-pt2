# Android Pie 为第三方开发者开放了最近的应用定制

> 原文：<https://www.xda-developers.com/android-pie-recent-apps-customization/>

在 Android 9 Pie 之前，Android 的堆叠卡最近应用程序界面自 Android 5.0 Lollipop 首次推出以来基本保持不变。随着 Android Pie 中手势导航的引入，谷歌[改进了最近的应用概述屏幕](https://www.xda-developers.com/everything-new-android-p-developer-preview-2/)。新界面的特点是水平排列的大型概览卡，但这不是最近应用程序界面的最大变化。由于最近应用程序的代码现在集成到股票启动器中，现在你可以从最近应用程序概览无缝过渡到启动器的应用程序抽屉。正如 *AndroidCentral 的* Ara Wagoner [解释的](https://www.androidcentral.com/android-pie-recents-system-launchers-only)，这让第三方启动器处于劣势，因为只有预装的系统启动器才能与最近的应用程序 UI 集成。另一方面，如果你有 root 权限，Android Pie 对最近应用概述的改变实际上开辟了一个全新的定制途径。

## 在 Android Pie 之前自定义最近的应用程序概述

在 Android 9 Pie 之前，多任务接口完全由 SystemUI 包处理。因此，定制最近应用程序屏幕的唯一方法是修改 SystemUI。这对于定制的 rom 来说不是问题，但是对于那些只有 root 权限的人来说就要棘手得多了。在这种情况下，唯一的选择是要么使用 Magisk 模块完全替换 SystemUI，要么使用 Xposed 模块替换处理最近应用程序 UI 的代码。不幸的是，这两个选项都有缺陷，因为任何这样的修改都是特定于 OEM 的，并且很容易被任何给定的更新破坏。对于一个开发者来说，为多种设备维护一个最新的应用切换模式将是一场噩梦。然而，如果开发人员不再需要担心修改 SystemUI 或其他系统应用程序，那么构建定制的最新应用程序转换器将会更容易。Android Pie 应该会让这种定制成为现实。

## 在 Android Pie 中自定义最近的应用概述

与你可能听说的相反，新的 Android Pie 最近应用程序 UI 不是 Pixel Launcher 功能。Pixel Launcher 是谷歌 Pixel 和谷歌 Pixel 2 上预装的启动器，所以它只是碰巧负责处理那些智能手机上最近的应用程序概述。在像 Essential Phone 这样的其他手机上，[预装的启动器](https://www.xda-developers.com/essential-phone-android-pie-android-9/)也集成了最近的应用程序 UI。[如](https://www.xda-developers.com/android-p-beta-3-oneplus-6/)OnePlus 6 所示，原始设备制造商甚至可以定制最近的应用程序屏幕。现在更新的 [AOSP 启动器](https://android.googlesource.com/platform/packages/apps/Launcher3/)的[源代码](https://www.xda-developers.com/android-pie-source-code-aosp/)已经可用，我们可以确切地看到新的最近应用程序界面如何与启动器集成。我们最初认为，第三方启动器需要捆绑到一个定制的 ROM 中，以利用最新的应用程序集成，但事实证明并非如此。

Lawnchair launcher 是一款流行的 Pixel Launcher 替代品，其开发者将处理最近应用的代码集成到了他们的应用中。然后，他们想出了让他们的启动器被识别为最近应用程序概览的默认处理程序所需的步骤。这使得在 Pixel 2 上使用 Lawnchair 而不是 Pixel 启动器作为默认启动器成为可能，而不会失去水平应用切换器或向上滑动应用抽屉。我们在下面的视频中演示了这一点，该视频记录在谷歌 Pixel 2 XL 上运行股票，根构建 Android 9 Pie。

Lawnchair 团队是怎么做到的？嗯，我被要求暂时不要分享他们是如何做到的，但让应用程序获得正确的权限以被系统识别却出乎意料的简单。不过，他们的方法仍在发展中，所以还没准备好与世界分享。(他们做的 Magisk 模块不行，我只好手动把正确的文件放到正确的位置，然后运行一个命令。)这也是为什么最近的应用程序屏幕看起来和传统的 Android 9 一模一样——他们还没有开始定制它。但是 Lawnchair 的开发者至少表明，在第三方启动器中实现新的最新应用程序 UI 是可能的。下一步是像一加在 OnePlus 6 上做的那样定制它。一旦 Lawnchair 的开发者有更接近的东西发布，我们会让你们都知道。