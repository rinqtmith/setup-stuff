# Install list

## Install fonts

```bash
sudo apt install fontconfig curl unzip fzf
git clone https://github.com/ronniedroid/getnf.git
cd getnf
./install.sh
```

## Install tmux

```bash
sudo apt install tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Copy the config file to `~/.tmux.conf`

## Install zsh

```bash
sudo apt install zsh
chsh -s $(which zsh)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
sudo apt install fortune cowsay
sudo apt install autojump
```

Copy the config file to `~/.zshrc` and `~/.zshenv`

## Install Python

```bash
sudo apt install python-is-python3
sudo apt install python3-pip
sudo apt install python3.10-venv
```

## Install Node.js

```bash
curl -fsSL https://deb.nodesource.com/setup_21.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
sudo npm install -g pnpm
```

## Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## Install Neovim

```bash
sudo apt-get install ninja-build gettext libtool libtool-bin autoconf automake cmake g++ pkg-config unzip curl doxygen xclip
git clone https://github.com/neovim/neovim
make CMAKE_BUILD_TYPE=Release
sudo make install
sudo npm install -g neovim
sudo npm install -g tree-sitter-cli
python3 -m pip install pynvim
```

Copy the config files.


# Install some tools

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
sudo apt-get install ripgrep
sudo apt install fd-find
```
