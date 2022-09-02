
修改/etc/yum.repos.d/openEuler.repo中的地址，指向https://mirrors.pku.edu.cn/openeuler
具体命令为：
```
sudo sed  -e "s|http://repo.openeuler.org|https://mirrors.pku.edu.cn/openeuler|g" \
          -i.bak \
          /etc/yum.repos.d/openEuler.repo
```
