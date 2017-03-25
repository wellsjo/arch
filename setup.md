## Setup

# pacman mirrorlist

# remove hashtags
```
# copy pacman mirrorlist to backup and remove hashtags from all servers
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup
set -i 's/^#Server/Server' /etc/pacman.d/mirrorlist.backup

# rank top 6 mirrors and output to mirrorlist
rankmirrors -n 6 /etc/pacman.d/mirrorlist.backup > /etc/pacman.d/mirrorlist
```
