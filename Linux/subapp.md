# <p align="center">Linux系统部分可替代软件</p>

linux自带的软件也许不是特别好用，当然基本使用在日常工作中是够了的，但是本着易于使用的原则，还是推荐用几款更优秀的软件来替代之。

小建议：在家目录下建一个名为app的文件夹，后面的操作会方便很多。

## zsh
zsh 用于替代bash，不要问为什么，好用就完了。这个软件还是推荐自行下载安装。
```bash

# 无root权限安装zsh
# 下载
wget -O zsh.tar.xz https://sourceforge.net/projects/zsh/files/latest/download
# 解压
tar -xvf zsh.tar.xz
cd zsh
# 配置，比如将zsh安装到~/app/zsh下
./configure --prefix=$HOME/app/zsh
make && make install
# 设置开机启动zsh
export PATH=$HOME/app/zsh/bin:$PATH
exec $HOME/app/zsh/bin/zsh
```
请搭配oh-my-zsh服用，效果更佳

```bash
# 下载脚本
# 如果不能下载可去网站下载后上传
wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh
# 安装oh-my-zsh
zsh install.sh

# 插件
# zsh-syntax-highlighting(命令语法高亮)
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
# zsh-autosuggestions(命令自动补全)
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
# 修改~/.zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting z extract)
```

## 其他软件
+ htop

替代top


+ exa

替代ls


+ axel

替代wget



+ bat

替代bat


+ duf

替代du

具体用法：
下载编译后压缩文件[sub.zip](https://github.com/sdy-xu/bioinformatics/blob/master/Linux/sub.zip)


```bash
# zshrc配置文件

# duf
alias duf='$HOME/app/duf/duf'

# ag
alias ag='$HOME/app/ag/bin/ag'

# axel
alias axel='$HOME/app/axel/bin/axel'

# exa
alias exa='$HOME/app/exa/bin/exa'

# bat
alias bat='$HOME/app/bat/bat'

# alias
alias ls='exa'
alias ll='exa -lh'
alias la='exa -la'

```





