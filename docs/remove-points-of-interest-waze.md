# 如何删除 Waze 中的兴趣点和广告

> 原文：<https://www.xda-developers.com/remove-points-of-interest-waze/>

[Waze](https://www.waze.com/) ，对于没听说过的人来说，是一个社区驱动的交通和导航 app。它适用于 Android 和 iOS，现在也适用于 [Android Auto](https://www.xda-developers.com/waze-is-now-available-on-android-auto-in-car-units-only/) 。它使用来自其他用户的实时数据来通知用户交通状况、更好的路线，并向用户提供“兴趣点”。这些兴趣点以气球的形式弹出，基本上是位置广告(通常伴随它们的是实际的全屏广告)。在某些情况下，这些广告可能是危险的，会分散司机的注意力，如果用户希望在应用程序上仍然看到道路，就需要取消它们。如下图所示，广告填满了屏幕的顶部，一个弹出窗口显示附近有麦当劳。

*应用中的兴趣点/广告*

然而，由于 XDA 成员[斯卡那迪安](https://forum.xda-developers.com/member.php?u=1542399)，这些兴趣点/广告可以通过使用 [Magisk](https://forum.xda-developers.com/apps/magisk) 或 init.d 脚本来禁用。如果您的 ROM 支持 init.d，并且您希望按照本指南对/system 进行修改，那么您可以简单地按照这些步骤操作，但是将“99waze”文件放在/system/etc/init.d/中。以下步骤取自[这里的](https://forum.xda-developers.com/showpost.php?p=73344318&postcount=6)。除非 Waze 的开发人员专门针对这个脚本，否则这应该适用于将来的更新。

下面的[教程](https://www.xda-developers.com/category/tutorials/) **需要您设备上的 root 访问权限**，因为您将制作一个脚本来修改位于/data 目录中的文件，特别是位于应用程序的 data 文件夹中的文件。这意味着你设备的引导程序可能已经解锁，你已经通过 [SuperSU](https://forum.xda-developers.com/apps/supersu) 或 [Magisk](https://forum.xda-developers.com/apps/magisk) 安装了一个超级用户二进制文件。

* * *

## 删除 Waze 中的兴趣点和广告

### 第一步

如前所述，您需要在设备上安装 Magisk。你也需要一个像 MiXplorer 这样的应用程序，所以请安装它或者任何其他支持 root 的文件管理器。

[appbox xda com.mixplorer]

### 第二步

导航至:

```
 /magisk/.core/post-fs-data.d/ 
```

在文件管理器中，创建一个名为 99waze 的文件。注意导航到/magisk 时，点击右上角的菜单按钮，如果使用 MiXplorer，则点击“显示隐藏”。

### 第三步

请 chmod 755 这个文件(即。更改文件的权限，这可以通过在 MiXplorer 中打开文件的属性来实现。这看起来像下面这样。

### 第四步

将以下几行添加到文件中。

### 99waze

```
 #!/system/bin/sh
sleep 30

sed -i -e 's|.*ExternalPOI.My Coupons Enabled:.*|ExternalPOI.My Coupons Enabled: no|g' /data/data/com.waze/preferences
sed -i -e 's|.*ExternalPOI.Feature Enabled:.*|ExternalPOI.Feature Enabled: no|g' /data/data/com.waze/preferences
sed -i -e 's|.*ExternalPOI.Max POIs Display:.*|ExternalPOI.Max POIs Display: 0|g' /data/data/com.waze/preferences
sed -i -e 's|.*ExternalPOI.Popup Enabled:.*|ExternalPOI.Popup Enabled: no|g' /data/data/com.waze/preferences
sed -i -e 's|.*ExternalPOI.Max POIs Display Small Screen:.*|ExternalPOI.Max POIs Display Small Screen: 0|g' /data/data/com.waze/preferences

chown root:root /data/data/com.waze/waze/skins/default
chmod 555 /data/data/com.waze/waze/skins/default
find /data/data/com.waze/waze/skins/default -name "*x28*" | xargs rm -rf

chown root:root /data/data/com.waze
chown root:root /data/data/com.waze/preferences
chmod 755 /data/data/com.waze
chmod 644 /data/data/com.waze/preferences 
```

### 第五步

重新启动你的手机，看看广告现在是否被禁用，没有兴趣点出现！所有的广告和兴趣点应该完全禁用。

* * *

## 说明

首先，“99waze”是一个无系统的 init.d 脚本。Init.d 是一个系统文件夹，包含引导时运行的脚本，文件名前面的前两个数字表示优先级。例如，文件名“01file”将在“99file”之前运行。这个脚本被留到最后，这样就不会干扰其他任何东西，也不会在以后撤销它的修改。

不仅优先级被设置到最后，而且脚本以“sleep 30”开始，这意味着在做任何事情之前要等待 30 秒。接下来，脚本调用 Linux 文本流编辑器“sed”。它可以让你通过命令逐行编辑文本文件。Sed 用于替换首选项文件中的许多参数。所有这些都用于广告或兴趣点，并禁用它们。

接下来，我们使兴趣点文件只能由 root(在本例中是超级用户)帐户编辑。这些文件位于上面提到的/skins/default 文件夹中。然后，我们删除所有包含字符串“x28”的文件，因为所有兴趣点文件都包含该字符串。当我们删除它们时，应用程序无法重新创建它们，因为超级用户帐户拥有该文件夹，因此即使首选项更改被撤消，您也无法再接收兴趣点文件。

接下来，脚本声明对首选项文件的根所有权，因此这也不能被编辑。这再次防止我们的更改被撤销，并有助于防止任何未来的应用程序更新撤销我们的更改。

就是这样！Waze 是一个非常有用的应用程序，但令人遗憾的是添加了这样的分散注意力的广告。它们会给司机带来麻烦，而用户找到了绕过它们的方法，这很好。希望有所改变，使广告更少侵扰。虽然在我看来广告可能是有益的，但在用户开车时在应用程序中出现这种侵扰性广告是不可接受的，我希望开发者可以接受这一提示。