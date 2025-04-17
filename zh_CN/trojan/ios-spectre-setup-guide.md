# iOS 下 Spectre 设置方法

## 1. 安装客户端

客户端当前正在测试，请等待正式发布。

有需要可以提交工单申请参加测试。

注：
- 当前客户端仍在继续开发，因此目前仅支持全局模式。

## 2. 查看节点信息

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://secure.shadowsocks.au/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

在节点信息最后一列：

- 点击二维码图标 ![icon-qrcode.png](/images/icon-qrcode.png) 即可显示对应的二维码
- 点击齿轮图标 ![icon-config.png](/images/icon-config.png) 即可获得对应的 Trojan URL

![portal-get-qr-or-url.png](/images/portal-get-qr-or-url.png)

## 3. 添加节点

打开客户端首页，可以选择扫码或是复制 Trojan URL 添加单个节点。

![home.png](/images/trojan/spectre/home.png)

### 3.1 单节点添加 - 扫码

使用其他设备打开节点二维码后，点击客户端界面的扫码图标 ![icon-spectre-scanqr.png](/images/icon-spectre-scanqr.png) 进行扫码即可完成添加。

如果不方便使用其它设备，可以截图或是保存二维码图片到设备中，然后在相机扫码界面点击右上角 ![icon-spectre-openqr.png](/images/icon-spectre-openqr.png) 打开刚才的二维码图片。

![add-by-qrpic.png](/images/trojan/spectre/add-by-qrpic.png)

### 3.2 单节点添加 - Trojan URL

首先复制节点的 Trojan URL， 点击客户端界面的 `+` 图标，复制的 Trojan URL 会自动填充，然后点击右上角的完成即可。

![add-by-url.png](/images/trojan/spectre/add-by-url.png)

### 3.3 添加订阅

在产品详情页面获取 Spectre / Trojan-QT5 / Shadowrocket 兼容的的服务器订阅链接。

![add-subscription-00.png](/images/portal-get-link-qt5.png)

注：**订阅链接与您的密码一样重要，请勿分享给他人，如不慎泄露，请在产品详情页面重置链接。**

点击 `订阅按钮` 可以选择 `复制订阅链接` 或是 `显示订阅二维码` 。

然后点击客户端主界面的 `添加服务器`。

![add-sub-01.png](/images/trojan/spectre/add-sub-01.png)

- 点击 `订阅` 右侧的 `+` ，在新弹出的窗口中，粘贴订阅链接，点击完成即可完成添加。

- 点击 扫码 ![icon-spectre-scanqr-sub.png](/images/icon-spectre-scanqr-sub.png) 按钮可以通过扫码的方式添加。  
 
![add-sub-02.png](/images/trojan/spectre/add-sub-02.png)  

![add-sub-03.png](/images/trojan/spectre/add-sub-03.png)

添加完成后，即可选择一个节点，点击连接开始使用。

![add-sub-04.png](/images/trojan/spectre/add-sub-04.png)

## 4. 启动连接

添加完成后，主界面会显示节点信息，点击顶部 `未连接` 右侧的按钮即可开始使用代理。

![add-done.png](/images/trojan/spectre/add-done.png)

第一次连接时，客户端会请求 VPN 设置权限，请选择允许。

![ask-vpn-p.png](/images/trojan/spectre/ask-vpn-p.png)

如果需要添加更多或是切换节点，请点击 `切换服务器` 进行添加或是更换节点。
