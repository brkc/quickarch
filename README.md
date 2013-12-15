archlinux-install
=================

A minimal script to automate an Arch Linux install.

```
mkfs.ext4 /dev/sda1
mount /dev/sda1 /mnt
pacstrap /mnt base base-devel
genfstab /mnt > /mnt/etc/fstab
arch-chroot /mnt
pacman -S git
git clone https://github.com/brkc/archlinux-install
cd archlinux-install
. archlinux-install
all
```
