---
title: "Linux"
weight: 1
description: >
  Don't just learn linux, better to practice it
categories: [operatingsystem]
tags: [Devops]
---

{{< alert color="success" >}}
UNIX is basically a simple operating system, but you have to be a genius to understand the simplicity.

  -- Dennis Ritchie
{{< /alert >}}

### Pre-requirements
- Any linux distribution (ubuntu/redhat/or any)
- VM/Metal/Containers
- Spin up instance in any cloud (openstack/ or any)
- WSL [windows subsystem for linux](https://learn.microsoft.com/en-us/windows/wsl/about)

{{< alert color="warning" >}}
Don’t try installing software if you are running the live CD. Because writeable space on a live CD uses virtual memory
(RAM), that space is limited and can easily run out. Also, when you reboot your system, anything you install will be gone.
{{< /alert >}}

# Beginners 

## Introduction to linux 
1. linux - opensource 
1. Kernel is in the middle layer between Hardware and Shell 
1. kernel - who is managing 
1. BDS license - mac 
1. difference from windows 

<iframe width="560" height="315" src="https://www.youtube.com/embed/QCAC4e6PxAc?si=LZNUsl9ClvAyiY27" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Where linux used
- Network switches
- Datacenter servers 





### Useful tools
- putty
- mremoteng
- winscp
- X11/Wayland

## popular distros 
transition from windows/mac to linux 
release frequency 
LTS kernel 

## Hardware OS details
hostname
tab completion 
top,
ps
df -h
free
tail
ping 
time, date 
uptime
version
lscpu

## repository
    default packages installed 
security packages 
## Terminal basics
    connect to a server remotely(putty)
## Filesystem basics
    everything in linux is a file 
        devices is a file 
        memory is a file
        directory is a file 
        file is a file
        file system organized 

process 
 $PATH
help/man

## User Management
describe user accounts/ root user
    local account 
    ldap/active directory 
    sssd
groups
create user account 
change password 
.bashrc
sudo 
default shell
### SSH 
ssh
ssh key
cron/systemd timer/
create a file 
text editors 
file permission (chmod)
chown
symbolic link
grep 
more
history

## Process:
Kill
background commands
input/output redirection 
system logs 
systemd/sysvinit/runlevel


## Network
curl,wget
ip
telnet,scp
iptables
ufw
selinux 

# Intermediate 

Fundamentals: 
    boot process 
    grub 
    BIOS/UEFI

## Resource managent and Isolation:
    cgroups
    session


## Unix file systems

btrfs
ext4
xfs
zfs

## Storage:
mount a drive 
filesystem types
inodes
swap
NFS
fdisk 
lvm
raid level


## Package manager:
apt
snap
repository management
internal/external repository 
install a package, history
restricted environment - artifactory 



# Advanced

## Installation:
    cloud-init 

## Shell scripting and bash:

## Virtualiztion and containers:
KVM 
NFS for linux and windows 
access control 
network booting 
    ipxe/pxe 
    netboot.zxy

## Network 
DHCP /DNS / Ethernet/ network identifier 
traceroute 
Security
ipv6 configuration
network namespaces 
virtual bridges 
OSI layer 
protocols 
TCP/UDP/HTTP/HTTPS

## Troubleshooting:


## Backup and recovery

## Performance tuning

## Clustering and HA

# Root directory structure 


# linux hardening 
security is a process not a product


Running program is a process
    even shell is a process


# create a process 
system() --> simply creates a shell and runs the process (inefficient/less secure)
fork() --> 


# syscalls

# kernel architecture 

macos is based on Mach kernal --> microkernel 


daemons are system services 
demons are device driver 


POSIX - Portable Operating System Interface for Unix 
SUS - Single Unit Specification 





ls --hide=Desktop

Most user commands that come with Linux are stored
in the /bin, /usr/bin, or /usr/local/bin directories. The /sbin and /usr/sbin
directories contain administrative commands 

/etc/profile -- executes when first login 
/etc/bashrc -- executes everytime 


> directs standard output, override the file 
>> directs standard output, appends to the file 
2> directs standard error 
&> directs standard error and output 