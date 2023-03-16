# 骁龙三星 Galaxy S9 和 Note 9 现在可以通过 exploit 进行 rooted

> 原文：<https://www.xda-developers.com/samsung-galaxy-s9-galaxy-note-9-snapdragon-root/>

众所周知，在美国销售的三星手机很难找到根源。Samsung Knox 让 root 变得特别烦人，如果你设法找到了 root，它往往会破坏很多东西。美国用户甚至无法在第一时间解锁 bootloader 来 root 他们的设备。然而，每隔一段时间，开发人员就会想出一个让我们扎根的漏洞。例如，[骁龙 Galaxy S7](https://www.xda-developers.com/att-galaxy-s7-has-finally-been-rooted/) 、[骁龙 Galaxy S8](https://www.xda-developers.com/sampwnd-root-galaxy-s8-snapdragon/) 和[骁龙 Galaxy Note 8](https://www.xda-developers.com/samsung-galaxy-note-8-root-samfail/) 都有可能利用漏洞进行根源攻击。S8/Note 8 的 SamPWND 漏洞背后的同一批开发人员再次利用骁龙 Galaxy S9、Galaxy S9+和 Galaxy Note 9 上的 root 访问权限，尽管有一个问题。

**[三星 Galaxy S9 XDA 论坛](https://forum.xda-developers.com/galaxy-s9)| |[三星 Galaxy S9+ XDA 论坛](https://forum.xda-developers.com/galaxy-s9-plus)** **[三星 Galaxy Note 9 XDA 论坛](https://forum.xda-developers.com/galaxy-note-9)**

问题是，骁龙 Galaxy S9、Galaxy S9+和 Galaxy Note 9 需要在设备上安装特定的 Android 版本。此时，Root 不可用于最新固件上的设备。目前，如果你运行的是 Android 8.0 或 8.1 奥利奥，你只能 root 骁龙 Galaxy S9、Galaxy S9+和 Galaxy Note 9。这是目前基于 Android 10 发布的两大版本 Android 的背后。你还需要运行所谓的组合固件——三星在工厂用于测试的固件。组合固件是 root 成为可能的唯一原因，但它也有自己的限制:不幸的是，刷新它会将电池充电限制在最高 80%。另一方面，三星 Knox 仍然在工作(因为你没有解锁引导加载程序)，所以像 Secure Folder 或 Samsung Pay 这样的应用程序继续工作。此外，在软件修改可能导致保修失效的国家，您可以保留保修。

Galaxy S9、Galaxy S9+和 Note 9 的 root 方法的另一个特点是，它不使用 Magisk，这意味着这不是无系统的 root。取而代之的是使用 SuperSU。由于引导加载程序仍然被锁定，因此无法为 Magisk 的工作修补引导映像。因此，借助 SuperSU，我们可以获得完全基于系统的根本解决方案。不幸的是，这也意味着安全网认证不会通过，这意味着像 Google Pay 和 Pokémon Go 这样的应用程序将无法工作。

更重要的是，由于 Safestrap 导致内核崩溃，也没有可用的 TWRP。您还需要在每次启动手机时使用特定的按键组合，以确保禁用写保护。幸运的是，你可以安装 [Xposed 框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)。考虑到过多的模块，这允许很多功能和定制。虽然大多数定制的 rom 因为锁定的引导程序而不能刷新，但是安装一个 GSI 是可能的。开发人员已经在 Galaxy S9+上测试并启动了一台 AOSP Android 9 Pie GSI，如下所示。

你需要的所有说明都已经在下面链接的论坛帖子里发布了。这个过程需要一些 Odin 闪烁，同时从你的电脑和 FlashFire 应用程序中运行一些脚本。论坛帖子中还链接了闪烁 GSI 的说明。

**[Root for Galaxy S9(G960U/U1)](https://forum.xda-developers.com/galaxy-s9/samsung-galaxy-s9--s9-snapdragon-roms-kernels-recoveries--other-development/root-t4041815/post81608559#post81608559)| |[Root for Galaxy S9+(G965U/U1)](https://forum.xda-developers.com/galaxy-s9/samsung-galaxy-s9--s9-snapdragon-roms-kernels-recoveries--other-development/root-t4043707/)| |[Root for Galaxy Note 9(N960U/U1)](https://forum.xda-developers.com/galaxy-note-9/samsung-galaxy-note-9-snapdragon-roms-kernels-recoveries--other-development/root-extreme-syndicate-t4043723)**

我们想对极端辛迪加根项目背后的开发者们大声疾呼。Team Syndicate 由 XDA 公认开发者/退役论坛版主 [elliwigy](https://forum.xda-developers.com/member.php?u=3812611) ，公认贡献者 [jrkruse](https://forum.xda-developers.com/member.php?u=1949695) ，资深会员 [klabit87](https://forum.xda-developers.com/member.php?u=4168602) ，资深会员 [me2151](https://forum.xda-developers.com/member.php?u=4591212) ，会员 [GSM-CHEN](https://forum.xda-developers.com/member.php?u=425309) 组成。他们都花了无数的时间来获得这些设备的 root 访问权限。