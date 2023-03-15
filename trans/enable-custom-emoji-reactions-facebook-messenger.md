# 如何立即在 Facebook Messenger 中启用自定义反应

> 原文：<https://www.xda-developers.com/enable-custom-emoji-reactions-facebook-messenger/>

众所周知，脸书总是和用户一起测试新功能。有些很酷，也很有用，但是，许多经常受到排他性的限制，有些人似乎得到了新特性，而更多的人没有。其中一个功能是自定义反应，脸书说这个功能很快就会出现在 Messenger 平台上。消息反应是快速交流的有趣而有用的方式，但 Facebook Messenger 默认提供的那些并没有涵盖所有的基础。我发现了一种启用它们的方法，你所需要的就是你的电脑，Tampermonkey，和我写的一个脚本。

## 在 Facebook Messenger 中启用自定义反应

首先，你需要安装 Tampermonkey 作为 Chrome 或 T2 Firefox 的扩展。Tampermonkey 是一个扩展，允许你在页面上运行“用户脚本”，这是修改页面的自定义 JavaScript 程序，我们将使用它来实现自定义反应。一旦你安装了 Tampermonkey，点击右上角的扩展并选择 Tampermonkey 图标。你会看到这个屏幕。

单击“创建新脚本”。

接下来，您需要将以下所有代码粘贴到您进入的窗口中。

```

// @grant none

(function() {
 'use strict';

  const heart = '\u2764';
  const clown = '\u{1F921}';

  const heartEncoded = encodeURIComponent(heart);
  const clownEncoded = encodeURIComponent(clown);

  const promptText = `React with:
1: ${heart} (Heart),
2: ${clown} (Clown)`;

  const oldOpen = XMLHttpRequest.prototype.open;

  XMLHttpRequest.prototype.open = function() {
      const query = arguments[1];

      if (query.includes('ADD_REACTION') && query.includes(heartEncoded)) {

      const new_reaction = Number.parseInt(prompt(promptText, '2'));

      if (1 === new_reaction) {
        arguments[1] = query.replace(heartEncoded, heartEncoded);
      } else if (2 === new_reaction) {
        arguments[1] = query.replace(heartEncoded, clown);
      }
    }

    oldOpen.apply(this, arguments);
  }
})(); 
```

点击文件->保存，然后在电脑上重新加载 [Messenger 的网站](http://messenger.com)。**确保你的心脏反应设置为默认的心脏反应，而不是紫心反应。**如果有效，试着用心回复脸书上的一条消息，你会在顶部看到这个提示。

键入“2 ”,您应该会看到您对该消息的反应是一张小丑脸。

接下来，重新启动手机上的 Facebook Messenger，当您尝试回复一条消息时，应该会看到以下内容。

就是这样！

在下面的评论中让我们知道这是否对你有用，或者你是否是已经在 Facebook Messenger 中获得自定义反应的幸运儿之一！