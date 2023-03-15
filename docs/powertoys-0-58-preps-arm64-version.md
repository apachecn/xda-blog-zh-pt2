# PowerToys 0.58 更新准备原生 ARM64 版本的应用程序

> 原文：<https://www.xda-developers.com/powertoys-0-58-preps-arm64-version/>

微软再次更新了用于 Windows 的 PowerToys 工具套件，使其版本达到 0.58。这个新的更新本身并没有增加任何新的面向用户的功能，但它确实做出了一些重要的改变，包括为即将到来的 ARM64 版本的应用程序做准备。目前，PowerToys 只为 x64 处理器设计，这意味着要在 Surface Pro X 等 ARM 设备上运行，它需要使用仿真，这会影响性能。PowerToys 在 ARM64 上运行所需的许多组件现在都包含在包中，所以希望我们现在不用等太久。

然而，这并不是此次更新改变的全部。该团队在幕后做了一些工作，使电动玩具达到更现代的标准。首先，它不再使用旧的 WebBrowser 控件来显示网页内容，而是切换到 WebView2，由基于 Chromium 的微软 Edge 浏览器提供支持。

同样，PowerToys 0.58 放弃了所有使用。NET Core 3.1 并完全过渡到。NET 6，所以更符合当前情况。关于开发方面的最后一点，PowerToys 设置窗口现在可以在 WinUI 3 上运行，这是微软 UI 框架的最新版本。此前，它使用 XAML 群岛将 UWP 风格的设计融入 Win32 应用程序中，但 WinUI 3 也将所有这些元素结合在一起，它是更新的。该团队表示，这种转变应该会解决一些与使用 XAML 群岛相关的问题，因此总体来说事情应该会更好。

除此之外，PowerToys 0.58 中还有大量较小的修复和调整，改善了整体体验。如果你想看到所有的改进，你可以阅读下面的完整列表。

### PowerToys 0.58 变更日志

**通用**

*   代码中的拼写检查修复。感谢 [@jsoref](https://github.com/jsoref) ！
*   修复了由于 GitHub API 更改导致的与拼写检查相关的 CI 错误。感谢 [@jsoref](https://github.com/jsoref) ！
*   修复了 GitHub 的文档参考。感谢 [@Cyl18](https://github.com/Cyl18) ！

**ARM64**

*   为 ARM64 端口准备解决方案和属性文件。感谢 [@snickler](https://github.com/snickler) ！
*   将未处理的异常处理程序端口连接到 ARM64。感谢 [@snickler](https://github.com/snickler) ！
*   设置项目到 ARM64 的端口。感谢 [@snickler](https://github.com/snickler) ！
*   大多数 PowerToys 到 ARM64 的端口。感谢 [@snickler](https://github.com/snickler) ！
*   调试工具到 ARM64 的端口。

**永远在顶端**

*   修正了某些应用程序中窗口最顶端的重置状态。(这是 0.57 的修补程序)

**颜色选择器**

*   CIEXYZ 格式现在可以用大写字母正确显示了。

**FancyZones**

*   在 Windows 11 上恢复圆角，并添加控制此行为的设置。(这是 0.57 的修补程序)
*   修正了 Windows 终端窗口打开时不会被抓取的错误。(这是 0.57 的修补程序)
*   改进了网格编辑器中的讲述人支持。(这是 0.57 的修补程序)
*   修复了 Windows 11 上恢复圆角时的 bug。(这是 0.57 的修补程序)
*   修复了在不同的 dpi 设置下不能正确调整窗口大小的问题。(这是 0.57 的修补程序)
*   从屏幕标识符中删除了分辨率，因此当分辨率改变时区域不会重置。
*   编辑时根据新的缩放比例/分辨率缩放画布布局。
*   发布一个新工具来帮助调试与 FancyZones 的交互。

**文件浏览器**

*   修复了开发文件预览中的崩溃，如果设置文件还没有被创建。(这是 0.57 的修补程序)
*   新的文件类型被添加到开发文件预览(。注册“，”。xslt“，”。xsd“，”。wsdl“，”。伊诺“，”。pde“，”。剃刀”)。感谢[@亚伦-勇克](https://github.com/Aaron-Junker)！
*   修复开发文件预览中现有的“文件仍在使用”问题。感谢[@亚伦-勇克](https://github.com/Aaron-Junker)！
*   开发文件预览现在能够以不区分大小写的方式解释文件扩展名。感谢[@亚伦-勇克](https://github.com/Aaron-Junker)！
*   SVG 和 markdown 查看器不再使用 WebBrowser，而是使用 WebView2。
*   Markdown 预览现在尊重 Windows 上的黑暗模式设置。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！

**鼠标实用程序**

*   修复了当鼠标工具在特定显示器配置上激活时，图标上设置的快捷键无法激活的错误。

**电动玩具运行**

*   修复了 PowerToys 在更新设置时使用高 CPU 和内存的问题。(这是 0.57 的修补程序)
*   将“以不同用户身份运行”功能添加到程序、外壳和搜索插件中。感谢 [@htcfreek](https://github.com/htcfreek) ！(这是 0.57 的修补程序)
*   修复了未设置虚拟桌面注册表项时 WindowWalker 崩溃的问题。感谢 [@htcfreek](https://github.com/htcfreek) ！(这是 0.57 的修补程序)
*   修复了 VS 代码工作区在安装或更新后不使用用户路径变量的问题。感谢 [@ricardosantos9521](https://github.com/ricardosantos9521) ！(这是 0.57 的修补程序)
*   修复了系统插件导致 PowerToys 运行缓慢时，许多网络接口存在。感谢 [@htcfreek](https://github.com/htcfreek) ！(这是 0.57 的修补程序)
*   修正了程序插件不显示空目标的特殊快捷方式，如控制面板。(这是 0.57 的修补程序)
*   终端插件的附加日志记录。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！(这是 0.57 的修补程序)
*   网络搜索和 URI 插件现在有更好的代码来检测默认浏览器。
*   修正了服务插件不能正确使用空格的问题。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！
*   修正了终端插件不能正确识别配置文件的问题。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！
*   修复了最新的 VSCode 内部版本没有显示在 VSCode 工作区插件中的问题。感谢 [@JacobDeuchert](https://github.com/JacobDeuchert) ！
*   增加了单位转换器插件中的浮点数精度。
*   VSCode 工作区现在可以找到 VS 代码的可移植安装。感谢 [@harvastum](https://github.com/harvastum)
*   修正了桌面未初始化时启动 PowerToys 运行的问题。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！

**设置**

*   设置现在运行在 WinUI3 而不是 XAML 群岛。
*   当 runner 以管理员身份启动时，Settings 不再以管理员身份运行。

**跑步者**

*   使用合理的默认时间来重新检查更新，以避免循环写入日志。(这是 0.57 的修补程序)
*   如果安装是最新的，Runner 会清理更新目录。感谢 [@davidegiacometti](https://github.com/davidegiacometti) ！

安装人员

*   分发一份签名的。内部的 msi。exe 安装程序引导程序。(这是 0.57 的修补程序)
*   移除了。来自安装程序的. NET 核心依赖项。
*   部分支持 ARM64 安装程序。
*   更新了。NET 到 6.0.4。
*   重新安装/更新时强制更新所有文件，尝试并修复安装问题。

**开发**

*   电动玩具不再依赖于。网芯。
*   WinUI3 是一个新的依赖项。因此，设置现在针对 win10-x64 和 win10-arm64。

PowerToys 过去的几次更新主要集中在质量改进上，而不是新功能上，但这不一定是件坏事。这些本质上的变化也应该使应用程序的维护变得更加容易。最近，我们看到一个名为 Peek 的新 [PowerToys 功能正在开发中，尽管它还不可用。它本质上是 macOS 快速查看的 Windows 版本，允许您快速查看文件，而无需在各自的应用程序中打开它们。](https://www.xda-developers.com/powertoys-peek-windows-version-macos-quick-look/)

如果你感兴趣的话，你可以今天从 GitHub 下载 PowerToys 0.58，或者如果你已经有了的话，在应用内检查更新。