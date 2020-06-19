# Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用

- [Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](#chrome--edge--firefox-安装-proxy-switchyomega-扩展使用)
  - [1. 首先要安装 Proxy SwitchyOmega 扩展](#1-首先要安装-proxy-switchyomega-扩展)
  - [2. 导入配置文件](#2-导入配置文件)
    - [2.1 通过恢复链接导入](#21-通过恢复链接导入)
    - [2.2 通过备份文件导入(与上面的方法二选一即可)](#22-通过备份文件导入与上面的方法二选一即可)
  - [3. 使用介绍](#3-使用介绍)
  - [4. 补充自定义规则](#4-补充自定义规则)
  - [5. 我是否需要安装扩展 Proxy SwitchyOmega](#5-我是否需要安装扩展-proxy-switchyomega)
      - [是否一定要安装扩展](#是否一定要安装扩展)
      - [扩展安装与否的区别](#扩展安装与否的区别)

**浏览器安装扩展需要您已完成客户端的设置** 

[Trojan 服务客户端设置教程索引](/README.md)

- 本教程提供的配置文件对应客户端的本地 `Socks5` 监听端口为 `1080`
- 本教程支持 **Chrome** 、 **Firefox** 以及 **新版 Microsoft Edge** 浏览器
- 新版 Microsoft Edge 浏览器下载地址：[https://www.microsoft.com/zh-cn/edge](https://www.microsoft.com/zh-cn/edge)

## 1. 首先要安装 Proxy SwitchyOmega 扩展
- Edge 请访问: [Edge 应用商店](https://microsoftedge.microsoft.com/addons/detail/dijmmgblneagkcdganednabkbgjmceoe)
- Firefox 请访问: [Firefox 应用商店](https://addons.mozilla.org/en-US/firefox/addon/switchyomega/)
- Chrome 请访问： [Chrome 应用商店](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif?hl=zh-CN)

**注**：Chrome 需要先开启代理客户端系统代理再进行安装，如果系统代理无法生效请查看： [无扩展、无系统代理情况下以代理模式启动 Chrome](/zh_CN/browser/chrome-start-without-system-proxy.md)

截图以 Edge 浏览器为例，首先点击 `获取`，再点击 `添加扩展`，即可完成添加:

![swo-install-winedge.png](/images/browser/swo-install-winedge.png)

## 2. 导入配置文件

在地址栏右侧的扩展图标上点击右键 > 点击选项，打开扩展的选项页面，选择 `导入/导出`。

### 2.1 通过恢复链接导入

根据所使用的客户端选择恢复链接，复制粘贴到在线恢复的输入框内(右键，选择复制链接地址)，点击恢复。

[OmegaOptions-1080.bak](https://dl.trojan-cdn.com/browser/OmegaOptions-1080.bak) (本地 Socks5 端口为 1080 的客户端：TrojanX)
[OmegaOptions-51837.bak](https://dl.trojan-cdn.com/browser/OmegaOptions-51837.bak) (本地 Socks5 端口为 51837 的客户端：Trojan-QT5 1.1.0 及以上版本)
[OmegaOptions-7890.bak](https://dl.trojan-cdn.com/browser/OmegaOptions-7890.bak) (本地 HTTP 端口为 7890 的客户端：ClashX、Clash for Windows v0.10.3 及以上版本)

导入成功后左侧情景模式会显示为 `代理模式` 与 `自动切换` 两个模式，使用方法请看后面的使用介绍。

![swo-import-by-link-winedge.png](/images/browser/swo-import-by-link-winedge.png)

![swo-import-succeeded-winedge.png](/images/browser/swo-import-succeeded-winedge.png)

### 2.2 通过备份文件导入(与上面的方法二选一即可)

![swo-import-by-file-winedge.png](/images/browser/swo-import-by-file-winedge.png)

## 3. 使用介绍

在地址栏右侧的扩展图标上点击可以选择需要使用的情景模式。

|模式名称|功能|
|:--:|--|
|直接连接|所有访问都不使用代理|
|系统代理|访问网站是否使用代理取决于操作系统的默认代理|
|代理模式|所有访问都使用代理|
|自动切换|根据规则决定访问的网站是否经过代理|

![swo-mode-intro-winedge.png](/images/browser/swo-mode-intro-winedge.png)

## 4. 补充自定义规则

选择自动切换模式时，会根据情景模式中的所包含的规则决定所访问的网站是否会经过代理。 

扩展提供的默认规则基于 GFWList 包含了大部分被屏蔽的网站，部分网站没有被 GFWList 包含或刚被屏蔽的网站没有及时的加入规则导致无法访问，可以自己手动添加。

- 首先打开扩展的选项页面，选择 `自动切换` 
- 点击右侧的 `添加条件`
- 简单的添加方法如下：
  1. 条件类型选择 `域名通配符`
  2. 条件设置：`*.网站主域名`，例如 `*.baidu.com` / `*.google.com`
  3. 情景模式：选择`直接连接`表示访问该网站将不会使用代理，选择`代理模式`表示访问该网站会使用代理
  4. 最后点击 `应用选项` 保存
- 点击底部的 `立即更新情景模式` 会更新 GFWList 所包含的规则

![swo-add-rule-winedge.png](/images/browser/swo-add-rule-winedge.png)

## 5. 我是否需要安装扩展 Proxy SwitchyOmega

#### 是否一定要安装扩展  
`否`，不安装扩展时，**浏览器会使用系统代理**，因此开启客户端的系统代理即可。

如果系统代理无法生效或是客户端无法修改系统代理，则需要安装扩展使用。

#### 扩展安装与否的区别  
- 安装时： 访问请求 > 浏览器 > `浏览器扩展` > 代理客户端 > 代理服务器 > 目标网站
- 不安装时： 访问请求 > 浏览器 > `系统代理` > 代理客户端 > 代理服务器 > 目标网站

若不安装扩展，浏览器的代理将取决于系统的默认代理，如果系统代理无法修改或是生效则无法使用。  

而且安装扩展可以更加方便地添加自定义访问规则，因此推荐安装扩展进行使用。