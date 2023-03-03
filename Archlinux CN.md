## 镜像配置

在 `/etc/pacman.conf` 文件末尾添加以下两行：
```unix-conf
[archlinuxcn]
Server = https://mirrors.pku.edu.cn/archlinuxcn/$arch
```
以添加并启用北大 Arch Linux CN 镜像源

之后用 `-Sy` 安装 `archlinuxcn-keyring` 包导入 GPG key：
```bash
sudo pacman -Sy archlinuxcn-keyring
```

最后执行命令：
```bash
sudo pacman -Syyu
```
强制刷新软件包列表
