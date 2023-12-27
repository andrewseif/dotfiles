# dotfiles
```
my dotfiles, for a unified dev experience across multiple devices.
```
### install primary utility tools
``````
sudo dnf install curl wget htop xclip neovim fd-find bat lsd net-tools wireshark-devel bind-utils git zsh nnn
``````
### Run nerd fonts installer
``````
./nerdfonts.sh
``````
### Install oh my zsh
``````
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)
``````
### install powerlevel10k
``````
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
``````
``````
cp .p10k.zsh
``````
``````
source ~/.p10k.zsh
``````
### install zsh highlight
``````
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
``````
### install zsh auto suggestion
``````
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
``````

### install zsh fzf
``````
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
``````
### copy .zshrc file
``````
cp .zshrc
``````
``````
source ~/.zshrc
``````
### Install kitty
``````
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin
``````


### install discord
``````
sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf update
sudo dnf install discord
``````
#### discord theme
``````
wget https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Linux.AppImage
``````
``````
cp mocha.theme.css
``````

### install slack
``````
wget https://downloads.slack-edge.com/releases/linux/4.35.131/prod/x64/slack-4.35.131-0.1.el8.x86_64.rpm
``````
#### slack theme
``````
#1E1E2E,#F8F8FA,#CBA6F7,#1E1E2E,#11111B,#CDD6F4,#CBA6F7,#EBA0AC,#1E1E2E,#CDD6F4
``````
### shortcuts
ctrl+f


ctrl+k

ctrl+d /ctrl+u like nvim

ctrl+s fzf 


