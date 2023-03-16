# [更新 2:重新推出]Windows 10 2020 年 5 月更新带来了 WSL 2，改进的 Cortana 助手，以及对 ARM 设备的“你的电话”呼叫

> 原文：<https://www.xda-developers.com/microsoft-windows-10-may-2020-update-wsl-2-revamped-cortana-assistant-your-phone-calls-arm-devices/>

**更新 2(美国东部时间 2020 年 6 月 10 日上午 10 点 42 分):**微软正在为之前版本的设备重新推出 Windows 10 2020 年 5 月更新，其中包括即将推出的 Surface Pro 7 和 Laptop 3 的修复程序。

**更新 1 (06/01/2020 @ 06:42 AM ET):** 微软在最新更新中发现了漏洞，因此将该更新置于“兼容性保留”状态。滚动到底部了解更多信息。下面保留了 2020 年 5 月 28 日发表的文章。

根据 StatCounter 的数据，Windows 占据了 76.5%的市场份额，这意味着世界上每四台电脑中就有三台运行 Windows。虽然 Windows 不可否认地失去了其作为跨平台操作系统的主导地位，但它仍然是许多许多用户的首选桌面。Windows 的最新版本 Windows 10 现在[正在接收 2020 年 5 月的稳定更新](https://blogs.windows.com/windowsexperience/2020/05/27/whats-new-in-the-windows-10-may-2020-update/)，它带来了几个关键功能，如 Windows Subsystem for Linux (WSL) 2、改进的 Cortana 体验、ARM 上 Windows 的手机功能等等。

## 用于 Linux 的 Windows 子系统(WSL) 2

用于 Linux 2 的 Windows 子系统[在微软 Build 2019](https://www.xda-developers.com/microsoft-announces-windows-terminal/) 期间首次公布，现在正在稳定的 Windows 10 分支下向所有用户推出。这次更新为稳定分支带来了一个完整的 Linux 内核。作为此次更新的一部分，WSL 2 现在也可以通过 Windows Update 更新[，所以用户不再需要仅仅依靠命令行来更新内核。](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004/)

微软确实在微软 Build 2020 上宣布了对 WSL 2 的 GPU 加速和 Linux GUI 应用支持。但是，这些功能甚至对 Windows 内部人员来说都还不可用，所以在稳定分支上肯定会有更多的用户等待。

## Cortana 基于聊天的用户界面

这次 Windows 10 版本更新的另一个亮点是新的 Cortana 体验，它现在采取与数字助理聊天的形式。

用户现在可以在基于聊天的用户界面中，通过文本或自然语言的语音与微软的数字助理进行交互。您可以在桌面上调整、移动和停靠应用程序窗口，以适应您偏好的工作流程。Cortana 将能够帮助你更快地访问信息，更快地与人联系，并帮助你跟踪你的日程安排。Cortana 可以完成的具体任务包括日历和日程协助，帮助加入微软团队的会议，了解组织中的人，制作列表和设置提醒，打开应用程序和设置页面，获得定义和快速回答，以及获得天气和新闻更新。

## 您的手机在 ARM 上运行 Windows 10

Windows 10 的 2020 年 5 月更新为 ARM 支持的 PC 带来了您的手机应用程序的通话功能。你的手机应用程序可以让你拨打、接听或回复电脑上的来电。以前，只有在您拥有受支持的 Android 设备和 x86/x86-64 Windows 10 PC 的情况下，该功能才有效。然而，随着 2020 年 5 月 Windows 10 的更新，微软现在开始在 ARM 设备上的 Windows 10 桌面手机应用程序中启用这一功能，如微软 Surface Pro X 和三星 Galaxy Book S。

## 其他功能

此更新中的其他小功能包括:

*   更快的蓝牙配对-设备现在可以直接从通知中的快速设置配对，而不是打开设置。
*   Windows 表情键盘中有更多的 kaomoji。
*   虚拟桌面现在可以命名了。
*   Xbox Game Bar 现在支持第三方小部件，允许您自定义覆盖体验以适应您的游戏方式。
*   Microsoft Edge 通过利用段堆功能改进了内存。
*   计算器应用程序现在可以浮动在其他窗口的顶部。
*   记事本应用程序正在更新，包括环绕查找/替换、快速文本缩放，以及通过在标题栏中显示星号来显示文件何时有未保存的更改。

Windows 10 2020 年 5 月更新正在向台式机推出，尽管微软最初限制了那些通过 Windows Update 寻求更新的运行 1903 和 1909 版本的设备的可用性。如果您希望安装更新，请导航到“Windows Update 设置”窗格(“设置”>“更新和安全”>“Windows Update”)，然后选择“检查更新”。更新出现后，您可以选择下载并安装。请注意，更新可能不会立即可见，因为微软将逐步推出。

**来源: [Windows 博客](https://blogs.windows.com/windowsexperience/2020/05/27/whats-new-in-the-windows-10-may-2020-update/)**

* * *

## 更新:Windows 10 2020 年 5 月更新暂停兼容性

微软上周发布了 Windows 10 2020 年 5 月更新，最初的推出按预期开始。然而，[自从更大范围的推广以来，一些错误和问题](https://docs.microsoft.com/en-us/windows/release-information/status-windows-10-2004)浮出了水面。这些问题中的几个已经导致了“兼容性保留”，这实质上阻止了通过 Windows Update 安装 Windows 10 2020 年 5 月更新。因此，如果您一直在检查更新，但没有看到任何东西，很可能您的设备现在被阻止更新。微软还向 Windows Update 添加了一条警告，针对那些不准备更新的设备。

希望，一旦错误和问题被修复，我们可以看到一个更广泛的推广，包括修复。

**来源:[The Verge](https://www.theverge.com/2020/6/1/21276653/microsoft-windows-10-may-2020-update-block-known-issues-list?utm_campaign=theverge&utm_content=chorus&utm_medium=social&utm_source=twitter)**

* * *

## 更新 2: Windows 10 版本 2004/2020 年 5 月更新重新推出

在第一次首次展示后，由于一些问题浮出水面，更大范围的展示暂停了。微软已确定问题出现在微软 Surface Pro 7 和微软 Surface Laptop 3 上，其中用户报告了意外重启。该公司已确定该问题与始终在线、始终连接的网络适配器有关，并已通过补丁 KB4557957 解决了该问题。

因此，针对 Windows 10 版本 2004 的[更广泛的更新部署现已针对运行 Windows 10 版本 1903 和 1909 的设备恢复](https://docs.microsoft.com/en-us/windows/release-information/status-windows-10-2004)。微软 Surface Pro 7 和微软 Surface Laptop 3 的用户仍然需要等待一段时间，因为微软已经为更新对这些设备进行了保护，并将在未来几周内解除保护。