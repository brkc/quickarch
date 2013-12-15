archlinux-install
=================

This script is mainly to prompt me for
the arguably mandatory settings
that I always forget to set when installing.

It does *not* guide you through partitioning,
pacstrapping, or anything else you might want
to do before chrooting.

Here is how I use it:
```
fdisk /dev/sda
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
