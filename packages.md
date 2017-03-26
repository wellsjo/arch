# Post-installation setup

## Install packages
```bash
# Basics
sudo pacman -S vim
sudo pacman -S git
sudo pacman -S openssh

sudo pacman -S mpstat
sudo pacman -S screenfetch
sudo pacman -S termite        # Terminal
sudo pacman -S conky          # System monitor
sudo pacman -S most           # Pager (improved less)
sudo pacman -S feh            # Image viewer
sudo pacman -S mesa           # OpenGL
sudo pacman -S xsel           # for copy/paste
sudo pacman -S yaourt         # AUR package installs

# Display
sudo pacman -S xorg-server
sudo pacman -S xorg-xinit
sudo pacman -S xorg-xrandr
sudo pacman -S dmenu
sudo pacman -S compton

yaourt -S i3-gaps-next-git             
yaourt -S i3blocks-gaps-git
yaourt -S ttf-ms-fonts
```

## Applications
```
yaourt -S google-chrome-beta
```
