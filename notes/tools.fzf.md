---
id: 6kpo1942ysua78f6grwyijm
title: Fzf
desc: ''
updated: 1688264432409
created: 1688264382675
---

### install and setup shortcuts
- `sudo dnf install fzf`
Put this in your zshrc:
```sh
if [ -x "$(command -v fzf)"  ]
then
    source /usr/share/fzf/shell/key-bindings.zsh
fi
```