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

``````
cp kitty.conf to ~/.config/kitty/
``````
``````
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
``````

``````
flatpak install discord
flatpak install obs studio 
flatpak install slack
flatpak install 
``````
``````

``````
``````

``````
``````
``````

``````
``````

#### discord theme
``````
wget https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Linux.AppImage
``````
``````
cp mocha.theme.css
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


