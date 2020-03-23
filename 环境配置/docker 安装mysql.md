### 安装mysql5.7版本

```
docker pull mysql:5.7
```

### 启动容器

```
docker run --name mysql5.7 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.7
```

* MYSQL\_ROOT\_PASSWORD为设置的初始密码
* -p 3306:3306:主机端口与容器端口



