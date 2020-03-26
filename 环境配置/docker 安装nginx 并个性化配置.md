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

* -p 80:80：将容器的80端口映射到主机的80端口

* --name mynginx：将容器命名为mynginx

* -v $PWD/www:/www：将主机中当前目录下的www挂载到容器的/www

* -v $PWD/conf/nginx.conf:/etc/nginx/nginx.conf：将主机中当前目录下的nginx.conf挂载到容器的/etc/nginx/nginx.conf。nginx容器启动时会使用该conf配置文件。conf配置文件中所使用的路径必须都是容器中的路径，这些路径对应的主机内容，可以通过 -v 来映射

* -v path:path

  * 主机目录映射到容器目录

* 查看运行情况

docker ps

