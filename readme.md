# 如何使用

下载到`~`目录

```shell
git clone https://github.com/Gonglja/dotfiles.git .dotfiles
git submodule init 
git submodule update 
```



## zsh

创建软链

```shell
ln -s .dotfiles/zsh/.zshrc .zshrc
```



## z.lua 配置

对于ubuntu，直接apt命令安装最新版本lua

```shell
sudo apt install lua5.4
```

然后`vim ~/dotfiles/.zshrc`，最后一行添加即可

```shell
eval "$(lua $HOME/.dotfiles/z.lua/z.lua  --init zsh once enhanced)"
```





## tmux 配置

```shell
ln -sf ~/.dotfiles/tmux/.tmux.conf .tmux.conf
ln -sf ~/.dotfiles/tmux/.tmux.conf.local .tmux.conf.local
```

