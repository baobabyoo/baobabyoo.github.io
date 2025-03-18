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


#### 6.0 Basics
Check network status can use `ifconfig` or `ip addr`
{: .fs-2 }

Set network configuration : Ubuntu
```
root> vim /etc/netplan/50-cloud-init.yaml

network:
  ethernets:
    enp45s0:
      dhcp4: true
    enp46s0:
      dhcp4: false
      addresses: [xxx.xxx.xxx.xxx/cidr]
      gateway4: xxx.xxx.xxx.xxx
      nameservers:
        addresses: [8.8.8.8,101.101.101.101]
  version: 2
```
{: .fs-2 }

{: .fs-2 }

We run `root> netplan apply` to make the new setup take effect.
if we want mask to be 255.255.255.0, we put cidr to be 24.
You can also set this using the GUI interface.
{: .fs-2 }

We can check active internet connection with the command `> sudo netstat -lntp`
{: .fs-2 }

#### 6.1 Enable port 22 ssh connection for Ubuntu (CentOS Steam 9 and Rocky Linux 9 does not require this.)
{: .fs-2 }

```
# install open ssh server
> sudo apt install openssh-server

# set the connection port (normally, port 22)
> sudo vim /etc/ssh/sshd_config
(if it is slow to login, try edit useDNS in this file to NO)

# restart ssh service
> sudo systemctl restart ssh
> sudo systemctl status ssh


# UFW is a simple firewall that is on Ubuntu
# check ufw status
> sudo ufw status

# enable ufw service
> sudo ufw enable

# enable port 22 connection
> sudo ufw allow ssh
# or
> sudo ufw 22/tcp
```
{: .fs-2 }


#### 6.2 IP forwarding

```
> vim /etc/sysctl.conf
(uncomment) net.ipv4.ip_forward=1
> sysctl -p
> iptables -t nat -A POSTROUTING -s 192.168.1.0/24 -j MASQUERADE
```
{: .fs-2 }


#### 6.X Practice of setting up Local Area Network (LAN) 區域網路設置實務 (Ubuntu)

Here, I assume you have
- One Ubuntu Linux desktop with two network interface card (網路卡). We call this desktop the **Master node**.
- One **router** (probably with 1 WAN port and several LAN ports; 路由器，亦稱IP分享器), which can also share WIFI.
- One Linux desktop with Linux OS systems (e.g., CentOS, Rocky Linux, Ubuntu, etc). We call this desktop the **Computing node**. If you have multiple computing nodes, the setup of each of them will be similar. Usually, each of your computing node only needs one network interface card.
- One fixed IP, e.g., **140.117.123.456** (you need to obtain this from the IT guy).
{: .fs-2 }

I assume that what you want to do is connecting from outside (e.g., your home) to your Master node using `ssh`, and then connecting from the Master node to the computing node. In addition, you want the computing nodes to be able to access to to the internet (e.g., check e-mail, browsing, or download files).
{: .fs-2 }

In this case, on the Master node, you need to use one network interface card to connect to the internet (let's call this card *NIC-global*), and use the other network interface card to connect to the local area network, likely from the router (let's call this card *NIC-local*).
{: .fs-2 }

The steps you need to follow are:
{: .fs-2 }
1. Connecting the Wide Area Network (WAN) internet cable (i.e., from outside of your office) to *NIC-global*. Then you can set the network configuration of your **Master node** for *NIC-global*.
   - set IP to 140.117.123.456 (for example). Typically, the netmask is 255.255.255.0, and typically, the gateway is 140.117.123.254 (i.e., change the last three digits of your IP to 254. Note that it is not necessarily this case. In case of problem, you need to consult the IT guy of your institution.)
    - set the Domain Name System (DNS) server(s) to 8.8.8.8 and/or 101.101.101.101. If you are in NSYSU, you can also include our DNS server, 140.117.11.1.
    - Apply your setup. Then with a command line, type `> ping 8.8.8.8` and see if you are connected (in this case, to the DNS server of google).
    {: .fs-2 }
2. Connecting another cable from *NIC-local* to your router, and then set the network configuration.
   - We may set the IP and netmask to 192.168.100.254 and 255.255.255.0. We can leave gateway blank or set it to 192.168.100.254.
3. Active the IP forwarding service (IP轉發) on the Master node, and properly set the firewall (防火牆). I will first uncomment `net.ipv4.ip_forward=1` in the file `/etc/sysctl.conf` (see also [IP forwarding](https://baobabyoo.github.io/pages/students_topics/software_tips_Linux.html#62-ip-forwarding)). I will then create a text file iptables.sh (e.g., using `vim`) with the content embedded below (if you use other IP for the LAN, you need to edit the IP correspondingly):
    and then execute this file by typing `> sudo sh iptables.sh`
4. Connect your computing node to a LAN port of your router, and then set the network configuration. You can set the IP, netmask, and gateway to be `192.168.100.ABC`, `255.255.255.0`, and `the LAN IP of your Master node (e.g., 192.168.100.254)`. Here, ABC should be an integer in the range of 002~253 (reserving 000, 001, and 254 for other purposes).
5. On the computing node, trying pinging 8.8.8.8 and see if you are connected. You can also try using browser.
6. Test the connection from outside. Since the firewall of NSYSU does not permit ssh connection from outside, you need to pretent being in the domain (網域) of NSYSU using the VPN service (please see the [instruction of the NSYSU VPN](https://lis.nsysu.edu.tw/p/412-1001-7113.php) and download the VPN client to your outside desktop or laptop, which is not your Master or computing node). Activate the VPN service and connect it. Then open an terminal and type `ssh 140.117.123.456` (i.e., ssh to the fixed IP of your Master node) to connect to the Master node. You should be able to ssh from the Master node to any of your computing nodes. 
7. You can also connect your printer to a LAN port of the router (if possible). 
{: .fs-2 }

Here is an example for the `iptables.sh` files:
{: .fs-2 }

```
#!/bin/bash
# part 1： 清除規則並設定預設政策
iptables -F
iptables -X
iptables -Z
iptables -P INPUT   DROP
iptables -P OUTPUT  ACCEPT
iptables -P FORWARD ACCEPT

# part 2； 基礎的三條防火牆規則
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
iptables -A INPUT -i lo -j ACCEPT
iptables -A INPUT -p icmp -j ACCEPT

# allow ssh from outside via port 22
iptables -A INPUT -p tcp --dport 22 -j ACCEPT

# part 3； 拒絕黑名單、開放白名單的設定
## 黑名單例子
# iptables -A INPUT -s 10.30.30.0/24 -j REJECT
# iptables -A INPUT -i enp1s0 -s 192.168.201.254 -j ACCEPT
## 中山校內網路設為白名單
iptables -A INPUT -i enp46s0 -s 140.117.30.0/24 -m state --state NEW -p tcp --dport 22 -j ACCEPT
## 實驗室內部網路設為白名單
iptables -A INPUT -i enp45s0 -s 192.168.100.0/24 -m state --state NEW -p tcp --dport 22 -j ACCEPT

# part 4： 一般通用放行的網際網路服務
iptables -A INPUT -m state --state NEW -p tcp --dport  80 -j ACCEPT
iptables -A INPUT -m state --state NEW -p tcp --dport 443 -j ACCEPT
iptables -A INPUT -m state --state NEW -p udp --dport  53 -j ACCEPT
iptables -A INPUT -m state --state NEW -p tcp --dport  53 -j ACCEPT

# part 5： 儲存規則
iptables-save

# part 6: 允許以及執行IP forwarding
iptables -t nat -A POSTROUTING -s 192.168.100.0/24 -j MASQUERADE
sysctl -p
```
{: .fs-2 }
