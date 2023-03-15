# 如何自动检查一个下载的 MD5 总和！

> 原文：<https://www.xda-developers.com/how-to-automatically-check-the-md5-sum-of-a-download/>

早在三月中旬，我们就花了[整整一周](http://www.xda-developers.com/xda-tasker-week-in-review/)的时间来介绍许多你可能从未在其他地方见过的令人敬畏的 Tasker 提示和技巧，以最好地增强你的智能手机的效用。希望您已经通过一些真实的例子了解了如何使用 Tasker。

今天，我给你们带来了一个我想出的新主意，这个主意应该会让我们论坛上的许多 flash 爱好者高兴。

如果你是一个喜欢通过刷新自定义 rom、内核等来控制自己设备的用户，那么你很可能是一个从 AndroidFileHost.com 等网站下载大量文件的人。你会注意到，像这样的托管网站上的每一个文件都包含 MD5 总和，供你下载完成后进行比较。

 <picture>![Oops](img/65d73f37811f6ca58d04ddf4a56bed26.png)</picture> 

Oops

在闪存关键文件(如收音机或引导程序)之前，比较 MD5 和非常重要，以确保您没有闪存损坏的文件。但是在移动设备上这样做很麻烦，因为你需要在你的文件浏览器应用程序中手动找到该文件，并将 MD5 总和复制/粘贴到一个文本框中，以便比较总和。

我停下来，心想，为什么不用 Tasker 来实现自动化呢？我查了一下，惊讶地发现在任何地方都没有提到这一点，但这是可能的，而且实际上很容易做到！

**如何完成**

工作原理:你在下载之前将 md5 和复制到你的剪贴板，然后当下载完成时，你被提示是否要比较值。如果您按“是”，Tasker 将计算下载文件的 MD5 总和，并将其与您的剪贴板中的内容进行比较。

* * *

**先决条件**

*   [通知监听器](https://play.google.com/store/apps/details?id=com.balda.notificationlistener&hl=en) 或[自动通知](https://play.google.com/store/apps/details?id=com.joaomgcd.autonotification&hl=en)。我个人使用自动通知，但为了本教程的缘故，我设置它使用通知监听器，因为它是免费使用的。
*   [Snackbar Tasker 插件](https://play.google.com/store/apps/details?id=com.nick.mowen.sceneplugin&hl=en)。不需要(虽然如果你导入我的个人资料，它会使用它)，但它比创建一个有按钮的场景要好。我已经将教程设置为只使用应用程序的免费功能。

* * *

**指令**

*   创建一个新的概要文件，并将其命名为' **Check MD5 Sum** s。'关于上下文，请转到**事件- >插件- >通知监听器**。选择“已发布”，向下滚动并选择您的浏览器应用。我个人使用 Chrome Dev，所以我选择了它。
*   **任务- >如果**。如果%nltext ~下载完成，则将其设置为。(或者当你的浏览器应用程序告诉你下载已经完成时，你的通知中的任何子文本。)这是为了当任务检测到下载已经完成时触发，如浏览器通知所指示的。
*   **插件- > Snackbar Tasker 插件**。选择“底部表单”对于标题，可以写成类似“检查 MD5 总和？”，对于项目，将其设为“是，否”，对于命令，将其设为“是，否”。
*   **任务- >如果**。设置为 If %bs_command ~ Y。
*   **代码- >运行外壳**。对于代码 make it `ls /sdcard/Download`设置它在%files 中存储结果。(将/sdcard/后面的内容更改为下载文件夹的路径。/sdcard/Download 是大多数人的默认)
*   **变量- >变量拆分**。分割%个文件。
*   **变量- >数组弹出**。弹出%files，位置 1，并将其设置为%download。
*   **代码- >运行外壳**。对于代码 make it `md5sum /sdcard/Download/%download`将其设置为将结果存储在%md5 中。同样，根据需要更改下载目录。
*   **变量- >变量拆分**。分割%md5。不要设置分割器。
*   **警报- >闪光**。文本:“MD5 总和匹配！”检查 If 并将其设置为 If %md51 ~ %CLIP。
*   **警报- >闪光**。文本:“MD5 总和不匹配！”检查 If 并将其设置为 If %md51！~ %剪辑。
*   **任务- >结束如果。**
*   **任务- >如果**结束。

以下是任务编辑器屏幕截图，让您更好地了解操作顺序:

对自己导入 XML 感兴趣吗？[在我们的 Tasker Tips &技巧论坛中，点击链接](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-automatically-check-md5-sum-t3365590/post66531924#post66531924)到我的帖子，滚动到文件的附件。要导入它，打开 Tasker，长按顶部的 profiles 选项卡，按 import，然后浏览到您下载的. prf.xml 文件。

* * *

有一个你一直想在 Tasker 中实现但不知道如何实现的想法？请在下面告诉我们，我们将来可能会为您的想法提供解决方案！