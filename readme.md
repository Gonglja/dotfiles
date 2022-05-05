# 如何使用

下载到`~`目录

```shell
cd  ~
git clone https://github.com/Gonglja/dotfiles.git .dotfiles
cd  ~/.dotfiles
git submodule init 
git submodule update 
```



## zsh

安装zsh
```shell
sudo apt install zsh
chsh -s /bin/zsh
```

创建软链

```shell
ln -s ~/.dotfiles/zsh/.zshrc  ~/.zshrc
```



## z.lua 配置

对于ubuntu，直接apt命令安装最新版本lua

```shell
sudo apt install lua5.4
```

然后`vim ~/dotfiles/zsh/.zshrc`，最后一行添加即可

```shell
eval "$(lua $HOME/.dotfiles/z.lua/z.lua  --init zsh once enhanced)"
```





## tmux 配置

```shell
ln -sf ~/.dotfiles/.tmux/.tmux.conf  ~/.tmux.conf
ln -sf ~/.dotfiles/.tmux/.tmux.conf.local ~/.tmux.conf.local
```



## 参考

1. [zsh & oh-my-zsh 的配置与使用](https://zhuanlan.zhihu.com/p/58073103)
2. [git submodule 使用小结](https://www.jianshu.com/p/f8a55b972972/)
