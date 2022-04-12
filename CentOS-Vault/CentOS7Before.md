## 镜像配置

该版本提供CentOS以不再维护的版本的镜像。
首先在服务器上运行``cat /etc/redhat-release``命令获取操作系统小版本号，比如``7.9.2009``
1. 使用命令修改
```
mirrorver=7.9.2009  #这里使用上面命令获取到的小版本号
sudo sed -e 's|^mirrorlist=|#mirrorlist=|g' \
          -e 's|^#baseurl=http://mirror.centos.org/centos/\$releasever|baseurl=https://mirrors.pku.edu.cn/centos-vault/$mirrorver|g' \
          -i.bak \
          /etc/yum.repos.d/CentOS-*.repo
```
2. 手动将``/etc/yum.repos.d/CentOS-*.repo``文件中baseurl=行取消注释并改为北大源地址http://mirrors.pku.edu.cn/centos-vault/${小版本号}开头。
