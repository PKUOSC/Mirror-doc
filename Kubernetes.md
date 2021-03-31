## Kubernetes镜像配置

CenOS中，创建Kubernetes镜像配置文件`/etc/yum.repos.d/kubernetes.repo`。

文件内容为：
```bash
[kubernetes]
name=kubernetes
baseurl=https://mirrors.pku.edu.cn/kubernetes/yum/repos/kubernetes-el7-$basearch
enabled=1
```

修改文件后需要更新缓存：
```bash
sudo yum makecache
```
