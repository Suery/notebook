### 修改主机名

```
hostname <hostname>
```

## 安装nodejs

```
curl --silent --location https://rpm.nodesource.com/setup_8.x | sudo bash -

sudo yum -y install nodejs
```

### 更新npm ：

```
npm install -g npm
```

### 更新node版本：

```
先清除npm缓存：
    npm cache clean -f

然后安装n模块：
    npm install -g n

升级node.js到最新稳定版：
    n stable
```

## 宝塔

#### 安装

```
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
```

#### Linux面板7.1.0升级命令：

```
curl http://download.bt.cn/install/update6.sh|bash
```

### 访问

```
端口默认为8888
```

### 上传和下载

* 首先安装lrzsz

```
yum -y install lrzsz
```

* 上传文件，执行命令rz，会跳出文件选择窗口，选择好文件，点击确认即可。
* 下载文件，执行命令sz



