# 谷歌放弃了底部地址栏“Chrome Home ”,转而采用新的“Chrome Duplex”界面

> 原文：<https://www.xda-developers.com/google-deprecating-bottom-address-bar-chrome-home-chrome-duplex/>

# 谷歌放弃了底部地址栏“Chrome Home ”,转而采用新的“Chrome Duplex”界面

谷歌放弃了底部地址栏的 Chrome Home 功能，转而支持新的 Chrome Duplex 分割工具栏功能。

随着 18:9 显示屏宽高比的智能手机不断发布，我们看到许多应用程序都进行了重新设计，将按钮移到了屏幕底部。一个显著的例子是与谷歌 Pixel 2 一起发布的底部带有搜索栏的 Pixel 启动器。另一个实际上已经进行了相当长时间的例子是“ [Chrome Home](https://www.xda-developers.com/googles-experimental-chrome-home-gets-a-redesigned-new-tab-page/) 实验，它将谷歌 Android Chrome 浏览器的地址栏移到了底部。现在，看起来谷歌正在放弃这个底部地址栏的实验，转而支持一个叫做 **Chrome Duplex** 的新东西。

今天早些时候， [*Android Police*](http://www.androidpolice.com/2018/02/06/google-might-scrapping-plans-chrome-home-bottom-address-bar-interface/) 报道称，谷歌可能会取消 Chrome Home 的实验。该报告引用了对已关闭的错误报告的评论，陈述如下:

> *“我们正在结束当前的 Chrome Home 实验，并关闭相应的 Chrome Home bugs。感谢反馈和支持！”*

此外， *Android Police* 注意到，该功能现在在最新的谷歌 Chrome Dev 和 Canary 版本中被默认禁用(尽管可以通过 chrome://flags 中的功能标志手动启用)。看起来谷歌确实正在摆脱这一功能，这让我们许多拥有更高智能手机(如谷歌 Pixel 2 XL)的人感到失望，因为这将导致你不得不伸出手去够地址栏。

然而，我们在 Chromium gerrit 中发现了一个新的提交,表明谷歌正在用一个名为“Chrome Duplex”的“分割工具栏”Chrome 主页界面取代底部地址栏。

我们还不完全确定这会给用户界面带来什么样的变化，但是一旦最新的 Chromium 版本上线，我们会进行测试并让你知道。作为参考，新的 Chrome 双工功能一旦上线，就可以在`chrome://flags#enable-chrome-duplex`启用。