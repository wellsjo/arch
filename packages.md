# Post-installation setup

## Basics
```bash
sudo pacman -S vim
sudo pacman -S git
sudo pacman -S openssh
sudo pacman -S xorg-server
sudo pacman -S xorg-xinit
sudo pacman -S termite
sudo pacman -S dmenu
sudo pacman -S feh

sudo pacman -S mesa           # OpenGL
sudo pacman -S xsel           # for copy/paste
sudo pacman -S yaourt         # AUR package installs

# AUR
yaourt -S i3-gaps             # Window manager
yaourt -S i3blocks-gaps-git
yaourt -S ttf-ms-fonts
```

## Configure
```
alias pbcopy='xsel --clipboard --input'
alias pbpaste='xsel --clipboard --output'
```

## Applications
```
yaourt -S google-chrome-beta
```
