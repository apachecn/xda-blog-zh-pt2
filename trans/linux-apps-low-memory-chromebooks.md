# Linux 应用现在可以在低内存的 Chromebooks 上运行得更好

> 原文：<https://www.xda-developers.com/linux-apps-low-memory-chromebooks/>

# Linux 应用现在可以在低内存的 Chromebooks 上运行得更好

最近的一项变化通过动态管理 RAM 为 Chrome OS 上的 Linux 应用程序引入了更好的资源管理——这对低内存 Chromebooks 来说是个好消息。

今年早些时候，Chrome 上的 Linux 应用程序[在 Pixelbook](https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/) 上发布，Pixelbook 是一款具有 8GB RAM 的快速 Chromebook。从那以后，[从低端到高端已经有数十款设备获得了支持](https://www.xda-developers.com/apollo-lake-chromebooks-acer-asus-lenovo-dell-linux-app/)，甚至 ARM Chromebooks 也是如此。[最近的 Chromium commit](https://chromium.googlesource.com/chromiumos/platform/crosvm/+/448516e3f985dd13fb5cd16f2c9efbcf097f9fa5) 通过动态管理 RAM 为 Chrome OS 上的 Linux 应用程序引入了更好的资源管理——这对低内存 Chromebooks 来说是个好消息。

 <picture>![The balloon taketh away](img/eab1117d22d7d98dddc6aea59c03bdee.png)</picture> 

Linux apps within the VM get dynamic memory management for low-memory conditions

Crostini 项目允许用户在虚拟机上运行 Linux 应用程序，与操作系统的其余部分隔离。虽然在虚拟机中隔离应用程序使其更加安全，但这使得操作系统很难知道虚拟机中发生了什么来正确分配 RAM。Chrome 开发人员最初决定过度分配内存，这意味着许多用户的虚拟机消耗的内存超过了其需求。对于顶级规格的 Pixelbook 来说很好——对于 4GB RAM 来说就不那么好了[三星 Chromebook Plus](https://www.xda-developers.com/samsung-chromebook-plus-linux-apps/) 。最近的这一变化引入了新的控件，可以动态响应虚拟机中的 RAM 使用情况，并在应用程序完成后将其返回给 Chrome。

一般来说，在幕后自动化资源管理对于最终用户来说是非常好的，并且在 Crostini 项目在几个月后面向大众推出之前为其增添了另一层光泽。用于 Chrome 的 Linux 应用将在 9 月份发布的 69 版中进入[稳定版和测试版。在此之前，Chrome OS 用户将不得不转向开发者或金丝雀频道。](https://www.xda-developers.com/stable-linux-apps-chrome-os-69/)