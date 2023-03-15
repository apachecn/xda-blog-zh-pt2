# 谷歌浏览器为加载速度快的网站添加了“快速页面”标签

> 原文：<https://www.xda-developers.com/google-chrome-85-fast-page-label/>

在过去的几个月里，谷歌已经推出了 Chrome 开发者工具，以减少页面加载时间，实现安全浏览，并建立类似于原生应用的体验。现在，[公司正在引入](https://blog.chromium.org/2020/08/highlighting-great-user-experiences-on.html)一项突出高质量网络用户体验的功能。从 Android 的 Chrome 85 测试版开始，谷歌将在上下文菜单中标记指向“快速页面”的链接。当一个网页被标记为快速，这意味着用户导航到它有一个“特别好的体验”

谷歌表示，来自一个网站的具有相似结构的 URL 的历史数据在标记时被聚集在一起。当所收集的关于 URL 的数据不足以评估速度或尚不可用时，例如当 URL 是新的或不受欢迎的时，在逐个主机的基础上评估该历史数据。

这项新功能是谷歌 [Web Vitals](https://www.xda-developers.com/google-announces-web-vitals-initiative/) 计划的一部分，该计划“测量网络可用性的各个方面，如加载时间、响应能力和内容加载时的稳定性，并为这些指标定义阈值，以设定提供良好用户体验的标准。”据谷歌称，当开发者做出改变使网页加载更快时，网站将会看到可用性的提高和参与度的增加。

尽管谷歌计划“随着核心网络生命体征的演变保持一致”，但该公司表示，开发者应该预计“核心网络生命体征的定义和阈值是稳定的”，并认识到为该计划进行优化需要投资。为此，该公司已经更新了其[开发者工具](https://web.dev/vitals-tools/)，如[灯塔](https://developers.google.com/web/tools/lighthouse)、[开发工具](https://developers.google.com/web/tools/chrome-devtools)、[页面速度洞察](https://developers.google.com/speed/pagespeed/insights/)和[搜索控制台](https://support.google.com/webmasters/answer/9205520)，以提供信息和建议。

截至目前，快速页面标记正在向 Chrome 85 beta 推出，但你可以通过进入“chrome://flags”并启用“上下文菜单性能信息和远程提示获取”来手动打开它一旦该功能推出，用户将在 Lite 模式下或打开“[让搜索和浏览更好](https://support.google.com/chrome/answer/9116376?co=GENIE.Platform%3DAndroid&hl=en)”选项时看到标签。

除了给网页贴上快速标签之外，谷歌[今年早些时候](https://www.xda-developers.com/google-search-page-experience-ranking/)表示，最快明年将开始根据“页面体验”对网站进行排名。如果搜索巨头认为人们不喜欢使用一个网站，它在搜索结果中的排名就不会很高。