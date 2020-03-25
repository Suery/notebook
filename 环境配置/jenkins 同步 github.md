## 介绍

```
利用jenkins 自动化部署github，这样只需要在本地提交项目到github就可以了，剩下的全交给Jenkins自动部署
```

## 

## 配置github

### webhooks

> payload url 后面会配置到，等会过来配置

![](/assets/jtbg-1.png)

![](/assets/jtbg-2.png)

### 

### access tokens

点击在右上角**settings**，剩下如下操作

![](/assets/jtbg-5.png)

![](/assets/jtbg-3.png)

> 注意，记下当前密钥

## jenkins配置

如下操作

![](/assets/jtbg-6.png)

### 配置ssh

* 先填下对应信息

![](/assets/jtbg-7.png)

* 然后配置凭据

![](/assets/jtbg-8.png)

* 用户名:服务器账号
* 密码:服务器密码
* ID:自定义
* 描述:自定义

然后在Credentials选择刚才创建的凭据，然后点击Check connection会出现如下类似信息

```
Successfull connection
```

### GitHub配置

点击高级选项，然后先配置如下信息

![](/assets/jtbg-10.png)

* 在Hook URL处的ur记住，这个地址应该填在上面所述的payload url 处
* 名称:自定义
* API URL:不能修改
* 凭据:如下



![](/assets/jtbg-11.png)

* secret：填写刚才在github生成的密钥
* ID:自定义
* 描述:自定义



### Git配置

![](/assets/jtbg-12.png)



### 

### Publish over SSH

步骤简单，就不说了

![](/assets/jtbg-13.png)



### 创建Job

点击首页的新建任务，自定义任务名称，然后选择构建一个自由风格的软件项目



填写如下

#### github 配置

![](/assets/jtbg-14.png)

#### git 配置

![](/assets/jtbg-15.png)









