---
layout: default
title: Linux
parent: Software Tips
grand_parent: To my students
nav_order: 1
---

### 1. Introduction

[Linux](https://zh.wikipedia.org/zh-tw/Linux) is an open-source operating system (OS; other operating systems include Microsoft Windows and Mac OSX, for example). The physics and astrophysics communities often adopt the Linux OS as it is compact, reliable, and secure. However, it takes some time to learn how to use it and how to troubleshoot it. 
{: .fs-2 }

My group is presently using the [Cent OS](https://www.centos.org/) Stream 9 and [Rocky Linux](https://rockylinux.org/) 9 Linux distributions. They are very similar to Redhat but are free (i.e., Redhat is not free). 
{: .fs-2 }


If you want to learn Linux, good Chinese documentation can be found at [鳥站](https://linux.vbird.org/). In particular, this website includes an introduction to how to maintain a Rocky Linux 9 server, see [this page](https://linux.vbird.org/linux_server/rocky9/). If you do not read Chinese, [this page](https://ryanstutorials.net/linuxtutorial/) may be workable but there should be others.
{: .fs-2 }


If you would like to install Linux to your laptop, instead of Rocky Linux or Cent OS, I usually also recommend [Ubuntu](https://ubuntu.com/).
{: .fs-2 }

Embedded below are some tips. 
{: .fs-2 }


### 2. Installing

You need to create a bootable USB drive.
{: .fs-2 }

First, insert your USB key. Use the command `fdisk -l` to identify this USB key from a list of devices. Use the following command to re-format the USB key to FAT32 file system, `mkdosfs -I /dev/sdc -F 32` (replace /dev/sdc with the actual device-name of your USB key).
{: .fs-2 }

In Linux, you may use the `dd` command to create it. See the introduction in [this Chinese webpage](https://kb.synology.com/zh-tw/DSM/tutorial/How_do_I_create_a_bootable_USB_drive_for_restoring_Linux), or [this English webpage](https://www.cyberciti.biz/faq/creating-a-bootable-ubuntu-usb-stick-on-a-debian-linux/).
{: .fs-2 }

Example:
{: .fs-2 }
```
dd if=xxx.iso of=/dev/sdc
```
{: .fs-2 }

### 3. Boot menu

In most cases, the boot menu is managed by a program called *grub*. You can set your preferences by editing the file `/etc/default/grub`, using any text editor (for example, *vim*). An example of the content in the /etc/default/grub file is as follows (please google or ask ChatGPT of you would like to understand some of the lines).
{: .fs-2 }

```
GRUB_TIMEOUT=-1
GRUB_TIMEOUT_STYLE=menu
GRUB_DISTRIBUTOR="$(sed 's, release .*$,,g' /etc/system-release)"
GRUB_DEFAULT=1
GRUB_DISABLE_SUBMENU=true
GRUB_TERMINAL_OUTPUT="console"
GRUB_CMDLINE_LINUX="crashkernel=1G-4G:192M,4G-64G:256M,64G-:512M resume=/dev/map
per/rl-swap rd.lvm.lv=rl/root rd.lvm.lv=rl/swap rhgb quiet"
GRUB_DISABLE_RECOVERY="true"
GRUB_ENABLE_BLSCFG=true
```
{: .fs-2 }


### 4. Installing packages

With CentOS or Rocky Linux, use `yum install`; with Ubuntu Linux, use `apt-get install`.
{: .fs-2 }

### 5. Accounts

#### 5.1 root password
```
> sudo -i
(enter password for user)
New password:
Retype new password:
> passwd
```
{: .fs-2 }

### 6. Network environment

Check network status can use `ifconfig` or `ip addr`
{: .fs-2 }

Set network configuration
```
root> vim /etc/netplan/50-cloud-init.yaml

network:
  ethernets:
    enp45s0:
      dhcp4: true
    enp46s0:
      dhcp4: false
      addresses: [xxx.xxx.xxx.xxx/cidr]
      nameservers:
        addresses:
  version: 2
```
{: .fs-2 }

We run `root> netplan apply` to make the new setup take effect.
if we want mask to be 255.255.255.0, we put cidr to be 24.
{: .fs-2 }
