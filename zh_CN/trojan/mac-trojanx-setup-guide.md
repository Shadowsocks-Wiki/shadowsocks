# macOS 下 TrojanX 设置方法

- [macOS 下 TrojanX 设置方法](#macos-下-trojanx-设置方法)
  - [1. 下载/安装客户端](#1-下载安装客户端)
    - [1.1 下载](#11-下载)
    - [1.2 安装](#12-安装)
  - [2. 查看节点信息](#2-查看节点信息)
  - [3. 添加节点](#3-添加节点)
    - [3.1 手动添加](#31-手动添加)
    - [3.2 扫码添加](#32-扫码添加)
    - [3.3 剪贴板导入](#33-剪贴板导入)
  - [4. 配置系统代理模式](#4-配置系统代理模式)
  - [5. 设置浏览器扩展](#5-设置浏览器扩展)

- 截图对应的客户端版本 `TrojanX-0.3.zip`
- 截图对应系统版本为 `macOS 15.1`

## 1. 下载/安装客户端

### 1.1 下载
访问右侧的链接下载 `TrojanX-[版本号]-macOS.zip` ：[https://dl.trojan-cdn.com/trojan/](https://dl.trojan-cdn.com/trojan/)

### 1.2 安装

找到刚才下载的 ZIP 文件并解压得到 TrojanX (一般在托盘的下载文件夹中点击 `TrojanX-[版本号]-macOS.zip` 后会自动解压并弹出文件窗口)。
将 TrojanX 文件拖动至应用程序中。

![trojanx-install.gif](/images/trojan/trojanx/trojanx-install.gif)

然后找到应用程序中的 TrojanX ，初次打开时会提示无法验证开发者，点击取消，然后按照下面图片所示在 Finder(访达) 中的应用程序文件夹中找到 TrojanX 右键选择打开。

![trojanx-install-02.png](/images/trojan/trojanx/trojanx-install-02.png)

右键选择打开。

![trojanx-install-03.png](/images/trojan/trojanx/trojanx-install-03.png)

系统会再次确认，请选择打开。

![trojanx-install-04.png](/images/trojan/trojanx/trojanx-install-04.png)

第一次打开时需要输入用户密码进行授权，输入密码后点击好。

![trojanx-install-05.png](/images/trojan/trojanx/trojanx-install-05.png)

打开后可以在右上角找到 ![icon-trojanx-indicator.png](/images/trojan/trojanx/icon-trojanx-indicator.png) 样式的客户端图标。

## 2. 查看节点信息

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

在节点信息最后一列：

- 点击二维码图标 ![icon-qrcode.png](/images/icon-qrcode.png) 即可显示对应的二维码
- 点击齿轮图标 ![icon-config.png](/images/icon-config.png) 即可获得对应的 Trojan URL

![portal-get-qr-or-url.png](/images/portal-get-qr-or-url.png)

## 3. 添加节点

目前 TrojanX 客户端不支持批量导入客户端，当前推荐使用 `扫码` / `剪贴板导入` 的方式添加客户端。

### 3.1 手动添加

右上角点击客户端图标，在菜单中点击 `服务器` > `服务器设置` ，打开服务器窗口。
按照自己的服务器信息填写后点击确定。

![trojanx-add-server.png](/images/trojan/trojanx/trojanx-add-server.png)

### 3.2 扫码添加

在服务详情页面，点击 ![icon-qrcode.png](/images/icon-qrcode.png) 打开需要添加的节点的二维码后，点击客户端菜单中的 `扫码屏幕上的二维码` 。

![trojanx-addby-qr.png](/images/trojan/trojanx/trojanx-addby-qr.png)

macOS 15 中扫码需要授权给客户端屏幕录制权限，否则会提示找不到二维码。   

![trojanx-addby-qr-02.png](/images/trojan/trojanx/trojanx-addby-qr-02.png)

需要在系统设置中进行权限设置，打开 `系统偏好设置` > `安全与隐私` ，在隐私标签中，左侧找到屏幕录制，勾选 `TrojanX` 。

![trojanx-qr-privacy.png](/images/trojan/trojanx/trojanx-qr-privacy.png)

当客户端菜单顶部显示 `Trojan: On` 时，表示 TrojanX 已经启用。

### 3.3 剪贴板导入

在服务详情页面，点击 ![icon-config.png](/images/icon-config.png) 打开需要添加的节点的服务器配置页面复制 Trojan URL。

之后点击客户端菜单中的 `从剪贴板导入服务器配置链接` 即可。

![trojanx-addby-url.png](/images/trojan/trojanx/trojanx-addby-url.png)

## 4. 配置系统代理模式

点击屏幕右上方菜单栏的 ![icon-trojanx-indicator.png](/images/trojan/trojanx/icon-trojanx-indicator.png) > `PAC 自动模式`。

![trojanx-set-pac.png](/images/trojan/trojanx/trojanx-set-pac.png)

- `PAC模式`： 表示可以实现自动代理，及本来可以访问的网站不会经过代理，推荐日常使用。
- `全局模式`： 表示计算机内大多数流量都会经过代理，不推荐日常使用。
- `手动模式`： 不设置系统代理，浏览器需要配合扩展才可以使用
- Safari 需要使用系统代理， Firefox / Chrome 在没有安装代理扩展的情况下默认使用的也是系统代理

## 5. 设置浏览器扩展

TrojanX 默认提供的本地 Socks5 监听端口为 1080 ，一般情况下不需要做改动，如果有同时运行其他 Shadowsocks / V2ray 的客户端可能存在冲突，所以不要同时运行多个代理客户端。

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)  