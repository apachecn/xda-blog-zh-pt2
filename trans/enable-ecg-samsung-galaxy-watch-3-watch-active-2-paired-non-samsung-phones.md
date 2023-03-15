# 如何在与非三星手机配对的三星 Galaxy Watch 3、Watch Active 2 上启用 ECG

> 原文：<https://www.xda-developers.com/enable-ecg-samsung-galaxy-watch-3-watch-active-2-paired-non-samsung-phones/>

三星的 [Galaxy Watch 3](https://www.xda-developers.com/tag/samsung-galaxy-watch-3/) 和 [Galaxy Watch Active 2](https://www.xda-developers.com/tag/samsung-galaxy-watch-active2/) 包括一个心电图(ECG)监视器。ECG 监护仪允许用户随时检查自己的心律是否有异常，如房颤(AFib)。但为了使用这项功能，你需要访问三星的心电图监测应用程序。三星[最近获得了 FDA 对该应用的许可](https://www.xda-developers.com/samsung-galaxy-watch-3-watch-active-2-ecg-monitoring-app-us/)，并开始向美国用户推广。然而，这款应用目前无法在非三星设备上运行。这意味着没有三星设备的 Galaxy Watch 3 和 Galaxy Watch Active 2 用户仍然无法利用心电图监测功能。不过，多亏了 XDA 会员 [*xxstd*](https://forum.xda-developers.com/member.php?s=d641a064663133f5dd4735daa9d1b52d&u=11140143) ，你现在可以按照这个简单的教程在非三星设备上实现心电图监测。

**[三星 Galaxy Watch 3 论坛](https://forum.xda-developers.com/smartwatch/samsung-galaxy-watch-3) || [三星 Galaxy Watch Active 2 论坛](https://forum.xda-developers.com/smartwatch/galaxy-watch)**

在我们开始这个过程之前，您需要满足几个要求才能完成本教程。首先，你需要一部 Android 手机、一台 Windows PC、一部 Galaxy Watch 3 或 Galaxy Watch Active 2，以及一个无线网络。然后，您需要从给定的链接下载并安装以下软件:

## 如何在非三星手机上的 Galaxy Watch 3 和 Galaxy Watch Active 2 上启用 ECG

下载完上述所有软件后，安装三星健康监视器 v.v.1..1.0.167 .手机上的 Caravana。然后遵循下面给出的说明:

**在您的 Galaxy Watch 3/Galaxy Watch Active 2 上:**

*   进入“设置”>“关于手表”>“软件”，然后轻按“软件版本”5 次，直到手表显示“开发者模式开启”
*   回到“关于手表”，点击“调试”打开它
*   现在，导航到手表上的 Wi-Fi 设置，将 Wi-Fi 设置更改为始终开启，并将其连接到与您的电脑相同的无线网络
*   重新启动手表，并确保它在重新启动后连接到 Wi-Fi 网络。

**在您的 Windows 电脑上:**

*   启动 Tizen 包管理器，导航到“5.5 可穿戴”，然后单击安装按钮(“X.X 可穿戴”版本需要与您手表的当前固件版本相对应，即，如果您的手表显示 Tizen 版本 5.5.0.1，则您需要安装 5.5 可穿戴)
*   向下滚动到 Tizen SDK 工具，然后单击安装按钮
*   单击扩展 SDK 选项卡
    *   单击附加项目上的箭头
    *   安装三星证书扩展和三星可穿戴扩展
*   检查进度标签，一旦它显示 100%，你可以关闭 Tizen 包管理器(不要启动 Tizen 工作室)
*   打开“证书管理器”
*   单击“+”图标，并在弹出窗口中单击三星徽标
    *   点击设备类型>移动/可穿戴设备>点击下一步
    *   创建证书配置文件(选择任意名称) >单击下一步
    *   创建新的作者证书>单击下一步
    *   输入作者姓名、密码，并在下一个屏幕中确认密码(记住密码，因为您在签署 TPK 文件时将需要它) >单击下一步
    *   然后会弹出一个窗口，要求您使用 Samsung 帐户登录，输入您的帐户信息并登录
    *   现在，它将显示证书已保存在“C:/Users/USERNAME/Samsung certificate/cert _ name”>中，单击下一步
    *   创建新的分发服务器证书>单击下一步
    *   不要更改权限和密码信息，不要关闭窗口
    *   在您的手表中启用调试模式，并将其连接到您的电脑
*   打开“设备管理器”
*   点击右上角的“远程设备管理器”图标
*   在以下弹出窗口中，单击右上角的“扫描设备”找到您的手表
*   一旦它找到你的手表，打开连接并关闭弹出窗口。现在，您应该能够在设备管理器中看到许多调试信息
*   回到 Tizen 证书管理器，你会看到一个 DUID 已经自动添加>点击下一步
*   现在，您应该看到您的证书已保存在“C:/Users/USERNAME/Samsung certificate/cert _ name”>中，单击“完成”
*   解压缩桌面上的 Fit2Installer.zip 文件夹
*   导航到您刚刚创建的证书，并复制文件夹中的所有文件
*   转到“C:\ Users \ USERNAME \ Desktop \ fit 2 installer \ cert ”,粘贴你刚才复制的所有文件
*   复制 ecg.tpk 文件，粘贴到“C:\ Users \ USERNAME \ Desktop \ fit 2 installer \ sign _ me”中
*   单击 Fir2Installer 文件夹中的 sign.bat 并输入您的证书密码
*   现在应该显示“Package(C:\ Users \ USERNAME \ Desktop \ fit 2 installer \ install _ me \ ECG . TPK)已成功创建”>按任意键关闭窗口
*   回到“设备管理器”>右键单击设备>选择“安装应用程序”>从“C:\ Users \ USERNAME \ Desktop \ fit 2 installer \ install _ me”中选择 ecg.tpk 文件
*   ECG 应用程序将在几秒钟内安装到您的手表上>打开应用程序
*   在您的手机上打开改装的三星健康监测应用程序，您现在应该能够从您的手表中读取心电图数据。

请注意，由于该功能仅在美国和韩国可用，此安装过程将不会在其他地区工作。一旦它在美国发布，你应该能够以类似的方式启用血压监测功能。

如果您想在与非三星 Galaxy 设备配对时在[三星 Galaxy Watch 4 和 Galaxy Watch 4 Classic](https://www.xda-developers.com/samsung-galaxy-watch-4/) 上启用心电图和血压监测，[请遵循本教程的更新说明](https://www.xda-developers.com/enable-ecg-blood-pressure-galaxy-watch-4-with-non-samsung-phones/)。

* * *

**来源: [XDA 论坛](https://forum.xda-developers.com/smartwatch/samsung-galaxy-watch-3/enable-ecgbp-featur-samsung-phones-t4168567)**