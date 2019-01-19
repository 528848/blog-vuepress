# xcode中git连接Github教程
代码版本控制是开发者开发过程中必不可少的环节，xcode中已经将Git作为内置的源代码控制（Source Control）工具了，接下来讲述一下如何与Github连接。

## 安装Git并生成ssh

如果你要使用Git，那么首要任务是安装一个Git，并生成一个ssh私钥，这里不再作陈述，不会的同学可以去Google。

## 创建git源

打开xcode，创建一个项目，输入项目的相关信息后一直点击下一步，在创建工程的最后一步Xcode会有一个复选框Create Git repository on my Mac，如果选择了它，git源就会被添加到工程目录中。例子如下：

![](https://ws4.sinaimg.cn/large/006tKfTcgy1fo26ob2lb9j30zq0h0dhl.jpg)



## 连接github

首先你要有一个Github，然后在Github中创建一个仓库，记住不要点击生成README.md文件，最后拿到仓库的ssh地址。

![](https://ws4.sinaimg.cn/large/006tKfTcgy1fo26vkf4ouj30qa0f4ac6.jpg)

然后打开命令行，进入到项目目录中，输入命令：git remote add origin git@github.com:codeteenager/ShareDemo.git，即可连接到github中。接下来你就可以使用xcode自带的Source Control进行代码的拉取和提交了