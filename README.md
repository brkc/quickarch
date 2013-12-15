archlinux-install
=================

This script is mainly to prompt me for
the arguably mandatory settings
that I always forget to set when installing.

It does **not** guide you through partitioning,
pacstrap, or anything else you might want
to do before chrooting.

When and how to run it:
```
fdisk /dev/sda
mkfs.ext4 /dev/sda1
mount /dev/sda1 /mnt
pacstrap /mnt base base-devel
genfstab /mnt > /mnt/etc/fstab
arch-chroot /mnt
pacman -S git
git clone https://github.com/brkc/quickarch
cd quickarch
./quickarch
```

How to use it:
```
editor?
1) vim
2) vi
3) nano
#? 3
Generating locales...
  en_US.UTF-8
  en_US.ISO-8859-1
Generation complete.
locale?
1) en_US.UTF-8
2) en_US
#? 1
localtime? (tab-tab) America/New_York
clock?
1) utc
2) localtime
#? 1
hostname? archlinux
```
