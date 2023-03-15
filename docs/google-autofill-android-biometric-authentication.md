# Android 上的谷歌自动填充现在支持生物认证

> 原文：<https://www.xda-developers.com/google-autofill-android-biometric-authentication/>

# Android 上的谷歌自动填充现在支持生物认证

所有 Android 设备上的谷歌自动填充服务现在支持密码和购买的生物认证(指纹、面部)。

早在一月份，我们发现[谷歌正在测试对其第一方自动填充服务的](https://www.xda-developers.com/google-autofill-biometric-authentication-passwords-payments/)生物认证支持。现在，这项功能似乎正在通过最近对 Google Play 服务的更新推出到 Google Autofill 中。

这项新功能意味着用户可以要求成功的生物特征认证，然后才能将信息填入表单。以前，谷歌的自动填充服务在用户锁屏上没有额外的保护措施，这使得它不如大多数第三方密码管理器安全。

根据 *[Android Police](https://www.androidpolice.com/2020/08/20/google-autofill-on-android-can-require-biometric-authentication-now/)* 的说法，该功能似乎已经广泛适用于 Google Play 服务 v20.33.13 的用户，但它也适用于 v20.26.14 版本的一些用户。这似乎是通过服务器端更新推出的，所以只需等待一个标志在你的设备上翻转。

新功能可以通过前往**设置>谷歌>自动填充>用谷歌**自动填充找到。你会看到一个名为**自动填充安全**的新菜单，在这里你可以切换生物特征。一旦切换，用户就可以使用 BiometricPrompt API 支持的任何生物认证硬件，包括指纹扫描仪、虹膜扫描仪或安全面部识别硬件，如 [Pixel 4](https://forum.xda-developers.com/pixel-4) 和 [Pixel 4 XL](https://forum.xda-developers.com/pixel-4-xl) 上的硬件。当然，你还需要在设置>系统>语言&输入>自动填充服务中打开谷歌自动填充服务。

添加生物认证不仅使登录更加安全，而且使用户登录更加方便。