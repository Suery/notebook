## 介绍

## 安装

### docker 安装

```
docker run --name devops-jenkins --user=root \
    -p 8080:8080 -p 50000:50000 \
    -v /opt/data/jenkins_home:/var/jenkins_home \
     -d jenkins/jenkins:lts
```



