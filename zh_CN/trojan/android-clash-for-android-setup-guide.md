# Clash for Android 设置方法

- [Clash for Android 设置方法](#clash-for-android-设置方法)
  - [1. 下载客户端](#1-下载客户端)
  - [2. 获取订阅链接](#2-获取订阅链接)
  - [3. 添加节点(通过订阅链接)](#3-添加节点通过订阅链接)

* 文中对应客户端版本 `Clash for Android 1.2.14`
* 文中对应系统版本 `Android 10`

## 1. 下载客户端 
- 访问 [Google Play](https://play.google.com/store/apps/details?id=com.github.kr328.clash) 下载
- 访问 [Github](https://github.com/Kr328/ClashForAndroid/releases) 下载 `app-universal-release.apk` 
- 访问 [我们提供的镜像仓库 ](https://repo.trojan-cdn.com/ClashForAndroid/LatestRelease/) 下载 `clash-for-android-[版本号].apk`

## 2. 获取订阅链接

访问 [我的产品与服务](https://secure.shadowsocks.au/clientarea.php?action=services)，点击要使用的服务打开服务详情页面查看节点信息。 

获取 Clash 的订阅链接。

![portal-clash-get-link.png](/images/portal-clash-get-link.png)

详情页面介绍请查看 [如何使用我们的网站 > 服务详情页面介绍](/zh_CN/trojan/android-igniter-setup-guide.md#服务详情页面介绍)

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

## 3. 添加节点(通过订阅链接)

安装后打开首页，点击配置：

![clasha-home.jpg](/images/trojan/clash-android/clasha-home.jpg)

点击新配置：

![clasha-add-02.jpg](/images/trojan/clash-android/clasha-add-02.jpg)

点击 URL (从 URL 导入)：

![clasha-add-03.jpg](/images/trojan/clash-android/clasha-add-03.jpg)

粘贴 Clash 订阅链接，点击右上角的保存：

![clasha-add-04.jpg](/images/trojan/clash-android/clasha-add-04.jpg)

下载完成后选中配置文件，然后返回首页点击 `点此启动` 开始使用：

![clasha-add-05.jpg](/images/trojan/clash-android/clasha-add-05.jpg)

第一次启动时会请求 VPN 权限，需要点击确定允许:

![clasha-vpn-p.jpg](/images/trojan/clash-android/clasha-vpn-p.jpg)

**该弹窗为系统弹窗，与客户端无关，如果无法点击基本上是其他 APP 有在使用悬浮窗权限导致，或者是一些系统的护眼模式。**

显示运行中即表示客户端已正常启动。

![clasha-start.jpg](/images/trojan/clash-android/clasha-start.jpg)

如果需要切换节点，请点开第二个 `代理` 选项即可。
