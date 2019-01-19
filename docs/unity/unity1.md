# Unity调用Android方法
1.	首先将build.gardle中将application改为Library
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcn6lh98nj30v006qgm5.jpg)
2. 去掉build.gradle中android{}下的defaultConfig下的applicationId。
![](https://ws4.sinaimg.cn/large/006tNbRwly1fwcn7jmc0xj30r60haac9.jpg)
3. 找到unity的classes.jar包。windows下和mac下包的路径分别为 C:\ProgramFiles\Unity\Editor\Data\PlaybackEngines\AndroidPlayer\Variations\mono\Release\classes.jar /Applications/Unity/PlaybackEngines/AndroidPlayer/Variations/mono/Release/Classes\classes.jar
4. 新建MainActivity并继承UnityPlayerActivity。
5. 配置AndroidManifest.xml文件，将Android默认主题去掉，删掉values中style.xml文件，使用系统自带的主题文件。然后并配置ManActivity如下。
![](https://ws4.sinaimg.cn/large/006tNbRwly1fwcnalqpl3j31fa0o6dld.jpg)

6. 在MainActivity中编写unity调用的方法。
![](https://ws2.sinaimg.cn/large/006tNbRwly1fwcnb3baujj319m0xk0zo.jpg)
7. 生成aar包即可。
8. 在unity中assets目录中，创建Plugins->Android目录，将aar和AndroidManifest.xml放进去。
![](https://ws4.sinaimg.cn/large/006tNbRwly1fwcndah2o7j30s60dw0up.jpg)
9. 在Scripts中创建c#文件。然后，一般调用Android方法如下：

```java
AndroidJavaClass jc = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
 AndroidJavaObject jo = jc.GetStatic<AndroidJavaObject>("currentActivity"); jo.Call("showToast", "allow....code:"+code+",msg:"+msg); 

```
至于c#调用android可以谷歌自行查看。

10. 在这里使用回调的方式，java中定义一个ResultCallback接口，然后c#也要写一个对应的接口。
![](https://ws4.sinaimg.cn/large/006tNbRwly1fwcnfp8k0sj30vk0dmmyy.jpg)
![](https://ws2.sinaimg.cn/large/006tNbRwly1fwcne7b8tbj31340myjxl.jpg)
然后传到android调用的方法参数中即可。
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcngh2ecej30yk06q40f.jpg)
其中

```java
AndroidJavaClass jc = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
 AndroidJavaObject jo = jc.GetStatic<AndroidJavaObject>("currentActivity"); 

```
是固定代码。
jo.call()函数第一个参数是Android调用的方法名，方法必须定义为public，参数为回调函数，Android中对应的java接口回调即可实现。

11. unity打包事项在File中点击Build Setting。
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcnn0hx92j30k80jqn0d.jpg)
12.	选择Android，中点击Player Settings。
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcnnxnxdxj30j00w0gp5.jpg)
13. 在Other Settings中配置包名，版本号等，最小的API与TargetAPI要与Android中build.gradle中对应。
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcnonw8whj30jk08uab0.jpg)
14. 在Publishing Settings中配置一下打包签名。
![](https://ws3.sinaimg.cn/large/006tNbRwly1fwcnpho247j30jy0agjs9.jpg)
15. 配置成功后点击Build And Run即可生成apk并运行在Android设备上。
![](https://ws1.sinaimg.cn/large/006tNbRwly1fwcnqabxaxj30p00q6n08.jpg)







