## 介绍

[solo博客](https://github.com/88250/solo) 类似于hexo，一款很漂亮的博客

## 搭建

### 安装docker

[点我进行学习](/环境配置/安装docker.md)

### 安装solo

```
docker pull b3log/solo
```

### 启动容器

```
docker run --detach --name solo --network=host \
    --env RUNTIME_DB="MYSQL" \
    --env JDBC_USERNAME="root" \
    --env JDBC_PASSWORD="CL6ABhYLdDtJiPZm" \
    --env JDBC_DRIVER="com.mysql.cj.jdbc.Driver" \
    --env JDBC_URL="jdbc:mysql://hostname:port/solo?useUnicode=yes&characterEncoding=UTF-8&useSSL=false&serverTimezone=UTC" \
    --volume /home/solo/skins:/opt/solo/skins   \
    --volume /home/solo/images:/opt/solo/images \
    b3log/solo --listen_port=4000 --server_scheme=http --server_host=120.27.60.149 --server_port=4001
```

* JDBC\_USERNAME: 用户名
* JDBC\_PASSWORD: 密码
* hostname: 主机
* port: 数据库端口
* --listen\_port: 进程监听端口,一般默认访问端口
* --server\_scheme: 最终访问协议，如果反代服务启用了 HTTPS 这里也需要改为https
* --server\_host: 最终访问域名或公网 IP，不要带端口
* --server\_port: 最终访问端口，使用浏览器默认的 80 或者 443 的话值留空即可



