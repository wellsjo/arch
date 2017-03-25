## Setup

### pacman mirrorlist
```
# copy pacman mirrorlist to backup and remove hashtags from all servers
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup
set -i 's/^#Server/Server' /etc/pacman.d/mirrorlist.backup

# rank top 6 mirrors and output to mirrorlist
rankmirrors -n 6 /etc/pacman.d/mirrorlist.backup > /etc/pacman.d/mirrorlist
```

### Create arch.conf
Get uuid of root into file first: `blkid -s PARTUUID -o value /dev/sdbX > /boot/loader/entries/arch.conf`
Edit file to this
```
title Arch Linux
linux /vmlinuz-linux
initrd /initramfs-linux.img
options root=PARTUUID=<root uuid> rw
```
