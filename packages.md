# arch
Arch Linux post-install setup

## Basics
```bash
sudo pacman -S vim
sudo pacman -S git
sudo pacman -S xsel # for copy/paste
sudo pacman -S yaourt
sudo pacman -S openssh
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
