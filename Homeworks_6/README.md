# 广播，自定义广播的使用。



## 动态注册广播接收器：新建一个类，继承BroadcastReceiver，并重写onReceive方法，当接收到广播时方法执行。

注意问题：

必须配置相应的权限声明，否则程序将直接崩溃。





### 接收系统广播，动态注册监听网络变化



![image-20201114162742487](README.assets/image-20201114162742487.png)



![image-20201114162800941](README.assets/image-20201114162800941.png)

打开和关闭数据网络时可以看到相应的提示，证明创建的广播接收器成功接收到系统发来的广播。







## 静态注册广播接收器：在AndroidManifest.xml中注册

![image-20201114171101386](README.assets/image-20201114171101386.png)

开机时可以出现相应的提示信息，证明创建的广播接收器成功接收到系统发来的广播。



## 发送自定义广播



### 点击按钮发送标准广播

![image-20201114172627778](README.assets/image-20201114172627778.png)

可以看到相应的提示信息，证明发送的自定义标准广播成功被接收。



### 按钮新增发送本地广播，即点击按钮发送全局广播和本地广播。

#### 本程序接收到了两种广播，分别是全局广播和本地广播。

![image-20201114174344532](README.assets/image-20201114174344532.png)![image-20201114174529290](README.assets/image-20201114174529290.png)



另一个程序BroadcastTest_1（程序已经实现接收这两个广播的功能）只接收到一条广播（全局广播），另一条本地广播未成功接收到。

![image-20201114175719123](README.assets/image-20201114175719123.png)

由此验证了本地广播只会在自身程序内传播。