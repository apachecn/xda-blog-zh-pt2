# KTweak 是一个新的 Magisk 模块，用于 Android 内核调整

> 原文：<https://www.xda-developers.com/ktweak-is-a-new-kernel-adjustment-mod-that-optimizes-the-performance-of-android-devices/>

在 XDA，我们喜欢[关注各个 Android OEMs 厂商的内核源代码发布事件](https://www.xda-developers.com/tag/kernel-sources/)。这种实践的操作方式在于，我们优秀的售后市场开发社区经常修补那些库存内核源代码，以[修复现有的 bug](https://www.xda-developers.com/custom-kernel-fix-green-tinting-issues-google-pixel-4-xl-units/)，甚至[添加某种新特性](https://www.xda-developers.com/kirisakura-custom-kernel-for-the-oneplus-8-pro-enables-control-flow-integrity-cfi-for-better-security/)。通用内核映像(GKI)的概念仍然像[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)一样成熟，这就是为什么这种特定于设备的定制内核是在 Android 生态系统中[操作低级硬件参数](https://www.xda-developers.com/unleash-true-performance-red-magic-5g-mod-custom-kernel/)的首选方法。

事实上，Linux 内核本身通过类似于 *sysfs* 和 *procfs* 的伪文件系统公开了许多可调参数。如果你曾经使用过一个[“内核管理器”应用](https://www.xda-developers.com/fk-kernel-manager-becomes-franco-kernel-manager-downloading-any-custom-kernel/)来调整你的 Android 设备的内核，你基本上是在使用一个漂亮的前端 *sysfs* (或者 *procfs* ，这取决于参数)。基于 Android 内核的这一方面，XDA 公认的开发者[tydraco](https://forum.xda-developers.com/member.php?u=8155542)提出了一个独特的 Magisk 模块，名为 **KTweak** ，可以作为一个通用的内核微调器。

据开发者称，Android 内核通常用`CONFIG_SCHED_DEBUG`以及设置为 true 的其他调试选项进行编译，如果你有 root 访问权限，这足以动态调整内核参数。谷歌最终将[为大众带来通用内核映像](https://android-review.googlesource.com/q/GKI+status:merged)，因此从长远来看，切换到设备无关的解决方案，而不是从头开始重新编译特定于设备的内核源代码来达到相同的结果，确实是可行的。

与一些流行的“一闪而过的内核优化器”不同，KTweak 是由 [KISS 原理](https://en.wikipedia.org/wiki/KISS_principle)驱动的。没有一个单独的编译组件，而[实际的代码库](https://github.com/tytydraco/ktweak/blob/master/system/bin/ktweak)(不过是一个 shell 脚本)不到 250 行长。展开下面的列表，查看 KTweak 应用的所有调整:

### KTweak 完成的修改列表

*   kernel.perf _ cpu _ 时间 _ 最大百分比:25 - > 5
*   kernel . sched _ auto group _ enabled:0-> 1
*   kernel . sched _ enable _ thread _ grouping:0-> 1
*   kernel . sched _ child _ runs _ first:0-> 1
*   kernel.sched_downmigrate: 20
*   kernel.sched_upmigrate: 80 80
*   kernel . sched _ group _ down migrate:20
*   kernel . sched _ group _ up migrate:80
*   kernel . sched _ tuned _ scaling:0
*   kernel . sched _ latency _ ns:1000000(10ms)
*   kernel . sched _ min _ granularity _ ns:1000000(1 毫秒)
*   kernel . sched _ migration _ cost _ ns:500000(0.5 毫秒)-> 1000000(1 毫秒)
*   kernel . sched _ min _ task _ util _ for _ boost:25
*   kernel . sched _ min _ task _ util _ for _ co location:50
*   内核迁移:32 - > 64
*   kernel.sched_schedstats: 1 - > 0
*   kernel . sched _ wake up _ granularity _ ns:1000000(1 毫秒)-> 5000000(5 毫秒)
*   kernel.timer_migration: 1 - > 0
*   net.ipv4.tcp_ecn: 2 - > 1
*   net.ipv4.tcp_fastopen: 3
*   net.ipv4.tcp_syncookies: 1 - > 0
*   VM . compact _ unevictable _ allowed:1-> 0
*   VM . dirty _ background _ ratio:5-> 10
*   vm.dirty_ratio: 20 - > 30
*   VM . dirty _ expire _ centisecs:300(3 秒)-> 1000(10 秒)
*   VM . dirty _ write back _ centi secs:500(5s)-> 0(0s)
*   vm.extfrag_threshold: 500 - > 750
*   vm.oom_dump_tasks: 1 - > 0
*   vm.page-cluster: 3 - > 0
*   vm.reap_mem_on_sigkill: 0 - > 1
*   vm.stat_interval: 1 - > 10
*   vm.swappiness: 100 - > 80
*   vm.vfs_cache_pressure: 100 - > 200
*   下一个伙伴
*   没有严格的跳过伙伴
*   没有非任务能力
*   TTWU 队列
*   调速器微调
    *   hispeed_load: 90 - > 80
    *   hispeed_freq
*   CAF CPU 加速调整
    *   输入升压频率:1.4 GHz
    *   输入升压毫秒:250 毫秒
*   输入－输出
    *   iostats: 1 - > 0
    *   预读:0
    *   请求数量:128 - > 512
    *   无/无
*   ZRAM

如果你需要深入了解所有上述调整以及它们如何提高你的 Android 智能手机或平板电脑的性能水平，请前往下面链接的模块讨论线程。所有可调参数和相应的强制值都是由开发人员根据它们对实际使用场景的影响精心选择的，所以您知道这不是骗人的。也欢迎您通过向[模块的 GitHub repo](https://github.com/tytydraco/ktweak) 提交 pull 请求来为项目做出贡献。

**[KTweak 内核调整 Magisk 模块— XDA 下载讨论线程](https://forum.xda-developers.com/android/software/module-ktweak-evidence-t4148447/)**