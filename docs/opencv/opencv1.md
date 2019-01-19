# opencv在ios平台上的使用教程
## 环境搭建
首先在[opencv下载地址](https://sourceforge.net/projects/opencvlibrary/files/)中下载ios版的opencv库。
![](https://ws1.sinaimg.cn/large/006tNbRwgy1fufz58s6mxj31kw0k5goi.jpg)

点进文件夹中，可以看到多个版本的opencv库。
![](https://ws1.sinaimg.cn/large/006tNbRwgy1fufz6prftfj31ki0x40x9.jpg)

选择其中一个版本点进去下载即可。
![](https://ws4.sinaimg.cn/large/006tNbRwgy1fug08hkhkrj31je0guabw.jpg)

下载完framework之后，在xcode中新建一个文件夹，然后将文件放进去，出现以下提示，注意勾选。
![](https://ws1.sinaimg.cn/large/006tNbRwgy1fug0c8g5ryj315e0oe40w.jpg)

现在就能在TARGETS中Build Phases下的Link Binary With Libraries中看到有一个库添加进去了。
![](https://ws4.sinaimg.cn/large/006tNbRwgy1fug0f1notqj31ck0hoju1.jpg)



