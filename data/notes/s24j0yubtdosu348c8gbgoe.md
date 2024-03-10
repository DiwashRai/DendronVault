
## wsl2: Ubuntu initial setup to getting neovim working

```
sudo apt update

sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install gcc g++
sudo apt install neovim
sudo apt install stow
sudo apt install cmake zip unzip
sudo apt install fzf ripgrep

```
Then follow github instructions on generating ssh-key and adding to ssh-agent. Add that ssh
key to github account.

```
git clone git@github.com:DiwashRai/.dotfiles.git
cd .dotfiles
stow nvim
cd
cd .config/nvim
nvim .
```