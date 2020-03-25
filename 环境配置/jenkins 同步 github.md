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

用户名:服务器账号

密码:服务器密码

ID:自定义

描述:自定义

