## 查询nginx

```
docker search nginx
```

## 下载nginx

```
docker pull nginx
```

### 运行 nginx

```
docker run -p 80:80 --name mynginx -v $PWD/www:/www -v $PWD/conf/nginx.conf:/etc/nginx/nginx.conf -v $PWD/logs:/wwwlogs  -d nginx
```

命令说明：

* -v 主机path:容器path

  * 主机目录映射到容器目录

* -p 主机port:容器port：

  * 将容器的端口映射到主机的端口

    * --name mynginx：将容器命名为mynginx

    * -v $PWD/www:/www：将主机中当前目录下的www挂载到容器的/www

    * -v $PWD/conf/nginx.conf:/etc/nginx/nginx.conf

      * 重要配置，将

## 查看运行情况

```
docker ps
```



