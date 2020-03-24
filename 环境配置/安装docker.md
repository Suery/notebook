### 卸载旧版本

```
sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-selinux \
                  docker-engine-selinux \
                  docker-engine
```

### 使用yum安装

```
sudo yum install -y yum-utils \
           device-mapper-persistent-data \
           lvm2

sudo yum-config-manager \
    --add-repo \
    https://mirrors.ustc.edu.cn/docker-ce/linux/centos/docker-ce.repo

sudo sed -i 's/download.docker.com/mirrors.ustc.edu.cn\/docker-ce/g' /etc/yum.repos.d/docker-ce.repo
```

### 安装Docker

```
sudo yum makecache fast
sudo yum install docker-ce
curl -fsSL get.docker.com -o get-docker.sh
sudo sh get-docker.sh --mirror Aliyun
```

## 启动 Docker CE {#启动-docker-ce}

```
sudo systemctl enable docker
sudo systemctl start docker
```

### 查看容器

```
docker ps -a
```



