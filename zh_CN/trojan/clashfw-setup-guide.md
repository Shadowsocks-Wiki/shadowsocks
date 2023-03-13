# Clash for Windows 设置方法
- [Clash for Windows 设置方法](#clash-for-windows-设置方法)
  - [1. 下载与安装](#1-下载与安装)
  - [2. 获取配置](#2-获取配置)
  - [3. 添加配置](#3-添加配置)
    - [3.1 Clash 主界面介绍](#31-clash-主界面介绍)
    - [3.2 通过订阅链接添加节点](#32-通过订阅链接添加节点)
  - [4. Clash 代理使用介绍](#4-clash-代理使用介绍)
      - [4.1 开启系统代理与开机启动](#41-开启系统代理与开机启动)
      - [4.2 Global 全局规则选项](#42-global-全局规则选项)
  - [5. Chrome / Edge / Firefox 配合 SwitchyOmega 扩展](#5-chrome--edge--firefox-配合-switchyomega-扩展)

## 1. 下载与安装

- 访问 Clash for Windows 官方  [Github Releases ](https://github.com/Fndroid/clash_for_windows_pkg/releases) 下载
- 访问我们提供的 [镜像仓库](https://repo.trojan-cdn.com/clash_for_windows_pkg/LatestRelease/) 下载 

  - Windows系统 下载 Clash.for.Windows.Setup.[版本号].exe 文件
  - macOS 系统下载 Clash.for.Windows-版本号.dmg 文件

在 Windows 上，双击打开 exe 文件进行安装，如果系统提示 `阻止了无法识别的应用启动`，请点击更多信息，然后再点击 `仍要运行` 进行安装。  

## 2. 获取配置

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

在产品详情页面获取 Clash 的服务器订阅链接。

![portal-clash-get-link.png](/images/portal-clash-get-link.png)

点击 ClashX 配置对应的 `获得地址`，在弹出的窗口中，复制订阅 URL。

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

## 3. 添加配置

### 3.1 Clash 主界面介绍

安装后 Windows 可以通过双击通知区域的 Clash for Windows 图标打开主界面 

![cfw-home.png](/images/trojan/clash-win/cfw-home.png)

### 3.2 通过订阅链接添加节点

首先打开 `Profiles` 配置选择页面，然后进行配置文件的添加

复制 `获取配置` 步骤中得到的订阅 URL，粘贴到 `Download from a URL` 输入框内，点击右侧的 `Download` 按钮。

显示 `Success!` 表示成功添加了配置文件，并且下面会多了一个配置，点击可以切换到对应的配置。  
具体使用方法请参考后面教程。

![cfw-add-config-link.png](/images/trojan/clash-win/cfw-add-config-link.png)
 
![cfw-add-config-link-done.png](/images/trojan/clash-win/cfw-add-config-link-done.png)

## 4. Clash 代理使用介绍

#### 4.1 开启系统代理与开机启动

首先打开 `General` 首页页面, 开启系统代理与开机启动，然后打开 `Proxies` 代理服务器选择页面。

![cfw-set-system-proxy.png](/images/trojan/clash-win/cfw-set-system-proxy.png)

点击 `Global` 标签，确认全局规则选择不是 `DIRECT` (选择 `DIRECT` 表示不使用代理) ，可以选择 `AUTO`（自动选择节点）或是直接选择自己想要使用的节点。

![cfw-select-node.png](/images/trojan/clash-win/cfw-select-node.png)

选择节点后可能没有立即生效，建议返回 `General` 首页页面 点击 `Clash for Windows` 字样通过快速重启客户端重新载入配置。

这时 Clash 已通过设置系统代理的方式进行工作，使用系统代理的软件已可以正常使用。

可以使用 IE / Edge / Safari 访问 https://www.google.com 测试

#### 4.2 Global 全局规则选项

`Global` 页面中的选项卡是设置 Clash 的代理规则，即设置 Clash 如何处理访问请求。

- Direct 表示直接连接，不使用代理  
![cfw-rule-direct.png](/images/trojan/clash-win/cfw-rule-direct.png)
- Reject 表示全部拒绝访问  
![cfw-rule-reject.png](/images/trojan/clash-win/cfw-rule-reject.png)
- 其他直接选中节点表示全部请求均通过代理，类似于 Shadowsocks 的全局模式

## 5. Chrome / Edge / Firefox 配合 SwitchyOmega 扩展

如果不使用客户端的系统代理，可以参考下面教程通过安装浏览器扩展使用（支持 Chrome / Firefox / 新版 Edge 浏览器）

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)

**由于扩展中代理模式对应客户端的端口为 1080，需要修改为 Clash 对应的 7890**，请按照下图进行修改：

![cfw-swo-port.png](/images/trojan/clash-win/cfw-swo-port.png)
