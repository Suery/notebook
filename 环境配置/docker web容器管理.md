## 简介

为了方便管理docker，利用docker搭建docker的web管理

## 安装

### shipyard {#daocloud}

#### 概述

Shipyard也是完全基于Docker API，支持container管理、engine管理（一个engine就是监听tcp端口的docker daemon）。

优点：

```
支持多主机；
支持container及engine资源限制及图形展示；
支持container实例横向扩展；
支持批量创建，支持images，container，node节点管理；
支持创建时自动调度,动态集群，可以扩展节点规模；
在线console终端；
```

缺点：

```
不支持container批量操作。
```

#### 相关组件

> shipyard依赖的容器

* Rethinkdb容器：作为数据存储工具（用来存放账号（account）、引擎（engine）、服务密钥（service key）、 扩展元数据（extensionmetadata）等信息，但不会存储任何有关容器或镜像的内容。）
* etcd容器：作为服务发现工具
* docker-proxy：docker容器网络代理工具
* swarm：swarm管理器

#### 安装部署

```
yum install docker -y && \
systemctl start docker && \
 curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://d6f11267.m.daocloud.io
for i in alpine library/rethinkdb microbox/etcd shipyard/docker-proxy swarm shipyard/shipyard;do docker pull $i;done
```

执行安装 `curl -s https://shipyard-project.com/deploy | bash -s`

shipyard访问页面默认登录用户名：admin，密码：shipyard，登录进去后，可以在"ACCOUNTS"选项里管理用户，可以添加用户，并对用户进行角色授权。

### 添加node节点

```
curl -sSL https://shipyard-project.com/deploy | ACTION=node DISCOVERY=etcd://172.20.6.20:4001 bash -s
```

上面命令中的172.20.6.20是shipyard的部署机的ip；

## 1.4 web管理

### Container管理

可以对Container进行重启、停止、暂停、删除、扩展、重命名、提交、查看状态监控/日志、及console登录等。

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442bed296c?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442c2d9897?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442bec2b6f?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442c600d6a?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

### Images管理

可以pull为images打tag

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442c858b5b?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

### Nodes管理

![](https://user-gold-cdn.xitu.io/2019/3/5/1694bd442d8452bf?imageView2/0/w/1280/h/960/format/webp/ignore-error/1)

