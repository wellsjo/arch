# arch
Arch Linux post-install setup

## Basics
```bash
sudo pacman -S vim
sudo pacman -S git
sudo pacman -S openssh
sudo pacman -S xorg-server

sudo pacman -S xsel     # for copy/paste
sudo pacman -S yaourt   # AUR package installs
```

## Configure
```
alias pbcopy='xsel --clipboard --input'
alias pbpaste='xsel --clipboard --output'
```

## Applications
```
yaourt -S google-chrome
```
