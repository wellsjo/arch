## Setup
(this is incomplete)

### pacman mirrorlist
```
# copy pacman mirrorlist to backup and remove hashtags from all servers
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup
set -i 's/^#Server/Server' /etc/pacman.d/mirrorlist.backup

# rank top 6 mirrors and output to mirrorlist
rankmirrors -n 6 /etc/pacman.d/mirrorlist.backup > /etc/pacman.d/mirrorlist
```

## Making bootable

### Install intel-ucode
```
pacman -S intel-ucode
```

### Create arch.conf
Get uuid of root into f ile first: `blkid -s PARTUUID -o value /dev/sdbX > /boot/loader/entries/arch.conf`  
Then edit file to this:
```
title Arch Linux
linux /vmlinuz-linux
initrd /initramfs-linux.img
options root=PARTUUID=<root uuid> rw
```

### Install gpu drivers (NVIDIA)
```
pacman -S nvidia lib32-nvidia-utils
```

Rebooot system

### Network
Find ethernet device, start it, and enable it for continued use
```bash
ip link # to get the device id
sudo ip link set <device> up
sudo systemctl start dhcpcd@<device>.service
sudo systemctl enable dhcpcd@<device>.service
```
