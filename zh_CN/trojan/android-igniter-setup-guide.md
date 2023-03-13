# Android 客户端 igniter 设置方法

- [Android 客户端 igniter 设置方法](#android-客户端-igniter-设置方法)
  - [1. 下载客户端](#1-下载客户端)
  - [2. 查看节点信息](#2-查看节点信息)
  - [3. 添加节点](#3-添加节点)
    - [3.1 手动添加](#31-手动添加)
      - [3.1.1 直接添加](#311-直接添加)
      - [3.1.2 通过 Trojan URL 添加](#312-通过-trojan-url-添加)
    - [3.2 扫码添加](#32-扫码添加)
    - [3.3 导入配置文件(批量添加)](#33-导入配置文件批量添加)
  - [4 节点的保存、载入与更换](#4-节点的保存载入与更换)

* 文中对应客户端版本 `igniter-0.9.4-beta`
* 文中对应系统版本 `Android 10`

## 1. 下载客户端
- [Google Play](https://portal.shadowsocks.nz/clientarea.php?action=productdetails&id=1212815)
- 访问 [我们提供的镜像仓库 ](https://repo.trojan-cdn.com/igniter/LatestRelease/) 下载 `igniter-[版本号]-universal-release.apk` 
- 访问 [Github Releases](https://github.com/trojan-gfw/igniter/releases) 下载 `xxx-universal-release.apk`

## 2. 查看节点信息

访问 [我的产品与服务](https://portal.shadowsocks.nz/clientarea.php?action=services)，点击要使用的服务打开服务详情页面查看节点信息。  

详情页面介绍请查看 [如何使用我们的网站 > 服务详情页面介绍](/zh_CN/trojan/android-igniter-setup-guide.md#服务详情页面介绍)

## 3. 添加节点
### 3.1 手动添加
首页选项说明：  
```
Remote Address: 服务器地址 
Remote Port: 服务器端口（默认为443） 
Password： 服务器密码 

Enable IPv6: 是否开启 IPv6 
Verify Certificate: 是否验证证书 
Exempt Chinese Domain/IPs: 是否代理中国大陆的网站
```

#### 3.1.1 直接添加
按照图中的标注填写后点击 `START` 启动。    
![igniter-add-server.png](/images/trojan/igniter/igniter-add-server.png)

#### 3.1.2 通过 Trojan URL 添加
首先在产品详情页面点击 ![icon-config.png](/images/icon-config.png) 按钮，获取节点对应的 Trojan URL。  

![portal-get-qr-or-url.png](/images/portal-get-qr-or-url.png)

然后打开客户端会提示是否导入，选择 `CONFIRM` 确认导入，然后点击 `START` 启动。   

![igniter-url-import-confirm.png](/images/trojan/igniter/igniter-url-import-confirm.png)

添加完成点击 START 即可，初次连接时系统会确认 VPN 权限，请选择允许。  
(该弹窗为系统弹窗，与客户端无关，如果无法点击基本上是其他 APP 有在使用悬浮窗权限导致，或者是一些系统的护眼模式)

![igniter-vpn-p.png](/images/trojan/igniter/igniter-vpn-p.png)


### 3.2 扫码添加
点击菜单 ![icon-menu.png](/images/icon-menu.png) 按钮，再点击 `Load Server` 打开节点列表页面，再点击顶部的二维码 ![icon-qr.png](/images/icon-qr.png) 按钮打开扫码界面进行扫码添加。

![igniter-add-by-qr.png](/images/trojan/igniter/igniter-add-by-qr.png)

### 3.3 导入配置文件(批量添加)
首先将 Lite / Pro 服务的 `gui-config.json` 配置文件下载到手机上，将文件名后缀修改为 `.txt` 。

![add-by-file.png](/images/portal-get-gui-config.png)

点击客户端顶部的菜单 ![icon-menu.png](/images/icon-menu.png) 按钮，再点击 `Load Server` 打开节点列表页面。

再次点击顶部菜单 ![icon-menu.png](/images/icon-menu.png) 按钮，选择 `Import from file` ，选择刚才下载配置文件即可。

![igniter-add-by-file.png](/images/trojan/igniter/igniter-add-by-file.png)

## 4 节点的保存、载入与更换
- `保存节点`：点击 ![icon-menu.png](/images/icon-menu.png) 按钮，再点击 `Save Server` 保存。
- `载入、更换节点`：点击 ![icon-menu.png](/images/icon-menu.png) 按钮，再点击 `Load Server` 打开节点列表页面，选择要使用的节点。