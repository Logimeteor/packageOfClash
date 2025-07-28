# 版本对应关系

## ubuntu

- ubuntu 20 —— 1.7.3
- ubuntu 22 —— 2.0.3 
- ubuntu 24 —— 2.3.2

## 



# 翻墙教程分为三大步：买流量、下软件、流量配置到软件上

***这里的表达都是自己乱写的，具体原理是啥，我也懒得去看，大概效果就是我说的那样\***

## 一、买流量

**我买的流量是15元130G，不限时间，从去年10月份开始用，一直用到现在，还剩下80多G，期间电脑常挂，手机偶尔，平板偶尔，但消耗确实很小。如果你不太放心，也可以选择1元的2G流量作个尝试。**

#### 下面是我买流量的网站（两个地址其实差不多，都是同一个地方）

https://mojie.me/#/login

https://xn--zuup71g88ae4i.com/

只需要去注册，订阅即可



## 二、下软件

**买流量了之后还需要下载软件进行托管，后面需要翻墙的时候只需要打开软件启动即可**

这里我推荐无论是手机、电脑、还是平板都用clash这款软件。（因为我自己只用过这款软件）

具体的安装包下载网址如下：

> ubuntu ：[Releases · zzzgydi/clash-verge](https://github.com/zzzgydi/clash-verge/releases)
>
> windows: https://github.com/zzzgydi/clash-verge/releases/download/v1.3.8/Clash.Verge_1.3.8_x64-setup.exe
>
> 手机：https://github.com/clashbk/clash_for_android/releases , 然后下载仓库中的apk后缀文件

为方便下载，我把需要用到的安装包放到国内 gitee 仓库和国外的 github 中，方便各位自取

> gitee ：https://gitee.com/logimeteor/package-of-clash.git
>
> github: https://github.com/Logimeteor/packageOfClash.git

​	

windows 一般随便下最新版，但是 ubuntu 上需要根据 ubuntu 版本来进行专门下载，下面是目前已知的适配关系

> ubuntu 20.04 —— 1.7.3 版本可用
>
> ubuntu  22.04 —— 2.0.3 版本可用
>
> ubuntu 24.04 —— 2.3.2 版本可用





**windows** 下载比较简单，这里就不说了，

**ubuntu** 下载过程如下：

```sh
sudo apt update #这条命令只要在 ubuntu 下载之后执行一次就够了，如果之前执行过就不需要再执行了
sudo dpkg -i ****.deb #后面省略的是安装包具体的名字，大概率报错，缺少依赖软件，大概是 lib** 的一个软件，下面就下载这个软件即可
sudo apt install lib* #这样依然会报错，此时会有 --fix-broken install 的提示信息，下面执行这条命令即可
sudo apt --fix-broken install #执行命令之后，如果显示让你确认是否安装，说明ubuntu可以安装这个版本的 clash，此次安装成功，如果显示让你确认是否卸载，那么说明这个 clash 不适配该版本的 ubuntu，此次安装失败
```



>  



## 配置（其实主要就是按照 mojie 的使用文档去做，需要图片参考的话请下载仓库中的 pdf 文件）

**下载好之后，就是把自己的买的流量给挂上去，具体操作其实在那个流量网站里面就有，这里我以windows举例，大概说一下，其实我自己也是看使用说明的才会的**

![image-20250718113419561](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718113419561.png)

**进入教程之后，按照说明的操作**

![image-20250718113441562](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718113441562.png)

接着按照说明进行设置

![image-20250718113511850](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718113511850.png)



设置好之后，只需要打开软件打开系统代理即可

![image-20250718113529694](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718113529694.png)



手机中进行类似的配置之后，使用的时候只需要点击启动即可

 ![image-20250718113538517](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718113538517.png)



 

 

# 使用注意事项

​	无论是 windows  还是 linux ，如果已经开始使用该软件进行翻墙操作，并且关机的时候依然打开了软件中的系统代理功能，那么下次开机时必须先打开该软件才能正常访问互联网，否则连国内网站都访问不了。

# 特别补充，ubuntu 上 openssl 对软件的重要作用

**补充实验**

​	本人后面为了验证 openssl 的神奇作用，又把这个软件给卸载了，结果发现 clash-verge 同时消失。而当我下载了 openssl 之后，再下载 clash-verge，整个过程没有任何阻碍。

​	这证明了 openssl 的安装，对于 clash-verge 非常重要。

**补充问题**

​	之后还遇到过配置文件无法导入的问题，具体现象是点击保存一直报错，这里的解决方法是疯狂点击多次
![image-20250718114153561](C:\Users\华硕\AppData\Roaming\Typora\typora-user-images\image-20250718114153561.png)

