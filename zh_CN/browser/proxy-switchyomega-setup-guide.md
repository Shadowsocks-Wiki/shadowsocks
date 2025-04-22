**安装浏览器扩展首先需要您完成客户端的设置**

[Trojan 服务客户端设置教程索引](../../README.md)

- 本教程提供的配置文件中对应的本地 Socks5 端口监听端口为 **7897**
- 本教程支持 **Chrome** 、 **Firefox** 以及 **Microsoft Edge** 浏览器

### 安装 Proxy SwitchyOmega 3 扩展

Proxy SwitchyOmega 3(Zero Omega) 是 Proxy SwitchyOmega 开源维护版本：[Github 项目主页](https://github.com/zero-peak/ZeroOmega)

可以从各自浏览器商店进行安装，目前只有 Chrome 的商店需要在代理环境下进行访问。

- **Edge** 请访问：[Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/zeroomegaproxy-switchy-/dmaldhchmoafliphkijbfhaomcgglmgd)
- **Firefox** 请访问：[Firefox Addon](https://addons.mozilla.org/en-US/firefox/addon/zeroomega/)  
- **Chrome** 请访问：[Chrome Web Store](https://chromewebstore.google.com/detail/pfnededegaaopdmhkdmcofjmoldfiped)  
    Chrome 需要先开启客户端的 **系统代理(System Proxy)** 功能再进行安装，如果系统代理无法生效请查看：
  - [无扩展、无系统代理情况下以代理模式启动 Chrome](/zh_CN/browser/chrome-start-without-system-proxy.md)

截图以 Edge 浏览器为例，首先点击 `获取`，再点击 `添加扩展`，即可完成添加 :

![browser-edge-install.png](https://dl.trojan-cdn.com/images/browser/zero/zero-add.jpg)

### 设置扩展图标常驻地址栏右侧

![](https://dl.trojan-cdn.com/images/browser/zero/zero-show.jpg)

### 导入配置文件

安装完成后会打开扩展的选项页面，可以选择 **跳过教程** 然后选择左侧的 `导入/导出`。

**右键点击下面 OmegaOptions-xxx.bak ，选择复制链接地址**

- [OmegaOptions-7897.bak](https://dl.trojan-cdn.com/browser/OmegaOptions-7897.bak) (本地 HTTP 端口为 **7897** 的客户端: **Clash Verge Rev**)
- 其他浏览器可以在图片底部获取

**通过恢复链接导入**

1. 选择左侧的 **导入导出**
2. 在 **在线恢复** 右侧输入框中粘贴恢复链接
3. 点击 **恢复** 按钮
4. 在地址栏右侧，点击扩展的图标，选择 **自动切换** 使用
5. 导入成功后左侧情景模式会变为 `代理模式` 与 `自动切换` 两个模式，使用方法请看后面的使用介绍。

![browser-edge-restore-link.png](https://dl.trojan-cdn.com/images/browser/zero/zero-import.jpg)

其他客户端请使用下面的链接

- [OmegaOptions-1080.bak](https://repo.trojan-cdn.com/browser/OmegaOptions-1080.bak) (本地 Socks5 端口为 **1080** 的客户端：TrojanX / Tanpopo)
- [OmegaOptions-51837.bak](https://repo.trojan-cdn.com/browser/OmegaOptions-51837.bak) (本地 Socks5 端口为 **51837** 的客户端：Trojan-QT5 v1.1.6)
- [OmegaOptions-7890.bak](https://repo.trojan-cdn.com/browser/OmegaOptions-7890.bak) (本地 HTTP 端口为 **7890** 的客户端：ClashX、Clash for Windows、Clash Verge、**FlClash**)

### 使用介绍

扩展安装后可以在地址栏右侧切换代理的情景模式，**推荐选择 `自动切换`，而不是系统代理** ：

|模式名称|功能|
|---|---|
|直接连接|所有访问都不使用代理|
|系统代理|访问网站是否使用代理取决于操作系统的默认代理|
|代理模式|所有访问都使用代理|
|**自动切换**|根据规则决定访问的网站是否经过代理|

![browser-edge-mode-intro.png](https://repo.trojan-cdn.com/images/browser/swo-mode-intro-winedge.png)

## 补充自定义规则

选择自动切换模式时，会根据情景模式中的所包含的规则决定所访问的网站是否会经过代理。 

扩展提供的默认规则基于 GFWList 包含了大部分被屏蔽的网站，部分网站没有被 GFWList 包含或刚被屏蔽的网站没有及时的加入规则导致无法访问，可以自己手动添加。

- 首先打开扩展的选项页面，选择自动切换
- 点击右侧的添加条件
- 简单的添加方法如下：
    1. 条件类型选择 `域名通配符`
    2. 条件设置：`*.网站主域名`，例如 `*.baidu.com` / `*.google.com`
    3. 情景模式：选择`直接连接`表示访问该网站将不会使用代理，选择`代理模式`表示访问该网站会使用代理
    4. 最后点击应用选项保存
- 点击底部的 `立即更新情景模式` 会更新 GFWList 所包含的规则

![browser-edge-add-rule.png](https://repo.trojan-cdn.com/images/browser/swo-add-rule-winedge.png)

### 我是否需要安装扩展

##### 是否一定要安装扩展？  

**推荐安装，但不是必须安装**，不安装扩展时，浏览器会使用系统代理，因此开启客户端的系统代理即可。

##### 扩展安装与否的区别  

**安装扩展后 Chrome 代理将不受系统设置的影响，而且可以更加方便地添加自定义访问规则，因此推荐安装扩展进行使用。**

- 安装时： 访问请求 > 浏览器 > **浏览器扩展** > 代理客户端 > 代理服务器 > 目标网站
- 不安装时： 访问请求 > 浏览器 > **系统代理** > 代理客户端 > 代理服务器 > 目标网站

若不安装扩展，浏览器的代理将取决于系统的默认代理，如果系统代理无法修改或是生效则无法使用。
