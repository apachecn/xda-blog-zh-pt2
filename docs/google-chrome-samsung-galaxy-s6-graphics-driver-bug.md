# 三星 Galaxy S6 的图形驱动程序漏洞如何泄露谷歌 Chrome 标签数据

> 原文：<https://www.xda-developers.com/google-chrome-samsung-galaxy-s6-graphics-driver-bug/>

早在 3 月下旬，一家专门测试 GPU 可靠性的英国初创公司向我们提出了一个 [GPU 漏洞，他们发现](https://www.xda-developers.com/the-snapdragon-samsung-galaxy-s9-has-a-gpu-stability-bug-that-can-be-exploited-to-trigger-remote-reboots/)会导致[高通骁龙 845](https://www.xda-developers.com/tag/qualcomm-snapdragon-845/) [三星 Galaxy S9](https://forum.xda-developers.com/galaxy-s9) / [S9+](https://forum.xda-developers.com/galaxy-s9-plus) 在访问网页时重新启动。这家名为 *[GraphicsFuzz](https://www.graphicsfuzz.com/)* 的公司和我们一起向[高通](https://www.xda-developers.com/tag/qualcomm/)和[三星](https://www.xda-developers.com/tag/samsung/)报告了这个问题。我们的一些读者有兴趣了解像 *GraphicsFuzz* 这样的公司如何能够找到这些漏洞，所以我们与该公司合作，展示他们如何发现一个更老的 GPU 漏洞。这个已经打了补丁的漏洞允许攻击者远程“窥探”在[三星 Galaxy S6](https://forum.xda-developers.com/galaxy-s6) 上[谷歌 Chrome](https://www.xda-developers.com/tag/google-chrome/) 浏览器标签的内容。

*该用户在访问恶意网页之前正在查看他们银行的网站。内容被捕获并上传到远程服务器。来源: [GraphicsFuzz](http://www.graphicsfuzz.com/) 。*

## GraphicsFuzz 如何发现 GPU bugs

图形驱动程序通过获取着色器程序并将其发送到 GPU 来执行，从而渲染图像。在将着色器发送到 GPU 之前，图形驱动将其翻译成 GPU 可以理解的形式；错误的翻译会导致渲染失败、程序或设备崩溃、错误的图像，甚至安全问题。 *GraphicsFuzz* 有一个[自动化测试套件](https://www.graphicsfuzz.com/howitworks.html)，允许他们根据一组参考着色器来找到这些 bug。当用户[运行他们的测试](http://www.graphicsfuzz.com/benchmark/android-v1.html)时，所有结果图像看起来都应该是一样的。任何看起来不同的图像意味着有一个错误。

*几款流行设备运行 GraphicsFuzz 测试套件的结果。三星 Galaxy S6、三星 Galaxy S7 和三星 Galaxy S8 包含在这些图表中。来源: [GraphicsFuzz](http://www.graphicsfuzz.com/) 。*

对于三星 Galaxy S6， *GraphicsFuzz* 发现其中一行中的图像显示了本应在另一个表格中的图像。这意味着早期测试的图像会泄漏到后来的测试中。该团队随后在谷歌 Chrome 中重新运行测试套件，发现网页的部分内容出现在图像中。此外，他们发现打开另一个标签会导致图像显示其他标签的部分内容。本质上，这个 bug 允许一个谷歌 Chrome 标签泄露另一个 Chrome 标签的信息！ *GraphicsFuzz* 背后的团队并非有意寻找安全漏洞，但他们最终在测试中发现了一个漏洞。(应该指出的是，该团队在 Galaxy S6 和 [Mozilla Firefox](https://www.xda-developers.com/tag/firefox/) 上重现了三星浏览器的漏洞。)

## 窃听器是如何工作的

*用来触发三星 Galaxy S6 长期运行的 bug 的图片。来源: [GraphicsFuzz](http://www.graphicsfuzz.com/) 。*

由 *GraphicsFuzz* 创建的“恶意”网页使用 WebGL 试图在画布内绘制一个空间场景，如上图所示。每个像素的颜色由片段着色器(fragment shader)确定，片段着色器是网页提供的在 GPU 上执行的程序。 *GraphicsFuzz* 框架修改了片段着色器，这使得它运行了很长时间。当着色器运行时间过长时，浏览器或操作系统通常会中止渲染。然而，虽然 GPU 在绘制了几个像素后中止了渲染，但 GPU 驱动程序没有向谷歌 Chrome 报告这一点。(如果你看一看文章顶部显示垃圾视频内存的图像，你实际上可以在左上角看到太空场景的一部分。)这意味着中止之前渲染的像素保持不变，意味着最终渲染的图像大部分是垃圾视频内存。因为视频存储器被连续地用于呈现其他网页，所以“垃圾”数据实际上包含其他网页的先前呈现。因此，其他网页最终显示在“恶意”网页上。至关重要的是，WebGL 允许网页捕捉正在呈现的任何内容；然后，该图像被上传到远程服务器。

*解释导致 Chrome 标签数据“泄露”的长期 GPU 错误的图表来源: [GraphicsFuzz](http://www.graphicsfuzz.com/) 。*

谷歌 Chrome 使用多个进程，因此不同的标签通常是隔离的，这使得这种利用从表面上看似乎是不可能的。然而，Chrome 使用单个“GPU 进程”与 GPU 进行交互，这意味着所有标签共享相同的 GPU 内存，从而允许这种利用发挥作用。上图更详细地展示了这一点。

在这段视频的前 22 秒中，我们演示了这个 bug。还演示了 GraphicsFuzz 发现的其他安全问题。

## 要吸取的教训

一个行为不端的 GPU 可以绕过谷歌 Chrome 和 Android 的所有安全措施，因为 WebGL 允许任何恶意网页向 GPU 发送代码以供执行。由于谷歌不控制硬件和驱动程序，它无法修复 GPU 的错误。在这种情况下，由 GPU 供应商(在这种情况下，ARM)来修复漏洞，其设备受到影响的 OEM(在这种情况下，三星)来将修复集成到更新中。再加上运营商，很容易看到像这样的漏洞需要很长时间才能修复——大多数三星 Galaxy S6 用户至少花了**5 个月**才收到补丁。

*GraphicsFuzz* 帮助 GPU 厂商发现难以检测的 bug，比如导致错误代码在 GPU 上生成和执行的误编译 bug。他们的自动化测试框架允许他们发现本文中展示的错误。由“恶意”网页引起的长时间循环也已被证明会在其他设备上引起问题，如 [HTC One M7](https://medium.com/@afd_icl/hey-a-web-page-just-restarted-my-phone-c06d3db76542) 和最近的[三星 Galaxy S9](https://www.xda-developers.com/the-snapdragon-samsung-galaxy-s9-has-a-gpu-stability-bug-that-can-be-exploited-to-trigger-remote-reboots/) 。 *GraphicsFuzz* 测试旗舰智能手机并发布[结果表](http://www.graphicsfuzz.com/#results)，根据这些设备在测试子集上的性能对其进行排名。**在他们的测试中已经发现了数百个崩溃和渲染错误**，但是大多数没有被调查，以查看它们是否构成安全威胁。然而，正如这个漏洞所示，行为不端的 GPU 是一个安全风险，有可能一个或多个关键的安全漏洞正在等待被发现。 *GraphicsFuzz* 希望 GPU 厂商未来优先提高驱动质量。

*显卡驱动程序的相对可靠性，按问题总数排序。来源: [GraphicsFuzz](http://www.graphicsfuzz.com/#results) 。*

## 披露时间表

*   2016 年 12 月， *GraphicsFuzz* 向[谷歌 Chromium bug 追踪器](https://bugs.chromium.org/p/chromium/issues/detail?id=675658#c39)报告了这个 bug，因为它符合 Chrome 奖励计划的条件。GraphicsFuzz 将该 bug 提交给谷歌 Chromium bug tracker 后，该 bug 被谷歌接受，并转发给 ARM 和三星打补丁。
*   谷歌[将报告](https://bugs.chromium.org/p/chromium/issues/detail?id=675658#c7)转发给 ARM 和三星的联系人。
*   三星默默地修补了这个漏洞，并在 2017 年 3 月至 6 月发布的 Android 7.0 牛轧糖更新中推出了修复程序。虽然没有三星、谷歌或 ARM 创建的 CVE，三星和 ARM 也没有发布任何关于该补丁的信息，但请注意 *GraphicsFuzz* 没有通过[适当的流程](https://security.samsungmobile.com/securityReporting.smsb)报告该错误。
*   后来， *GraphicsFuzz* 能够确认三星和 ARM 都看到了该报告，并且 ARM 能够根据该报告修复该问题。
*   2017 年 8 月， *GraphicsFuzz* 因漏洞报告被谷歌奖励 2000 美元。
*   2017 年 11 月，[bug 报告公开](https://bugs.chromium.org/p/chromium/issues/detail?id=675658#c39)。