
# Cordova初探
Apache Cordova是一个开源的移动开发框架。允许你用标准的web技术-HTML5,CSS3和JavaScript做跨平台开发。应用在每个平台的具体执行被封装了起来，并依靠符合标准的API绑定去访问每个设备的功能，比如说：传感器、数据、网络状态等。
<!--more-->
## Cordova适用人群
* 移动应用开发者，想扩展一个应用的使用平台，而不通过每个平台的语言和工具集重新实现。
* web开发者，想包装部署自己的web App将其分发到各个应用商店门户。
* 移动应用开发者，有兴趣混合原生应用组建和一个WebView(一个特别的浏览器窗口) 可以接触设备A级PI，或者你想开发一个原生和WebView组件之间的插件接口。

## Cordova架构
![](http://ww2.sinaimg.cn/large/0060lm7Tly1fjvnvv40vcj30nf0ijgmp.jpg)

## Cordova环境搭建
1. 下载和安装Node.js。安装完成后你可以在命令行中使用node和npm。
2. 安装JDK和Android SDK，并配置相关的环境变量。同时添加Android SDK的tools和platform-tools目录到环境变量中。
3. 安装Android Studio，并将其中的Gradle配置到环境变量中。
4. 安装cordova模块使用Nodejs的npm工具。cordova模块会被npm工具自动下载。
	```java
	npm install -g cordova
	```
	-g标志是告诉 npm 我们全局安装 cordova。否则我们将会安装在当前工作目录的 node_modules子目录。安装完成后，你应该能够在命令行中运行cordova命令，在没有任何参数的时候会打印一些帮助信息。
5. 创建APP，通过输入以下命令创建App。
	```java
	cordova create MyApp com.example.shuaijie HelloWorld
	```
	其中后面三个参数分别为：创建项目的目录，项目的包名，项目名称。
6. 添加平台，所有后续命令都需要在项目目录或者项目目录的任何子目录运行。
	```java
	cordova platform add android --save //添加android平台
	cordova platform add ios --save //添加ios平台
	cordova platform ls //检查当前平台设置状况:
	```
7. 检测是否满足构建平台的要求:
	```java
	cordova requirements
	```
	要构建和运行App，你需要安装每个你需要平台的SDK，此命令查看所需平台的SDK是否安装。
8. 构建APP
	```java
	cordova build //此命令是为所有平台构建
	cordova build android //此命令只构建android平台
	```
9. 测试APP
	移动平台的SDK通常会绑定模拟器，它是一个可执行的设备镜像，这样你就可以在主屏幕启动你的App，看看它在多个平台是如何交互的。 在命令行运行下面的命令，会重新构建App并可以在特定平台的模拟器上查看。
	```java
	cordova emulate android
	```
	或者，你可以将你的手机插入电脑，在手机上直接测试App。
	```java
	cordova run android
	```