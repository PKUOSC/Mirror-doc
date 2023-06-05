## 镜像配置

修改 `/etc/opkg/distfeeds.conf` 文件，将源地址 `downloads.immortalwrt.org` / `mirrors.vsean.net/openwrt` 更改为
`mirrors.pku.edu.cn/immortalwrt`，然后运行 `opkg update` 刷新软件包列表。

您也可以登录 LuCI 后台，进入 `系统` -> `软件包` 页面，点击 `配置 opkg` 并按上述说明完成对源地址的更改。
