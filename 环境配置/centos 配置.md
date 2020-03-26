### 修改主机名

```
hostname <hostname> # hostname 是主机名 # 这个方法重启系统后就会失效
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

## 上传和下载

* 首先安装lrzsz

```
yum -y install lrzsz
```

* 上传文件，执行命令rz，会跳出文件选择窗口，选择好文件，点击确认即可。
* 下载文件，执行命令sz



