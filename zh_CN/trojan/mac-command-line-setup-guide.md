# macOS 下命令行版本设置方法

- 命令行客户端仅提供最基础的功能，如果没有必要，推荐使用其他图形客户端。

## 1. 下载客户端

- 访问 [我们提供的镜像仓库](https://repo.trojan-cdn.com/trojan-gfw/trojan/LatestRelease/) 下载
- 访问 [Github](https://github.com/trojan-gfw/trojan/releases) 下载

下载 `trojan-[版本号]-macos.zip` 文件

## 2. 获取配置

命令行客户端只能设置单节点。

登入到客户中心，依次访问 `产品服务` > [`我的产品与服务(点击前往)`](https://portal.shadowsocks.nz/clientarea.php?action=products) ，查看 Trojan 服务对应的 `云加速服务 - Lite` / `Pro` 服务器信息。

在节点信息最后一列：
- 点击齿轮图标 ![icon-config.png](/images/icon-config.png) 打开单节点的配置窗口，点击 `复制配置` 即可复制节点配置。

![portal-get-qr-or-url.png](/images/portal-get-qr-or-url.png)
![portal-copy-config.png](/images/portal-copy-config.png) 


## 3. 配置客户端

将下载 `trojan-[版本号]-macos.zip` 解压，之后打开 trojan 文件夹，选择使用 文本编辑器 打开 `config.json` 文件，使用 `2. 获取配置` 中复制的配置替换全部的内容后保存。

![edit-config-mac.png](/images/trojan/terminal/edit-config-mac.png) 

## 4. 运行、退出客户端

在 macOS 10.15 以上版本中会有各种权限请求，请点击允许。

右键点击 `start.command` 选择打开，如果有权限询问窗口，请选择 `打开`、`允许`。  

![start-command-mac.png](/images/trojan/terminal/start-command-mac.png)

![permission-requests-01.png](/images/trojan/terminal/permission-requests-01.png)   

![permission-requests-02.png](/images/trojan/terminal/permission-requests-02.png) 

运行成功会显示下面的窗口。

![run-successed-mac.png](/images/trojan/terminal/run-successed-mac.png)

如果需要退出，关闭该窗口即可。

## 5. 设置系统代理

不同于图形客户端，命令行客户端运行后不会对系统或其他软件有任何影响，需要手动进行 `系统代理` 或是浏览器扩展的设置。

请依次打开 `系统偏好设置` > `网络` > `高级` (窗口右下角) ，切换到 `代理` 标签页，勾选 `SOCKS` 代理后，按照如图进行设置。

![set-system-proxy-mac.png](/images/trojan/terminal/set-system-proxy-mac.png)

点击 `好` 保存。

注：退出客户端后，系统设置需要手动恢复，否则无法上网，因此推荐安装浏览器设置扩展使用。

## 6. 设置浏览器扩展

参考下面教程通过安装浏览器扩展使用（支持 Chrome / Firefox / 新版 Edge 浏览器）

设置方法请参考：[Chrome / Edge / Firefox 安装 Proxy SwitchyOmega 扩展使用](/zh_CN/browser/proxy-switchyomega-setup-guide.md)  
