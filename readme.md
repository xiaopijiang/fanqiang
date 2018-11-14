# 教程背景

由于学习，需要科学上网，使用现成的VPN不好找不说，即便找得到，稳定性也有待考证，而且VPN价格都不便宜，那么，**有成本较低且能够实现科学上网**的方式呢？

有！那就是自己搭梯子！

  用了1天的时间，各种找搭梯子的教程，搭梯子的教程往上有很多，但太过于笼统，对于小白不是很友好，且有很重要的一点：**需要购买一台境外的服务器**，比如大家推崇的搬瓦工，最低服务器也需要年付19.9美元，作为小白且脸比兜都干净的我，不免担心，万一自己搭不好，万一买到服务器不稳定，20刀岂不是白花了，毕竟这20刀可以吃好几顿肉呢^_^!

**那有没有只需几元钱，就可以学习搭梯子的方式呢？**

有的，且看教程

# 搭建教程
### 1. 购买服务器
点击此链接(https://billing.virmach.com/cart.php?gid=18),
进入到如下页面，然后选择$1.25的这款，点**Order Now**。
![图片1.png](https://upload-images.jianshu.io/upload_images/3752928-74cf4693482ff673.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如下图所示选择：

-选择$1.25 Monthly（这是月付的意思，年付会减免两个月）

-选择Ubuntu 16 64Bit（这里可以自由选择，如果你是小白，先按照教程来）

-选Los Angeles，CA（这是选择机房的位置，据说San Joe，CA（圣何塞）的机房稳定性相对最好，但很少有货，其次是Los Angeles，CA）

![图片2.png](https://upload-images.jianshu.io/upload_images/3752928-5ffa69f49b0fb366.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后在下图的标红处打钩，点击Add to Cart，走你~

![图片3.png](https://upload-images.jianshu.io/upload_images/3752928-3d10dd63def2d624.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

就会出现下图的页面：然后点击标红的Promo？（这里是输入优惠码的地方，新用户是有一次7折的机会，从1.25变成0.87就是这个原因）

![图片5.png](https://upload-images.jianshu.io/upload_images/3752928-13347803aba8caa9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

点击之后会弹出输入折扣码的对话框（对话框内会默认一个优惠码，由于我已经购买过，不算新用户，所以没有给我30%的折扣，这是我从网上找的7折优惠码：zhujiceping 终身7折， 仅限新用户，大家可以试一下，应该可以用）

![image.png](https://upload-images.jianshu.io/upload_images/3752928-fbd14aeba395b332.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

输入优惠码后点击**Validate Code**，价格就会刷新成优惠价格（这里我就使用的默认给我的20%折扣的优惠码，优惠后1刀，合人民币7块钱），之后点击**Checkout**

![image.png](https://upload-images.jianshu.io/upload_images/3752928-83af4c7ecd5a4e48.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

之后就会跳转到下面的页面。这里稍微说明一下，会有小概率你所购买的IP是被屏蔽了的，万一真的发生了这种情况，也别更换IP了，就申请退款好了。付款方式自由选择，我选择的是支付宝，记得小红框内的选择框打钩，然后点击**Complete Order**
（在填写注册信息的时候，注意记住邮箱和密码，邮箱就是登录的账号，这个过程中会给你的邮箱发一份验证邮件，你需要登录邮箱验证一下，并且在成功购买后，会把你购买的服务器信息发到你的邮箱）

![image.png](https://upload-images.jianshu.io/upload_images/3752928-da66b07e3696f354.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/3752928-43c59bc4b3da66cd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

顺利的话，付款成功后你就拥有一个海外的VPS啦~



### 2. 部署服务器

 开通服务器可能需要等几分钟，根据邮件的提示，最多不超过10分钟
 
![image.png](https://upload-images.jianshu.io/upload_images/3752928-faf1e547d4ba5d37.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


登录你的账号，会进到如下页面，点击红框的部分，进入控制台

![image.png](https://upload-images.jianshu.io/upload_images/3752928-4274281eaf73e480.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在控制台这里，你可以看到服务器的相关信息，也可以进行相应的操作，这里我们只需要确保服务器是开启的状态就可以，即 Status 显示 Online

![image.png](https://upload-images.jianshu.io/upload_images/3752928-32a3969fbeac6114.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

开启服务器后进行下一步操作：

#### 连接远程Linux服务器

Windows上推荐使用WinSCP+PuTTY（如果会用Xshell，也可以用Xshell来连接）
Mac通过Terminal远程连接Linux即可。

WinSCP下载：[WinSCP-5.13.2-Setup.exe](https://jaist.dl.sourceforge.net/project/winscp/WinSCP/5.13.2/WinSCP-5.13.2-Setup.exe)

PuTTY下载：
[putty-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.70-installer.msi)
[putty-64bit-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.70-installer.msi)

使用方法：配置主机IP地址，用户名和密码（这些信息邮件里都有），登录后，点击命令-在PuTTY中打开

[![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-4f9c2601493f3792.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0k4t1szxj20r40h2jt5.jpg)

#### 一键搭建shadowsocks
在购买VPS并用PuTTY连接上你刚购买的VPS后，你将看到如下图所示的界面：

[![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-80d66b84d3355a24.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0jnt59zlj20id0ciaao.jpg) 

1.下载一键搭建ss脚本文件，只需要执行一次，卸载ss后也不需要重新下载

    git clone https://github.com/flyzy2005/ss-fly 
2.运行搭建ss脚本代码

     ss-fly/ss-fly.sh -i password 1024

其中password换成你要设置的shadowsocks的密码即可，最好只包含字母+数字，一些特殊字符可能会导致冲突。而第二个参数1024是端口号，也可以不加，不加默认是1024。
 [![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-fbcb1cece2d116b6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0jrpq7vuj20id0cijs9.jpg) 

界面如下就表示一键搭建ss成功了：

[![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-fe194ed0bde6e16f.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0juvuqu5j20id08iwf0.jpg)

#### 一键开启BBR加速

BBR是Google开源的一套内核加速算法，可以让你搭建的shadowsocks/shadowsocksR速度上一个台阶，本一键搭建ss/ssr脚本支持一键升级最新版本的内核并开启BBR加速。

BBR支持4.9以上的，如果低于这个版本则会自动下载最新内容版本的内核后开启BBR加速并重启，如果高于4.9以上则自动开启BBR加速，执行如下脚本命令即可自动开启BBR加速：

    ss-fly/ss-fly.sh -bbr

[![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-722868a9d1411e9c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0kbjmcz5j20pf07ma9y.jpg) 

装完后需要重启系统，输入y即可立即重启，或者之后输入reboot命令重启。

判断BBR加速有没有开启成功。输入以下命令：

    sysctl net.ipv4.tcp_available_congestion_control

如果返回值为：

    net.ipv4.tcp_available_congestion_control = bbr cubic reno

后面有bbr，则说明已经开启成功了。

#### 客户端shadowsocks登录使用
**Windows客户端:** [https://github.com/shadowsocks/shadowsocks-windows/releases](https://github.com/shadowsocks/shadowsocks-windows/releases)

**Mac客户端:** [https://github.com/shadowsocks/ShadowsocksX-NG/releases](https://github.com/shadowsocks/ShadowsocksX-NG/releases)

**Linux客户端:** [https://github.com/shadowsocks/shadowsocks-qt5/wiki/Installation](https://github.com/shadowsocks/shadowsocks-qt5/wiki/Installation)

**Android/安卓客户端：**[https://github.com/shadowsocks/shadowsocks-android/releases](https://github.com/shadowsocks/shadowsocks-android/releases)

**iOS客户端：**商店搜索Wingy/shadowsocks(美国地区)下载

以Windows为例，依次填入服务器IP，服务器端口，密码（此处的端口和密码是你运行 ss-fly/ss-fly.sh -i password 1024命令时设置的端口和密码），保存配置

[![一键脚本搭建SS/搭建SSR服务并开启BBR加速](http://upload-images.jianshu.io/upload_images/3752928-72eb9ed4571fc361.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)](https://ws1.sinaimg.cn/large/77c76f11gy1fs0jj5rdzij20ct0cet8z.jpg) 

在状态栏右击shadowsocks，勾选开机启动和启动系统代理，在系统代理模式中选择PAC模式，服务器->编辑服务器，一键安装shadowsocks的脚本默认服务器端口是1024，加密方式是aes-256-cfb，密码是你设置的密码，ip是你自己的VPS ip，保存即可。






