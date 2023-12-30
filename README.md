# dotfiles

```
my dotfiles, for a unified dev experience across multiple devices.
```

### install primary utility tools

```
sudo dnf install curl wget htop xclip neovim fd-find bat lsd net-tools wireshark-devel bind-utils git zsh nnn
```

### Run nerd fonts installer

```
./nerdfonts.sh
```

### Install oh my zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)
```

### install powerlevel10k

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
```

```
cp .p10k.zsh
```

```
source ~/.p10k.zsh
```

### install zsh highlight

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

### install zsh auto suggestion

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### install zsh fzf

```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

### copy .zshrc file

```
cp .zshrc
```

```
source ~/.zshrc
```

### Install kitty

```
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin
```

```
cp kitty.conf to ~/.config/kitty/
```
### adding QEMU
``````
dnf install @virtualization
dnf install qemu -y 
``````

### Download Flatpak
```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

### Install flatpak productivity apps
```
flatpak install flathub com.github.xournalpp.xournalpp
flatpak install flathub com.obsproject.Studio
flatpak install flathub com.discordapp.Discord
flatpak install flathub com.slack.Slack
flatpak install flathub io.github.bkueng.qMasterPassword
flatpak install flathub org.videolan.VLC
flatpak install flathub com.jetbrains.IntelliJ-IDEA-Ultimate
flatpak install flathub us.zoom.Zoom
flatpak install flathub com.github.IsmaelMartinez.teams_for_linux
flatpak install flathub com.microsoft.Edge
flatpak install flathub com.brave.Browser
flatpak install flathub org.mozilla.Thunderbird
flatpak install flathub com.belmoussaoui.snowglobe
flatpak install flathub org.getoutline.OutlineClient
```


#### discord theme

```
wget https://github.com/BetterDiscord/Installer/releases/latest/download/BetterDiscord-Linux.AppImage
chmod a+x 
```

```
cp mocha.theme.css
```

#### slack theme

```
#1E1E2E,#F8F8FA,#CBA6F7,#1E1E2E,#11111B,#CDD6F4,#CBA6F7,#EBA0AC,#1E1E2E,#CDD6F4
```

### shortcuts

ctrl+f

ctrl+k

ctrl+d /ctrl+u like nvim

ctrl+s fzf


### languages to install

c/c++
nodejs
go
rust
java
python (pre-installed with fedora)



#### C lang packages
``````
dnf install clangd
dnf install gcc-c++
dnf install cmake
dnf install csbuild
(use it as csbuild -c 'make ...')
``````

#### Node Js
``````
dnf install nodejs
``````

#### Go
``````
dnf install golang
``````

#### Rust

``````
dnf install rust cargo
``````

#### Java

``````
dnf install java-devel
dnf install maven
dnf install java-openjdk
``````

