# Developer dual-boots Windows 11 on the Microsoft Surface Duo

> 原文：<https://www.xda-developers.com/windows-11-dual-boot-on-microsoft-surface-duo/>

Many of you probably dual-boot your PCs - be it to [run a Linux distribution alongside Windows](https://www.xda-developers.com/dual-boot-windows-11-linux/) or because you have a Mac and want to play some games through Windows. On traditional x86 computers, the process has gotten relatively simpler over time. On Android, however, the story is different.

The modern x86 platform usually provides a truly OS-independent boot solution in the form of the Unified Extensible Firmware Interface (UEFI), which replaces the legacy Basic Input/Output System (BIOS). This is why you can simply take a bootable installation media and boot from it on your PC to install a new OS. However, when it comes to the Android ecosystem, the boot solutions (UBoot, Little Kernel, etc.) are coupled to the OS. As a result, there is no one-click solution for multi-booting and you must hack around the low-level bootloader stuff to be able to boot a non-Android OS like Windows on an Android device.

Lucky for us, there are extremely talented people who are relentlessly trying to simplify the quest. The first-generation [Microsoft Surface Duo](https://www.xda-developers.com/microsoft-surface-duo-review/) is the latest hurdle cleared by the modding community, as you can now install Windows 11 besides the factory-installed Android OS on this foldable.

## Install Windows 11 on the Microsoft Surface Duo

Gustave Monce, aka XDA Senior Member [gus33000](https://forum.xda-developers.com/m/gus33000.7651894/) is the lead developer behind this impressive achievement. Monce, who has a long-standing reputation for [booting Windows on otherwise incompatible devices](https://www.xda-developers.com/windows-11-on-lumia-950-xl-raspberry-pi-4/), gave us the first glimpse of booting Windows on the OG Surface Duo back in February. Thanks to his formidable skills and open-sourced development, anyone can now boot Windows on Microsoft's inaugural Android-powered foldable smartphone.

Keep in mind that the steps described below are intended for both the unlocked and the AT&T models of the Surface Duo. The Qualcomm Snapdragon 888-powered Surface Duo 2 isn't at all compatible with this mod.

**Warning:** Before we get into how to dual-boot Windows 11 on the Microsoft Surface Duo, remember to take an off-device backup. That’s because the process **requires wiping all the data on your phone, including the files on the internal storage**. You may **permanently brick your device**, so only attempt this if you know what you're doing.

* * *

### Step 1 – Download Windows 11

The Microsoft Surface Duo uses an ARM64 processor, hence we need to get our hands on an ARM64 variant of the Windows 11 installer. Unfortunately, Microsoft doesn't offer an official ARM64 ISO, while the [official VHDX release for Insider Preview users](https://www.microsoft.com/en-us/software-download/windowsinsiderpreviewARM64) isn't suitable for installation on a physical device.

Don't worry, though, as we can use third-party tools to download Microsoft's Unified Update Platform files and prepare the ARM64 installer ourselves. The [UUP dump project](https://uupdump.net/) provides extensive resources to get started with this domain. Alternatively, use Monce's cross-platform [UUP Media Creator](https://github.com/gus33000/UUPMediaCreator) tool to create the ISO.

* * *

### Step 2 – Unlock the bootloader of the Surface Duo and perform partitioning

1.  On the Surface Duo, go to *Settings* => *About*=> click on the *Build number* until Developer options are enabled.
2.  Go back and select *System* => *Developer options*. Next, enable the OEM unlocking toggle.
3.  Boot to the bootloader interface.
    *   You can do so by [booting to the recovery mode](https://support.microsoft.com/en-us/surface/recover-surface-duo-if-it-won-t-start-1e6fb3cf-4e24-92a8-bc05-4984274bc6a4#ID0EDD=Surface_Duo) and then choosing the *Reboot to bootloader* option.
    *   If USB debugging is turned on, then execute the following command on your PC while the Surface Duo is connected to force it to boot to the bootloader mode:

        ```
         adb reboot bootloader 
        ```

4.  Now that the device is in its bootloader mode, use the following Fastboot command to unlock the bootloader:

    ```
     fastboot flashing unlock 
    ```

    Note that **this step will factory reset the device**.

The bootloader is now unlocked, which means we can manually change the partition layout of the device and make room for the Windows instance. The developer has compiled a semi-working TWRP image for the Duo, so that we can run the `parted` binary from TWRP's internal shell to modify the partitions. Click on the link below to go through the most up-to-date partitioning guide.

**[Making the required partitions on the Surface Duo](https://github.com/WOA-Project/SurfaceDuo-Guides/blob/main/InstallWindows.md#making-the-partitions)**

Notably, the initial version of the guide only targets 128GB devices. You must calculate the partition size values yourself for the 256GB variant.

* * *

### Step 3 - Boot the custom UEFI

If everything goes correctly during partitioning, you can now boot a specially crafted custom UEFI image (internally referred to as "SurfaceDuoPkg") that helps you to boot Windows.

1.  Download the precompiled boot.img from the [latest release section of the project's Github repo](https://github.com/WOA-Project/SurfaceDuoPkg/releases/latest).
2.  Boot the UEFI image:fastboot boot boot.imgThis step will be needed every time you'll want to boot Windows.
3.  You should see the Developer Menu. Navigate with the volume up/down buttons to Mass Storage Mode, and press the Power Button to confirm.

* * *

### Step 4 - Install Windows and drivers

The Mass Storage Mode exposes the internal partitions of the Surface Duo's internal flash storage to the host PC's OS, hence we can easily mount them using the Disk Management console and prepare for Windows installation.

Make sure the target Surface Duo device is in Mass Storage Mode and you have prepared the Windows 11 ISO beforehand. Next, click on the links below to view the most up-to-date guides from the developer on how to apply the Windows image and subsequently install the drivers using the Deployment Image Servicing and Management (DISM) tool.

**[Applying the Windows image using DISM](https://github.com/WOA-Project/SurfaceDuo-Guides/blob/main/InstallWindows.md#installing-windows) || [Installing drivers using DISM](https://github.com/WOA-Project/SurfaceDuo-Guides/blob/main/InstallWindows.md#installing-the-drivers)**

* * *

### Step 5 - Boot Windows on the Surface Duo

At this point, Windows 11 has been successfully installed on the Surface Duo, but the default boot path always leads to the Android OS. If you want to start Windows, boot to the bootloader mode, start the custom UEFI (from Step 3), and Windows should start loading instead of Android.

According to Gustave, the current set of drivers is merely mature to handle the CPU frequency, side buttons, and the sleep/wake events (depending on the folding position). Everything else, including the touch interface, isn't working. The custom UEFI image, on the other hand, is capable enough to boot mainline Linux after necessary adjustments.

* * *

## Conclusion

Dual-booting makes sense on a computer, but does it on a phone like the Microsoft Surface Duo? Not for the general user. Even experienced users might call it an answer without a question, and it does come with some fair annoyances too. But to us at XDA, the additional freedom and choice mean that, if used right, dual booting can be a power user’s Holy Grail.

* * *

**Source:** [Gustave Monce on Twitter](https://twitter.com/gus33000/status/1501990271436967941)