quickarch
=================
This script automates the tedium
that comes after chrooting your
Arch Linux installation. This includes
* adding users
* enabling sudo
* installing a bootloader
* setting your
  - locale-specific information
  - hostname
  - passwords
* and anything else you might forget to do
  before your mass package install!

It does *not* guide you
through partitioning, pacstrap,
or anything else you might want to do
before chrooting.

When and how to run it:
```
mount /dev/sdaX /mnt
pacstrap /mnt base base-devel
genfstab /mnt > /mnt/etc/fstab
arch-chroot /mnt
curl -L tinyurl.com/quickarch > quickarch
bash quickarch
```

How to answer it:
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
want dhcp? y
want wifi? y
want grub? y
```
