## Docker-ce安装包镜像配置

Debian/Ubuntu 用户

以下内容根据 [官方文档](https://docs.docker.com/engine/install/debian/) 修改而来。

如果你过去安装过 docker，先删掉:

```
sudo apt-get remove docker docker-engine docker.io containerd runc
```

首先安装依赖:

```
sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common
```

根据你的发行版，下面的内容有所不同。你使用的发行版： 

### Ubuntu

信任 Docker 的 GPG 公钥:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

添加软件仓库:

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://mirrors.pku.edu.cn/docker-ce/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

最后安装

```
sudo apt-get update
sudo apt-get install docker-ce
```

### Debian

信任 Docker 的 GPG 公钥:

```
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

添加软件仓库:

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://mirrors.pku.edu.cn/docker-ce/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

最后安装

```
sudo apt-get update
sudo apt-get install docker-ce
```