## How to Dual Boot Linux on Windows 10

**Linux is an open-source operating system.** The idea of open-source is that the Linux software is free to share, modify, and distribute. You can install Linux OS on a Mac or Windows computer.

In addition, there are different kinds of Linux operating systems termed distributions (distros). They are based on the Linux kernel and are free to download. Common Linux distributions are **Ubuntu**, **Debian**, **Fedora**, **openSUSE**, **CentOS**, etc.
![Redhat.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376620369/Rlf_RLXEi.png)
By reading through the content of this guide, **you will learn how to install the Ubuntu distribution on a Windows 10 computer.** 
You can install an operating system on a machine, either by replacing the current one or alongside the existing OS.

This guide is handy for Software developers, IT specialists and System administrators. People in these professions usually install and set up operating systems for personal development or work.
## What You Will Need
- A laptop or desktop computer
- At least 50 GB of Free Storage space
- A flash drive (USB stick) of at least 8 GB
- Internet connection

## Installing Linux on a Windows 10 PC. 
There are three steps to dual boot Linux and Windows on the same machine.
- First, create a space for the Linux OS to live. To do this, you will have to partition your hard drive. 
- Next, make a Linux bootable USB
- Finally, install Linux from the bootable USB

### How to Partition the Hard Disk Drive on Windows 10
**First, open the Windows search bar.** It is the magnifying glass icon in the bottom-left corner of your screen.
**Next, input "diskmgmt.MSC" in the search bar and press enter.**
![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376673477/qO8KYknbxo.png)
**Then, right-click on your main hard drive and select "Shrink Volume".** If you have more than one drive, ensure you choose the "Primary Partition". It is usually labelled as (C:) drive.
![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376703456/yAJL4hjsg.png)
**Afterwards, determine how much you want to take from your drive.** At least 40 GB (40,000 MB) is recommended for Linux.
![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376273284/4vcOEZdbr.png)
**Finally, click "Shrink".**

### How to Make a Bootable Linux USB Drive
Having created the space to install Linux, the next phase is to write a Linux distro onto a USB drive or external drive of 4 GB or more.

**Step 1: Download a Linux distro in ISO format.** An ISO file is a disk image. It is free to download from each Linux distro website.

For illustration purposes, the distro used in this guide is Ubuntu. You can download the latest Ubuntu distribution [here](https://ubuntu.com/download/desktop). **Ensure to save it to a memorable location on your PC.**
![6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376242793/REYiSe52k.png)

**Step 2: Insert the USB drive into your computer.** However, it may require you to format your hard disk. Formatting a drive will erase all the data stored on such a disk. Therefore, ensure to back up your files before you begin.

**Step 3: Download Rufus.** Rufus is a utility that helps format and creates bootable flash drives. You can find the latest version of the application  [here](https://rufus.ie/).

**Step 4: Open Rufus.** Then select your USB drive from the Device list. If you do not know which drive to use, eject all other drives until you have one storage to choose from.
 
**Step 5: Click the Select button under Boot Selection.** Select the Linux distro ISO file you downloaded earlier. Do not alter other default settings.
![7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376160190/B885weNPp.png)

**Step 6: Click Start.** If you get a pop-up message asking you to select a mode to write the image,  click on ISO.
![8.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376124808/-TsMj_GMo.jpeg)

Wait for Rufus to mount your ISO file onto your drive. This process might take some time, so be patient if the progress bar gets stuck.

**Warning:** This will erase all the data on your drive. Ensure you back up all other files on the USB stick.
 
### How to Install Linux from a USB
**To start, insert a bootable Linux USB drive. Then, click the start menu.** It is the Windows icon in the lower-left corner of your screen.

**Next, hold down the SHIFT key while clicking "Restart".** It will take you into the Windows Recovery Environment.
![9.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376086759/_n15AI75v.jpeg)
  
**While in the "Windows Recovery Environment", select "Use a Device".**
![10.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376040485/Xy9SUSa2z.jpeg)
 
Following this step, find your device in the list. However, if you do not see your drive, select EFI USB Device, then pick your drive from the next screen.
![12.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643376028821/mtEEuV0uN.jpeg)

Your computer will now boot Linux. If your computer reboots Windows, it is either an issue with the USB drive or you might have to change settings in your BIOS.

**Warning:** Altering BIOS settings can cause harm to your computer if you do not know what you are doing. 
 
**Next, select "Install Linux".** Some distros also let you try out the OS before installing it here.
![13.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643375998798/sIdO4y5mW.jpeg)

**Go through the installation process.** The process will be unique to the distro you are trying to install. The details might include your Wi-Fi network, language, time zone, keyboard layout, etc. 

Also, you might be required to create an account with a username and password. Make sure to write down any details, as you will likely need them in the future.
Most distros will allow you to partition your drive or erase it and do a clean installation.

**Warning:** Erasing your disk will mean you will lose your settings, files, and Windows operating system. Only select Erase if you have saved copies of all your files before starting the installation process.

**Finally, reboot your computer when prompted.** If you have more than one OS in your system, you will be taken to a GNU GRUB screen after rebooting. This screen allows you to select which OS you want to boot.
![14.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1643375951439/VWcjtNI1A.jpeg)

If you do not see a GRUB screen when you boot up your computer, you can try moving your Linux distro higher on your boot list in BIOS.

At last, you can perform a hardware check. Mostly, you may need to download additional drivers to make some hardware components work. The option to download drivers is within the system settings of the Linux OS. After verifying that your hardware is working, you can start exploring and using your Linux distro.
 
## Wrapping Up
Linux OS is easy to use and adapt to if you are tech-savvy or simply know how to navigate your way through any other OS.

Ensure you follow up the instructions carefully to avoid mistakes. Take note of any changes made to the BIOS. It will help you troubleshoot any problem due to altering those settings.