
### install and setup shortcuts
- `sudo dnf install fzf`
Put this in your zshrc:
```sh
if [ -x "$(command -v fzf)"  ]
then
    source /usr/share/fzf/shell/key-bindings.zsh
fi
```