# 谷歌浏览器的最新实验旨在提高电池寿命和性能

> 原文：<https://www.xda-developers.com/google-chromes-experiments-designed-improve-battery-life-performance/>

为了提高谷歌 Chrome 的性能，减少其对电池寿命的影响，谷歌正在测试这款浏览器的两个新功能。第一个功能是在 Chromium bug tracker 页面上发现的，它添加了一个新的节省电池的 meta 标签，该标签将优化已知具有高 CPU 或电池成本的网站。一个关于新 meta 标签的解释者说:

*“节省电池或 CPU 对于没有连接到电源的计算设备来说很重要，或者对于在运行的进程之间更好地共享公共 CPU & GPU 资源来说也很重要...已知具有高 CPU 或电池成本的网站可能想要请求 UA 针对 CPU 或电池进行优化，即使用户没有请求...大多数现代操作系统还具有电池节省功能，当电池电量低或用户希望节省电池时，这些功能就会发挥作用。理想情况下，网站应该能够尊重这些设置。营业点可能希望向 UA 建议在这些情况下哪种策略对该方最有效。”*

谷歌 Chrome 中的新 meta 标签将允许网站添加 meta 标签以降低帧速率，允许一般的脚本执行减速，并根据电池节能设置改变行为以延长电池寿命。为了做到这一点，网站将能够添加类似的标签。meta 标签将允许视频或视频会议网站减少 CPU 使用并延长电池寿命，减慢不会直接影响 UX 的 JavaScript 任务，并在用户希望时切换到电池节省模式。

解释者进一步强调了电池节能功能将包含以下组件:

*   允许站点指示首选模式的 meta 标签。
*   媒体查询允许网站根据电池电量的节省来调整它们的样式表。
*   规范文本说明，如果用户或操作系统进入了电池节能模式，那么用户代理应该将一个或多个电池节能应用到站点。
*   规范文本说明 UAs 应该尊重站点上的 meta 标签，除非它与用户或操作系统设置冲突。

第二个功能旨在提高谷歌 Chrome 的性能，仅限于 Android 设备。该功能已被添加到浏览器的一个新标志下，名为*CPU-affinity-restrict-to-LITTLE-cores，*，其描述如下:“将 Chrome 线程限制在大内核设备的小内核上。很少或相似的 CPU 架构。”

根据最近来自 *Chrome Story* 的[报道，该功能有望使 Chrome 在 ARM 设备上更加节能，并提高其性能。这项功能目前处于试验阶段，谷歌正在研究它对功耗、流畅度和其他系统健康指标的影响。因此，我们可能需要等待相当长的时间，才能在浏览器的稳定版本中实现这一功能。](https://www.chromestory.com/2020/08/big-little-processor-chrome/#:~:text=Restrict%20to%20LITTLE%20cores%20%E2%80%93%20Chrome&text=%E2%80%9CRestrict%20to%20LITTLE%20cores%3A%20Restricts,other%20system%20health%20metrics%20etc.)

值得注意的是，这些并不是谷歌为 Chrome 增加的唯一功能，以提高其性能并减少对电池寿命的影响。该公司预计将在 Android 版 Chrome 86 中添加一个[后退前进缓存功能](https://www.xda-developers.com/back-forward-google-chrome-faster-bfcache/)，这将允许用户在浏览器中更快地后退和前进。谷歌也在测试[节流后台 JavaScript 定时器](https://www.xda-developers.com/google-chrome-tests-throttling-background-javascript-timers-improve-battery-life/)，以改善 Chrome 对电池寿命的影响。

* * *

**来源: [Chromium bug 追踪器](https://bugs.chromium.org/p/chromium/issues/detail?id=1114184)， [GitHub](https://github.com/chrishtr/battery-savings/blob/master/explainer.md) ， [Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/2348774)**