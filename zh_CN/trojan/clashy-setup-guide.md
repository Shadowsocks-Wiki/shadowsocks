# 【Windows / macOS / Linux】Clashy 设置方法
- [【Windows / macOS / Linux】Clashy 设置方法](#windows--macos--linuxclashy-设置方法)
  - [1. 下载客户端](#1-下载客户端)
  - [2. 安装与运行](#2-安装与运行)
  - [3. 客户端界面](#3-客户端界面)
  - [4. 添加节点](#4-添加节点)
    - [4.1 获取订阅链接](#41-获取订阅链接)
    - [4.2 添加订阅](#42-添加订阅)
  - [5. 使用介绍](#5-使用介绍)
    - [5.1 模式选择](#51-模式选择)
    - [5.2 端口设置](#52-端口设置)
  - [6. Edge / Chrome / Firefox 配合 SwitchyOmega 扩展](#6-edge--chrome--firefox-配合-switchyomega-扩展)

- 截图对应客户端版本 `Clashy 0.1.16`
- 截图对应系统为 `Windows 10` / `macOS 10.15.1` / `Ubuntu 20.04`

## 1. 下载客户端

- GIthub：https://github.com/SpongeNobody/Clashy/releases
- 访问 https://dl.trojan-cdn.com/trojan/ 下载  
- Windows 下载 `Clashy-版本号.exe`
- macOS 下载 `Clashy-版本号.dmg`
- Linux 下载 `Clashy-版本号.AppImage`

## 2. 安装与运行

- Windows 直接打开 Clashy-xx.exe
- Linux 为 Clashy-xx.AppImage 添加运行权限后直接打开即可
- macOS 打开 Clash-xxx.dmg 后，将客户端拖入 Applications 文件夹中，随后在启动台中打开客户端，然后点击右上角客户端 ![icon-clasy.png](/images/icon-clashy.png) 图标，再点击 Show Clashy 即可打开客户端主界面。

## 3. 客户端界面

![clashy-home-win.png](/images/trojan/clashy/clashy-home-win.png)  

- [查看 macOS 系统截图](/images/trojan/clashy/clashy-home-mac.png)  
- [查看 Ubuntu 系统截图](/images/trojan/clashy/clashy-home-ubuntu.png)  

## 4. 添加节点

### 4.1 获取订阅链接

首先前往产品服务详情页面获取 Clash 的订阅链接。

![portal-clash-get-link.png](/images/portal-clash-get-link.png)

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

### 4.2 添加订阅

点击左侧 `Profiles` 标签，在底部粘贴订阅链接，点击 `Save` ，等待配置下载完成后选择对应配置文件。

一般情况下此时开启客户端的系统代理即可正常使用(开启方法请看后文修改设置部分)。

前往 `Proxies` 页面可以选择需要使用的节点。

![clashy-add-config-win.png](/images/trojan/clashy/clashy-add-config-win.png)  

- [查看 macOS 系统截图](/images/trojan/clashy/clashy-add-config-mac.png)  
- [查看 Ubuntu 系统截图](/images/trojan/clashy/clashy-add-config-ubuntu.png)  

## 5. 使用介绍

### 5.1 模式选择

- `GLOBAL`：全局模式
- `RULE`：按照规则切换
- `DIRECT`：直连，不使用代理

![clashy-settings-win.png](/images/trojan/clashy/clashy-settings-win.png) 

- [查看 macOS 系统截图](/images/trojan/clashy/clashy-settings-mac.png) 
- [查看 Ubuntu 系统截图](/images/trojan/clashy/clashy-settings-ubuntu.png) 


### 5.2 端口设置

如果导入本站提供的浏览器扩展 Proxy SwitchyOmega 的配置文件，将 Socks 端口修改为 `1080` 即可使用。

## 6. Edge / Chrome / Firefox 配合 SwitchyOmega 扩展

参考下面教程通过安装浏览器扩展使用（支持 Chrome / Firefox / 新版 Edge 浏览器）

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)  