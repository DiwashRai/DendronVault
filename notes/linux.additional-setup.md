---
id: qogf6mgpnnfneh0wjxxl7dh
title: Additional Setup
desc: ''
updated: 1687225022369
created: 1687087095027
---

## install nerd fonts
Download JetBrains at least
- download nerd fonts from [here](https://www.nerdfonts.com/font-downloads)
- mkdir `~/.local/share/fonts`
- `unzip JetBrainsMono.zip -d ~/.local/share/fonts`

## zsh
- `sudo dnf install zsh`
  - `sudo dnf install util-linux-user`
  - `chsh -s $(which zsh)`
  - setup zsh settings upon first login
    - history
      - HISTSIZE=10000
      - SAVEHIST=10000
          - HISTFILE=~/.zsh_history
    - completion system
      - default
    - key bindings (vi or emacs)
      - vi
    - other shell options
      - unset beep
- install powerline10k

## other packages
- `sudo dnf install tmux`
- `sudo dnf install ulauncher`
- `sudo dnf install dmenu`
- `sudo dnf install neovim python3-neovim`
- `sudo dnf install vlc`

## install brave browser
- `sudo dnf install dnf-plugins-core`
- `sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/x86_64/`
- `sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc`
- `sudo dnf install brave-browser brave-keyring`