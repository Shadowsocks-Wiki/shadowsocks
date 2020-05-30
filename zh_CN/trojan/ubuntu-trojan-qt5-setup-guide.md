# Ubuntu 下 Trojan-QT5 设置方法
- [Ubuntu 下 Trojan-QT5 设置方法](#ubuntu-下-trojan-qt5-设置方法)
  - [1. 下载客户端](#1-下载客户端)
  - [2. 查看节点信息](#2-查看节点信息)
  - [3. 添加节点](#3-添加节点)
    - [3.1 单节点添加 - 手动](#31-单节点添加---手动)
    - [3.2 单节点添加 - 扫码](#32-单节点添加---扫码)
    - [3.3 批量添加 - 订阅](#33-批量添加---订阅)
    - [3.4 批量添加 - 导入配置文件](#34-批量添加---导入配置文件)
  - [4. 设置开机启动](#4-设置开机启动)
  - [5. 系统代理的设置](#5-系统代理的设置)
  - [6. 配合浏览器扩展使用](#6-配合浏览器扩展使用)

- 截图对应客户端版本 `Trojan-QT5 v1.1.3`
- 截图对应的系统 `Ubuntu 20.04`

## 1. 下载客户端

- 访问 [https://dl.trojan-cdn.com/trojan/](https://dl.trojan-cdn.com/trojan/) 下载 
- 访问 [Github Releases](https://github.com/Trojan-Qt5/Trojan-Qt5/releases) 下载

根据自己的系统下载对应的版本

- Windows 下载 `Trojan-Qt5-ubuntudows.7z` ，解压后直接运行 `Trojan-qt5.exe` 即可
- macOS 下载 `Trojan-Qt5-macOS.dmg`，安装请查看： [macOS 下 Trojan-QT5 安卓说明](/zh_CN/trojan/mac-trojan-qt5-install-guide.md)
- Linux 下载 `Trojan-Qt5-Linux.7z` ，解压后运行 `Trojan-qt5.AppImage` (需要赋予文件可执行权限)


注：
- **由于部分客户端版本存在配置互不兼容的情况，建议更换版本时直接删除原版本重新配置** 
- Windows 启动时如果提示 VCRUNTIME140.dll 和 MSVCP140.dll 缺失，请访问 [最新支持的 Visual C++ 下载](https://support.microsoft.com/zh-cn/help/2977003/the-latest-supported-visual-c-downloads) 安装 `vc_redist.x86.exe` 与 `vc_redist.x64.exe`
- 如果点击连接时时闪退/报错/没有反应，请确认没有其他程序占用客户端的监听端口

## 2. 查看节点信息

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

## 3. 添加节点

推荐通过 **订阅** 方式批量添加，单节点添加推荐通过扫码的方式进行添加。

### 3.1 单节点添加 - 手动

打开客户端，点击 `连接(C)` > `添加(A)` > `手动(M)` > `手动添加 TROJAN 连接`，在弹出的窗口中填写信息。

![add-manually-01-ubuntu.png](/images/trojan/troajn-qt/add-manually-01-ubuntu.png)  

一般只需填写红框部分：

- `配置名称`：随意填写一个备注名称
- `服务器地址`：填写服务器节点对应的域名
- `服务器端口`：填写对应的服务器端口

勾选底部的 `程序启动时自动连接` 会在打开客户端时自动连接该节点。  

![add-manually-02-ubuntu.png](/images/trojan/troajn-qt/add-manually-02-ubuntu.png)

### 3.2 单节点添加 - 扫码

在产品详情页面，可以点击节点信息中最后一列的二维码图标 ![icon-qrcode.png](/images/icon-qrcode.png) 即可显示对应的二维码。

![add-by-qr.png](/images/trojan/troajn-qt/add-by-qr.png) 

打开客户端，点击 `连接(C)` > `添加(A)` > `手动(M)` > `扫描屏幕上的二维码(C)` 。

### 3.3 批量添加 - 订阅

在产品详情页面获取 Trojan-QT5 的服务器订阅链接。

![add-subscription-00.png](/images/trojan/troajn-qt/add-subscription-00.png)

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

右键点击系统通知区域的客户端图标 ![icon-trojan-indicator.png](/images/icon-trojan-indicator.png) 打开菜单。

依次点击 `服务器订阅` > `服务器订阅设置` ，打开订阅管理窗口。

![add-subscription-01-ubuntu.png](/images/trojan/troajn-qt/add-subscription-01-ubuntu.png)

1. 点击添加
2. 将订阅链接粘贴到网址中，**替换掉默认生成的链接**
3. 点击确定
4. 打开客户端菜单，点击 `服务器订阅` > `更新服务器订阅(不通过代理)`，等待节点列表出现。
5. 选中一个节点，点击顶部的连接按钮 ![icon-trojan-link.png](/images/icon-trojan-link.png) 即可连接
6. 连接后，在窗口底部可以确认客户端当前监听的端口数字

![add-subscription-02-ubuntu.png](/images/trojan/troajn-qt/add-subscription-02-ubuntu.png)

![add-subscription-03-ubuntu.png](/images/trojan/troajn-qt/add-subscription-03-ubuntu.png)


### 3.4 批量添加 - 导入配置文件

在产品详情页面获取 Trojan-QT5 的配置文件 `gui-config.json` 。

![add-by-file.png](/images/trojan/troajn-qt/add-by-file.png)

打开客户端，点击 `文件(F)` > `从 gui-config.json 导入连接(I)` 。

选择刚才下载的 `gui-config.json` 文件即可。 

## 4. 设置开机启动

点击顶部菜单 设置 > 常规设置 。

勾选登陆时启动即可。

![set-startup-ubuntu.png](/images/trojan/troajn-qt/set-startup-ubuntu.png)

## 5. 系统代理的设置

在系统通知区域 Trojan 客户端图标上右键打开菜单可以设置系统代理的模式：

- **直连模式**：不设置系统代理，需要手动在软件内设置代理或是安装扩展进行使用
- **PAC 模式**：设置系统代理，为 PAC 模式，按照 PAC 文件内规则决定访问的网站是否经过代理，推荐日常使用
- **全局模式**：设置系统代理，为全局模式，表示电脑中所有使用系统代理的流量都会经过代理

如果菜单不一致，请更新客户端版本

![system-proxy-mode-ubuntu.png](/images/trojan/troajn-qt/system-proxy-mode-ubuntu.png)

## 6. 配合浏览器扩展使用

如果不使用客户端的系统代理，可以参考下面教程通过安装浏览器扩展使用（支持 Chrome / Firefox / 新版 Edge 浏览器）

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)  

**如果使用的客户端是 1.1.0 以上版本，请继续查看下面内容：**

由于扩展中提供的本地 Socks5 端口为 1080，需要修改为 Trojan-QT5 1.1.0 以上版本中对应的 `51837` ，其他内容不需要修改：

客户端连接时可以在左下角确认所监听的 Socks5 端口。

![socks-port.png](/images/trojan/troajn-qt/socks-port.png)

![switcyomega-port-change.png](/images/trojan/troajn-qt/switcyomega-port-change.png)





