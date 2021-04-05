## Docker-ce安装包镜像配置

CenOS中，使用下述命令下载Docker-ce安装包镜像配置文件到指定位置。

```bash
sudo wget http://mirrors.pku.edu.cn/repoconfig/docker-ce/docker-ce.repo -O /etc/yum.repos.d/docker-ce.repo
```

修改文件后需要更新缓存：
```bash
sudo yum makecache
```
