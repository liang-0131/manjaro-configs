## Manjaro全局设置
### 代理
#### 安装代理软件

```shell
# 安装qv2ray
sudo pacman -S qv2ray
```
[v2ray-core](https://github.com/v2fly/v2ray-core/releases/tag/v4.44.0) 5.0以上版本可能用不了

#### 配置
软件设置：
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241717718.png)
浏览器设置：
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241721317.png)

### 终端代理
- [配置](https://github.com/liang-0131/terminal-proxy)
### neovim
```shell
# nvim
sudo pacman -S neovim
```

### 输入法
安装：
- [五笔输入法](http://wp02.ysepan.com/)    

配置：
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241648265.png)
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241650207.png)



### 配置国内源
1.配置镜像源:
```shell
sudo pacman-mirrors -i -c China -m rank
```
2.设置 archlinuxcn 源,antergos源,arch4edu源:
sudo nvim /etc/pacman.conf
```shell
[archlinuxcn]
SigLevel = Optional TrustedOnly
#中科大源
Server = https://mirrors.ustc.edu.cn/archlinuxcn/$arch
#清华源
Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch

[antergos]
SigLevel = TrustAll
Server = https://mirrors.tuna.tsinghua.edu.cn/antergos/$repo/$arch

[arch4edu]
SigLevel = TrustAll
Server = https://mirrors.tuna.tsinghua.edu.cn/arch4edu/$arch
```

3.更新源列表
```shell
sudo pacman-mirrors -g
```

4.更新pacman数据库并全面更新系统
```shell
sudo pacman -Syyu
```

5.防止PGP签名错误
```shell
sudo pacman -S archlinuxcn-keyring
sudo pacman -S antergos-keyring
```

### 安装ARU包管理工具
```shell
sudo pacman -S yay
```

## 应用安装

### syncthing
安装

```shell
sudo pacman -S syncthing
```

```shell
# 创建
mkdir -p ~/.config/systemd/user && cp /usr/lib/systemd/user/syncthing.service ~/.config/systemd/user
# 启动
systemctl --user enable syncthing.service
```

开机自启
- [参考](https://linuxconfig.org/how-to-keep-files-and-directories-synchronized-across-different-devices-using-syncthing-on-linux)

### obsidian
安装
```bash
sudo pacman -S obsidian
```

可选依赖：
- [PicGo](#PicGo)
- [xclip](#xclip)
- [ob切换输入法](#obsidian切换输入法)
### obsidian切换输入法
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241638962.png)
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241640460.png)

### PicGo
安装：
```shell
yay -S picgo-appimage
# picgo依赖于xclip进行第三方剪贴操作
yay -S xclip
```

[配置](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#github%E5%9B%BE%E5%BA%8A)
- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241627047.png)

- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241631019.png)

依赖：
- xclip
### xclip
```shell
# 第三方进行picgo剪贴操作所需依赖
yay -S xclip
```
### 系统截图工具-Spectacle
配置：

- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241336925.png)

- ![](https://raw.githubusercontent.com/free-150/For-PicGo/main/202202241624401.png)

