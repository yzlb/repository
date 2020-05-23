# [GitHub上提交代码完整教程]

**提交步骤：**

1、创建github repository(仓库) 

2、安装git客户端

3、为Github账户设置SSH key

4、上传本地项目到github

## 一、创建github repository(仓库)

**1.1、登录GitHub**

github的官方网址：https://github.com ，如果没有账号，赶紧注册一个。

点击Sign in进入登录界面，输入账号和密码登入github。

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711135555599-461995350.png)

 

 

**1-2 创建repository(仓库--简明明了的就是新建一个空间来存放我们项目代码的地方)**

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711140028506-1779404486.png)

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711140627867-638127161.png)

创建成功后，就可以看到自己的仓库地址，如下图：

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711141617973-1944726102.png)

## 二、安装git客户端（git下载地址https://git-scm.com/downloads）

**2.1下载git**

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711142200147-1723347259.png)

 

 

**2.2、 安装客户端**

下载好之后咋们开始安装吧，欢迎界面，下一步。

选择安装路径，千万别选带中文的路径，有时候会引起不必要的误会。

一直next，最后finish就OK

**2.3、绑定用户**

打开git-bash.exe，（在你的项目文件夹所在的地址右键点击，弹出窗口。）

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711143037151-27293512.png)

 

因为Git是分布式版本控制系统，所以需要填写用户名和邮箱作为一个标识，用户和邮箱为你github注册的账号和邮箱

提示（配置的帐号名和邮箱一定要与GitHub相同，不然会提交失败）

 git config --global user.name "@@@"   (GitHub相对应的帐号名称)

 git config --global user.email "123@163.com" （GitHbu相对应的邮箱帐号）

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711145256123-1576130239.png)

 

## 三、为Github账户设置SSH key

**3.1、 生成ssh key**

首先检查是否已生成密钥 cd ~/.ssh，ls如果有3个文件，则密钥已经生成，id_rsa.pub就是公钥

 ![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711145416020-932560671.png)

 

如果没有，输入: ssh-keygen -t rsa -C "你的邮箱"

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711155135006-458973993.png)

 

**3.2、复制ssh key**

 方法1: 输入 clip < ~/.ssh/id_rsa.pub  会自动复制ssh key，可以直接粘贴

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711150857630-1321965671.png)

 方法2:在c/Users/Administrator/.ssh/id_rsa)文件找到直接复制

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711150932612-1478161474.png)

 

 

**3.3、连接github，打开GitHub 进入setting找到ssh key并新建**

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711151830920-877566481.png)

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711152017912-1651603673.png)

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711152242633-1972966452.png)

 

**3.4、然后测试连接是否成功**

输入: ssh -T git@github.com 

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711152508736-450105130.png)

 

**3.5、进入本地要提交项目文件的的所在位置右键点击打开Git Bash Here 或者在当前命令窗口 执行 cd F:\test 进入目录。**

 然后依次执行

　1、git init  

  2、git add .

  3、git commit -m "提交描述"

  4、git remote add origin https://github.com/MyJoanna/test.git  （这里的 https://github.com/MyJoanna/test.git 是你的仓库地址）

  5、git push -u origin master  

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711154006660-1638758494.png)

 

最后我们就可以在GitHub的仓库上看到我们提交上去的代码了

![img](https://img2018.cnblogs.com/blog/774824/201907/774824-20190711154725695-1110829177.png)

 