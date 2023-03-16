# 【更新 2:正在运行】谷歌 Chrome 可能会有自己的直播字幕功能

> 原文：<https://www.xda-developers.com/google-chrome-getting-live-caption-feature/>

**更新 2(美国东部时间 2020 年 6 月 9 日中午 12 点 05 分):**谷歌 Chrome 的金丝雀版本现在可以使用直播字幕了。

**更新 1(美国东部时间 4/21/2020 @ 6:20PM):**在最新的 Chromium 版本中，切换直播字幕的选项现已可用。虽然该功能还不能工作，但它应该很快就会开始处理更多的代码提交，并最终成为稳定的 Google Chrome 版本。

回到去年的 Google I/O，该公司[在 Android 10 中发布了一款名为 Live Caption](https://www.xda-developers.com/google-accessibility-live-caption-android-q-live-relay-live-transcribe/) 的新工具。顾名思义，该工具旨在自动为设备上播放的音频提供字幕。它与视频、播客、音频信息和其他支持的媒体一起工作，使其成为听力受损者的一个很好的辅助工具。最重要的是，该工具还可以用来帮助改善嘈杂环境中的视频观看体验。现在，根据 Chromium Gerrit(via[*Chrome unboxed*](https://chromeunboxed.com/live-captions-chrome-browser-pixel-phones/))上发现的提交，似乎谷歌 Chrome 团队正在努力将该功能引入浏览器。

问题中的[提交是针对 SODA(设备上的语音 API)服务的，这对于在浏览器上获得直播字幕至关重要。提交的描述是，“这个 CL 创建一个沙盒服务，它托管设备上的语音 API (SODA)。它包含从渲染器进程启动服务所需的组件，但是服务本身的实现被剔除。该功能的设计文档位于:go/chrome-live-captions。SODA 是谷歌语音团队制作的第一方产品，将音频转录成文本。设计文档的名称引用了“Live Caption”，Chromium 提交中的几个方法和常量也暗示了这一点。](https://chromium-review.googlesource.com/c/chromium/src/+/2017563)

在其中一条评论中，一名谷歌员工明确地将这一功能与 Android 上的功能进行了比较，他说，“我认为我们应该在使用功能名称来匹配 Android 上的功能时使用‘实时字幕’。”然而，谷歌希望 SODA 不仅仅用于直播字幕，这是基于另一位谷歌人的评论，他说:“根据我们与 ChromeOS 团队的讨论，听起来他们可能希望在未来建立其他语音识别场景。将这种汽水命名的好处是，其他特性可以使用这个组件，尽管它可能被视为一个有漏洞的抽象。”

谷歌目前没有发布任何关于即将到来的功能的信息，但基于上述信息，我们可以有把握地假设，一旦发布，它将非常类似于 Android 10 的 Live Caption 功能。不过，截至目前，该功能仍处于早期开发阶段，在谷歌 Chrome 稳定发布之前，还需要一段时间。

* * *

## 更新 1:谷歌 Chrome 标志

当这篇文章在二月中旬首次发表时，我们只看到了直播字幕功能将进入桌面 Chrome 的暗示。现在，一个[提交被合并](https://chromium-review.googlesource.com/c/chromium/src/+/2158008),带来了谷歌 Chrome 标志。该标志旨在通过在 Chrome 的设置中添加一个易于控制的开关来测试 Canary builds 中的功能。可以通过首先启用 chrome://flags # enable-Accessibility-Live-Captions 中的标志，然后在 Chrome 的可访问性设置中启用“Live Captions”切换来启用该切换。然后可以在 Windows 10 设置中自定义字幕 UI。字幕框也可以在屏幕上移动。目前，标题框只显示一个静态字符串，所以它目前不工作。不过，我们会监控这项功能，并在它开始工作时向您报告。

* * *

## 更新 2:现在工作

直播字幕现在可以在谷歌 Chrome 的金丝雀版本中使用。您必须启用一个标志，并在辅助功能选项中启用该功能。要启用该标志，请进入*# enable-accessibility-live-captions*，将其打开，然后重启 Chrome。之后，你需要进入 Chrome **设置>高级>辅助功能**，切换“直播字幕”您现在可以在浏览器中播放的任何视频上看到字幕。

**来源: [Chrome 故事](https://www.chromestory.com/2020/06/live-captions/)**