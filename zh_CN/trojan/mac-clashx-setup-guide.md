# macOS 下 ClashX 设置方法
- [macOS 下 ClashX 设置方法](#macos-下-clashx-设置方法)
  - [1. 下载与安装](#1-下载与安装)
  - [2. 获取订阅链接](#2-获取订阅链接)
  - [3. 添加配置](#3-添加配置)
  - [4. 使用介绍](#4-使用介绍)
  - [5. Chrome / Edge / Firefox 配合 SwitchyOmega 扩展](#5-chrome--edge--firefox-配合-switchyomega-扩展)

---

- 截图对应客户端版本为 `ClashX 1.20.1`
- 截图对应的系统版本为 `macOS 10.15.1`

## 1. 下载与安装 

- 访问 [https://dl.trojan-cdn.com/trojan/macos/](https://dl.trojan-cdn.com/trojan/macos/) 下载
- 访问 [Github](https://github.com/yichengchen/clashX/releases) 下载

下载 `ClashX.dmg` 后双击打开，将 ClashX 图标拖动至右侧 `Applications` 文件夹内。

然后在启动台中即可找到 ClashX ，点击打开即可。

![clashx-install.png](/images/trojan/clashx/clashx-install.png)

## 2. 获取订阅链接

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.au/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

在产品详情页面获取 Clash 的服务器订阅链接。

![portal-clash-get-link.png](/images/portal-clash-get-link.png)

点击 ClashX 配置对应的 `获得地址`，在弹出的窗口中，复制订阅 URL。

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

## 3. 添加配置

点击右上角的 Clash 图标打开菜单。

按 `⌘+M` 或是依次点击 `配置` > `托管配置` > `管理` 打开订阅管理窗口。

![clashx-add-01.png](/images/trojan/clashx/clashx-add-01.png)

点击添加，然后填写内容后点击确定完成添加。

- `Url`: 填入订阅链接
- `Config Name`：填写一个备注名称

![clashx-add-02.png](/images/trojan/clashx/clashx-add-02.png)

## 4. 使用介绍

点击右上角的 Clash 图标打开菜单。

![clashx-menu.png](/images/trojan/clashx/clashx-menu.png)

点击 `设置为系统代理` 即可开启系统代理，此时即可正常使用。

点击第一项 `出站模式` 可以选择客户端的代理模式：

![clashx-mode.png](/images/trojan/clashx/clashx-mode.png)

`全局模式`： 所有访问请求都使用代理。  
`规则链接`： 根据配置文件内规则处理访问请求是否使用代理。  
`直接连接`： 所有访问请求都**不使用代理**。  

点击 `Proxy` 可以切换需要使用的节点。

## 5. Chrome / Edge / Firefox 配合 SwitchyOmega 扩展

如果不使用客户端的系统代理，可以参考下面教程通过安装浏览器扩展使用（支持 Chrome / Firefox / 新版 Edge 浏览器）

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)

**由于扩展中代理模式对应客户端的端口为 1080，需要修改为 Clash 对应的 7890**，请按照下图进行修改：

![cfw-swo-port.png](/images/trojan/clash-win/cfw-swo-port.png)