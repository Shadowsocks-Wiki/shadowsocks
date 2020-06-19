# iOS 下 QuantumultX 设置方法

- QuantumultX 推荐使用我们提供的订阅进行节点的添加

## 1. 查看节点信息

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。


### 1.1 获取订阅链接
点击 `获得地址`，在弹出的窗口中点击 `复制地址` 复制 QuantumultX 对应的订阅链接。

![portal-qx-get-link.png](/images/trojan/quantumultx/portal-qx-get-link.png)

## 2. 添加订阅

在客户端首页点击右下角的功能图标打开设置页面。

![qx-home.png](/images/trojan/quantumultx/qx-home.png)

然后点击右上角的 ![icon-qx-link.png](/images/trojan/quantumultx/icon-qx-link.png) 图标，进行订阅链接的添加。

![qx-settings.png](/images/trojan/quantumultx/qx-settings.png)

在弹出的窗口中，粘贴 `1.1 获取订阅链接` 复制的链接，然后点击 `好` 完成添加。

![qx-add-by-link.png](/images/trojan/quantumultx/qx-add-by-link.png)

添加成功后会如下图进行提示，点击确定再点击左上角的 ![icon-down-arrow.png](/images/trojan/quantumultx/icon-down-arrow.png) 按钮返回首页。

![qx-add-done.png](/images/trojan/quantumultx/qx-add-done.png)

在首页界面，顶部的按钮用于切换节点、查看配置文件的规则。点击顶部 `已停止` 右侧的开关按钮即可开始连接。初次连接会请求 VPN 权限，请选择允许。

![qx-ask-p.png](/images/trojan/quantumultx/qx-ask-p.png)

**第一次连接时可能无法使用，推荐断开后再重新连接一次试一下。**

长按右下角的功能图标可以切换客户端的运行模式。

- 蓝底白图标： **全局模式**，所有流量都会经过代理。
- 白底彩图标： **规则切换**，会按照配置文件中的规则决定流量是否经过代理，**推荐日常使用**。
- 黄底白图标： **直接连接**，不使用代理。

![qx-mode.png](/images/trojan/quantumultx/qx-mode.png)