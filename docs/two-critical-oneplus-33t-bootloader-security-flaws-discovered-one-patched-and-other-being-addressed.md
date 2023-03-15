# [更新:第二个漏洞已修补]发现两个严重的 OnePlus 3/3T 引导加载程序安全漏洞，一个已修补，另一个正在解决

> 原文：<https://www.xda-developers.com/two-critical-oneplus-33t-bootloader-security-flaws-discovered-one-patched-and-other-being-addressed/>

自本文发表以来，Oxygen OS 4 . 0 . 3 版本已经修补了本文讨论的第二个安全漏洞，即 dm-verity 漏洞。

在进入 Android 生根、定制 rom、内核和其他修改的奇妙世界之前，您首先必须解锁设备上的引导加载程序。

在一些设备上(尤其是运营商品牌的设备)，这造成了一个问题，因为用户必须在解锁引导加载程序之前处理重大的技术障碍。华为手机等其他设备要求你向原始设备制造商申请一个独特的引导加载程序解锁代码——这是一个小小的障碍，但并不十分困难。更好的是谷歌 Nexus/Pixel 系列或一加手机，它们只需要你在开发者设置中勾选一个选项，然后发送几个*快速启动*命令。

但是不管解锁你的引导程序有多难，有一件事是永远不变的:解锁后擦除设备的要求。这样做是出于明显的安全原因，因为一旦 bootloader 解锁，您的整个数据分区就可以很容易地被提取出来。如果恶意实体(拥有技术知识)能够访问您的数据，他们可以快速启动自定义恢复并提取您设备的完整备份。这就是为什么解锁您的引导加载程序被认为是一个安全风险，也是为什么您的设备在解锁后会被擦除。假设一切正常，普通用户应该不会被攻击者解锁引导加载程序来绕过标准的 Android 锁定方法。然而，并非一切都按计划进行。

* * *

## OnePlus 3/3T 引导加载程序解锁漏洞

Roee Hay([@ roe Hay](https://twitter.com/roeehay))刚刚披露了一组新的漏洞[，其中第一个漏洞允许 OnePlus 3/3T 的引导加载程序解锁**，无需用户确认，也无需触发工厂重置。**这个标记为](https://securityresear.ch/2017/02/08/oneplus3-bootloader-vulns/#exploiting-cve-2017-5626-for-kernel-code-execution) [CVE-2017-5625](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5626) 的漏洞被认为是一个严重漏洞，它会影响所有运行 OxygenOS 3.2-4.0.1 的 OnePlus 3/3T 设备。已经升级到 [incremental OxygenOS 4.0.2](https://forums.oneplus.net/threads/oxygenos-4-0-2-n-ota-for-oneplus-3.489599/) 更新**的用户不会受到这个漏洞的影响**，因为 Hay 先生在 1 月 23 日私下向一加**透露了这个缺陷，所以他们可以立即修补这个问题。**

该漏洞通过发送专有的隐藏快速启动命令:`fastboot oem 4F500301`来工作。通过发送该命令，绕过用户的引导加载程序锁定状态(即使在开发者设置中没有启用“允许 OEM 解锁”时)。设备不会提示用户，也不会像应该的那样擦除设备——事实上，设备仍然会报告引导加载程序被锁定！另一个快速引导命令`fastboot oem 4F500302`将重置一些引导程序设置，并可用于锁定已经解锁的设备。

Hay 先生发现，第一个快速启动命令设置了他所谓的“ **magicFlag** ”，它覆盖了在执行闪存或擦除命令时确定引导加载程序锁定状态的检查。

```

int sub_918427F0()
{
  magicFlag_dword_91989C10 = 1;
  if ( dword_9198D804 != dword_9198D804 )
    assert(1, dword_9198D804, dword_9198D804);
  return sendOK((int)"", dword_9198D804);
}

```

### 快速启动闪存处理程序

```

const char *__fastcall sub_91847EEC(char *partitionName, int *a2, int a3)
{
  char *pname; 
...
  pname = partitionName;
  v4 = a2;
  v5 = a3;
  if ( returnTRUE1(partitionName, (int)a2) )
  {
    result = (const char *)sub_918428F0(pname, v6);
    if ( (result || magicFlag_dword_91989C10)
      && ((result = (const char *)sub_91842880(pname, v10)) != 0 || magicFlag_dword_91989C10) )
    {
      result = (const char *)sub_918428F0(pname, v10);
      if ( !result || magicFlag_dword_91989C10 )
        goto LABEL_7;
      v8 = dword_9198D804;
      if ( dword_9198D804 != dword_9198D804 )
        goto LABEL_28;
      v11 = "Critical partition flashing is not allowed";
    }
    else
    {
      v8 = dword_9198D804;
      if ( dword_9198D804 != dword_9198D804 )
        goto LABEL_28;
      v11 = "Partition flashing is not allowed";
    }
    return (const char *)FAIL2((int)v11, v10);
  }
LABEL_7:
  ...
    if ( *v4 != 0xED26FF3A )
    {
      if ( *v4 == 0xCE1AD63C )
        cmd_flash_meta_img(pname, (unsigned int)v4, v5);
      else
        cmd_flash_mmc_img(pname, (int)v4, v5);
      goto LABEL_10;
    }
    v7 = v4;
  }
  cmd_flash_mmc_sparse_img(pname, (int)v7, v5);
  ...
 }

```

### Fastboot Erase 指令

```

int __fastcall sub_91847118(char *partitionName, int a2, int a3)
{
 ...
  v3 = partitionName;
  v4 = returnTRUE1(partitionName, a2);
  if ( !v4 )
  {
LABEL_7:
    ...
    if ( v4 )
    {
      if ( dword_9198D804 == dword_9198D804 )
        return eraseParition(v3);
    }
    ...
  }
  v4 = sub_918428F0(v3, v5);
  if ( !v4 && !magicFlag_dword_91989C10 )
  {
    v6 = dword_9198D804;
    if ( dword_9198D804 == dword_9198D804 )
    {
      v7 = "Partition erase is not allowed";
      return FAIL2((int)v7, v5);
    }
    goto LABEL_23;
  }
  v4 = sub_91842880(v3, v5);
  if ( !v4 && !magicFlag_dword_91989C10 )
  {
    v6 = dword_9198D804;
    if ( dword_9198D804 == dword_9198D804 )
    {
      v7 = "Partition flashing is not allowed";
      return FAIL2((int)v7, v5);
    }
LABEL_23:
    assert(v4, v5, v6);
  }
  v4 = sub_918428F0(v3, v5);
  if ( !v4 || magicFlag_dword_91989C10 )
    goto LABEL_7;
  v6 = dword_9198D804;
  ...
  v7 = "Critical partition erase is not allowed";
  return FAIL2((int)v7, v5);
}

```

CVE-2017-5626 可以用来**执行内核代码**。攻击者可以刷新他们想要的任何启动映像。但是，如果他们刷新一个修改过的引导镜像，验证过的引导就会启动，并警告用户已经检测到修改。有一种方法可以绕过这个问题，那就是刷新一个旧的、未修改的启动映像——一个包含旧的漏洞的映像，这些漏洞已经被打了补丁。即便如此，您得到的“警告”仅持续 5 秒钟，它会自动解除自身并引导至 verifiedboot 状态，攻击者的代码仍将在该状态下执行。

Hay 先生提到有很多方法可以恶意利用这个缺陷。例如，他修改了一个引导映像，将 SELinux 模式设置为*许可*，并在引导时自动包含 ADB 访问。然后，在利用这个漏洞刷新他修改过的启动映像后，他能够在用户输入他们的凭证之前访问一个**根 shell。**

```
 OnePlus3:/ 
uid=0(root) gid=0(root) groups=0(root),1004(input),1007(log),1011(adb),
1015(sdcard_rw),1028(sdcard_r),3001(net_bt_admin),3002(net_bt),
3003(inet),3006(net_bw_stats),3009(readproc) context=u:r:su:s0

OnePlus3:/ 
Permissive

```

不用说，这是相当严重的。您认为由于您的典型安全措施而安全的被盗或被屏蔽的设备可以使用此漏洞完全击败。

* * *

## OnePlus 3/3T SELinux 漏洞

第二个漏洞，标记为 [CVE-2017-5624](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5624) ，影响**oxygen OS**的所有版本，并允许**禁用 dm-verity。**Hay 先生于 1 月 16 日**向一加安全团队披露了该漏洞，但需要注意的是，XDA 资深会员 [th3g1z](https://forum.xda-developers.com/member.php?u=3878912) [于 1 月 23 日**独立发现该漏洞**](https://forum.xda-developers.com/showpost.php?p=70698410&postcount=112)**。我们与一加进行了对话，他们已经确认他们已经承认并将在未来的更新中修复第二个漏洞。****

 ****这种攻击执行起来也相当简单。只需发出一个快速启动命令就可以禁用(或启用)dm-verity: `fastboot oem disable dm-verity`。要启用它，只需发出`fastboot oem enable dm-verity`。该命令的处理程序取自引导装载程序的转储，如下所示。

```

int sub_9183B8EC()
{
  int v0; 
  int v1; 

  dmVerity_dword_91960740 = 0;
  v0 = sub_91845E10("ANDROID-BOOT!");
  if ( dword_9198D804 != dword_9198D804 )
    assert(v0, v1, dword_9198D804);
  return sendOK((int)"", v1);
}

```

发出这个命令将设置一个标志，Hay 先生称之为 dmVerity，引导装载程序使用它来发送一个内核命令行参数，该参数可以启用或禁用 dm-verity。

这可以与第一个漏洞结合使用，在未经用户同意的情况下在 OnePlus 3/3T 上执行高度特权代码，并访问用户的数据。例如，Hay 先生能够将一个应用程序安装到/system/priv-app，这使得该应用程序被添加到 priv-app 域。这使得恶意应用程序能够访问设备上的高特权功能。在下面的视频中，Hay 先生展示了这两种漏洞被同时利用的情况。如您所见，当他启动设备时，他构建的应用程序显示为已经预装。

* * *

## 一加的结论和说明

这两个安全漏洞的潜在滥用是可怕的。我们赞扬海先生私下里如此迅速地向一加披露了这些漏洞。尽管如此，我们还是忍不住对这些设备上可以使用这样的快速启动命令感到担忧。当我们编写如何[发现隐藏的快速启动命令](https://www.xda-developers.com/how-to-discover-hidden-fastboot-commands/)的指南时，我们的意图是告诉用户，他们可以使用一些有趣的命令来增强他们的体验。**我们从来没有想到如此高特权的命令会存在于引导程序代码中**。至于**“为什么”**这些快速启动命令包含在固件中，我们得到的是**“无可奉告。”**

目前，如果你没有在每个 Oxygen OS 版本发布后立即更新 OnePlus 3/3T，我们建议你立即更新。更新到 Oxygen OS 4.0.2 将保护你免受第一个漏洞的攻击，但我们必须等到一加推出修补第二个漏洞的更新后，才能说你完全安全免受这些攻击。我们将不得不在未来继续关注这种利用。

* * *

[**来源:roe 有**](https://securityresear.ch/2017/02/08/oneplus3-bootloader-vulns/#exploiting-cve-2017-5626-for-kernel-code-execution)****