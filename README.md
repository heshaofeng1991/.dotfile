### 使用
```shell
git clone https://github.com/Laily123/.dotfile.git ~/.dotfile
```
### zsh 安装
安装 zsh  
```shell
https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH
# macOS
brew install zsh zsh-completions
# CentOS
sudo yum -y install zsh
# Ubuntu
apt install zsh
```

安装 oh-my-zsh  
```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
初始化配置  
```shell
ln -sf ~/.dotfile/.zshrc ~/  
ln -sf ~/.dotfile/laily.zsh-theme ~/.oh-my-zsh/themes/
ln -sf ~/.dotfile/.tmux.conf ~/
ln -sf ~/.dotfile/.gitconfig ~/.gitconfig
```

### spacevim 安装
安装  
`curl -sLf https://spacevim.org/install.sh | bash`  
初始化配置  
`ln -sf ~/.dotfile/.SpaceVim.d ~/` 

### autojump 安装
autojump 是通过记录进入过的目录到数据库来实现的, 所以必须是曾经进入过的目录才能跳转.
macOS 安装
推荐使用 Homebrew 安装 autojump
`brew install autojump`

### zsh-autosuggestions 安装
zsh-autosuggestions自动补全插件
zsh-autosuggestions 安装
`git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`

### zsh-syntax-highlighting安装
zsh-syntax-highlighting语法高亮插件
zsh-syntax-highlighting安装
`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git`

### 上述都安装完之后的操作
vi ~/.zshrc 在plugins下添加autojump,zsh-suggestions等你喜欢的插件 ：wq保存退出
根目录下 mkdir .zprofile文件,添加以下内容进去
```shell
. HOME/autojump/autojump.sh
source HOME/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
source ZSH_CUSTOM/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
:wq 保存退出
source ~/.zshrc
```


