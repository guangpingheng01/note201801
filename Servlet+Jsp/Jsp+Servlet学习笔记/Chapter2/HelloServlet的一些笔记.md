# HelloServlet的遇到的一些问题及笔记

## 问题一：

### 现象：
>在eclipse中打开Run on server 报错，端口被占用

### 原因及解决

在eclipse中运行servlet程序时，**不用在外面先打开tomcat**,而是直接Run as->Run on Server。
否则会报错，说端口被占用。

## 问题二：tomcat在eclipse中启动成功，主页却打不开

> 参考 <http://blog.csdn.net/zhanggaokai/article/details/73469473>

>参考 <http://www.cnblogs.com/mubin/p/3906684.html>

### 现象：
> tomcat在eclipse里面能正常启动，而在浏览器中访问http://localhost\:8080/不能访问，且报404错误。同时其他项目页面也不能访问。

>关闭eclipse里面的tomcat，在tomcat安装目录下双击startup.bat手动启动tomcat服务器。访问htt://localhost\:8080/能正常访问tomcat管理页面。

### 原因

eclipse将tomcat的项目发布目录（tomcat目录中的webapp）重定向了,所以你会发现在tomcat安装目录下的webapp目录里面找不到你的项目文件。

### 解决

**重新配置eclipse下tomcat服务器：**

在eclipse中的server页面，双击tomcat服务，会看到如图所示的配置页面：

![双击](https://github.com/guangpingheng01/note201801/raw/master/picture/servers.jpg)

![servers conf](https://github.com/guangpingheng01/note201801/raw/master/picture/servers-conf.gif)

其中第二项Server Locations是选择部署等相关的。此时如果该tomcat中部署了项目的话，这红圈中的选项会灰掉不能修改，要修改必须得先把tomcat中的部署的服务都移除。通过右键单击tomcat服务器选择 Add and Remove，在弹出的对话框中移除已部署的项目。移除完确定后，将看到上面的选项面板部分可编辑了。

![addandremove](https://github.com/guangpingheng01/note201801/raw/master/picture/addandremove.gif)

如果还是不能修改，那么就还是在上图的那个选项中，Clean，重新运行即可。


然后在那个服务器配置Server Locations那选择Use tomcat installation(Task control of Tomcat installation) 即选择tomcat的安装目录来作为项目的发布目录。

然后,下来四行,看到"Deploy Path"了没?它后面的值默认是"wtpwebapps",把它改成"webapps",也就是tomcat中发布项目所在的文件夹名字。
修改后关掉该页面，保存配置。这样就将项目部署到了tomcat安装目录下的webapp
重启tomcat服务器，访问http://localhost:8080则能正常访问了，自己部署的项目也能正常访问了。

如果还是不行，那么就在“Deploy path”那手动点击Browse选择你的tomcat的webapps的文件。

**如果这样设置完，在eclipse中还是不能用浏览器打开，而从外面浏览器中能打开，那就在eclipse中换一个浏览器**