## 1. 下载与安装

- [购买服务](https://secure.shadowsocks.au/store/cloud)

从 1.x 更新至 2.x 版本时建议选择 **安装前卸载** 的选项（在下一步骤中不要勾选删除数据，不会丢失配置）

Clash Verge Rev 是跨平台客户端， Windows 、 macOS 、 Linux 都可以使用，请访问 [Clash Verge Rev - GitHub Releases](https://github.com/clash-verge-rev/clash-verge-rev/releases) 下载对应的安装文件，常用下载文件参考
 - Windows 64 bit：Clash.Verge_[版本号]_x64-setup.exe  
 - macOS M 芯片： Clash.Verge_[版本号]_aarch64.dmg
 - macOS Intel 芯片： Clash.Verge_[版本号]_x64.dmg

下载后运行安装包进行安装。

## 2. 安装时可能遇到的问题
**Windows** 安装时提示 **WebView2** 错误或是无法启动，请访问下面链接安装 WebView2 组件   
https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/#download 
      
**Windows** 安装时提示 **VCRUNTIME140.dll** 缺失  
请访问 最新支持的 Visual C++ 下载，下载并安装 **vc_redist.x86.exe** 与 **vc_redist.x64.exe**   
https://support.microsoft.com/zh-cn/help/2977003/the-latest-supported-visual-c-downloads

## 3. 获取配置
登入后前往 [我的产品与服务](https://secure.shadowsocks.au/clientarea.php?action=services) ，点击有效的服务，打开产品详情页面，向下滑动。

点击 Clash 配置右侧的获得地址，在弹出的窗口中，选择 **复制地址** 或是 **下载配置**。

![portal-clash-get-link.png](https://repo.trojan-cdn.com/images/portal-clash-get-link.png)

如果点击获得地址没有反应，请更换使用 **Chrome** 、Firefox 或是 EDGE 浏览器访问客户中心。

注1. **订阅链接与您的密码一样重要，请不要分享给他人，如不慎泄露，请在产品详情页面重置链接并提交工单申请重置服务密码。**

注2. 如果使用链接添加时报错，可以点击 **下载配置** ，手动添加 

## 4. 添加配置
打开客户端后，使用第三步的订阅链接添加配置

- 首先点击左侧 **订阅(Profiles)** ，粘贴订阅链接后点击 导入
- 添加成功后点击左侧 **代理(Proxies)** 选择节点使用
- 如果添加失败，请在 **第3步** 中手动下载配置文件，将下载的配置文件拖放到 **订阅** 界面即可
- 下面是使用链接添加演示动图

![](https://dl.trojan-cdn.com/images/trojan/clashvr/ss-cvr-add.gif)

## 5. 客户端使用介绍
正常在添加配置后，前往 **设置**，开启 **系统代理** 后即可正常使用

![](https://dl.trojan-cdn.com/images/trojan/clashvr/cvr-settings.png)

客户端模式（在 **代理 (Proxies)** 界面右上角切换）介绍：

- **规则模式**：自动区分是否代理大陆网站的流量，日常情况推荐使用这个模式
- **全局模式**：所有转发给客户端的流量都会经过代理，切换到全局模式后请选择节点，不需要选择 **DIRECT** 
- **直连模式**：不使用代理

关于 **AUTO 分组** 介绍，Auto 是客户端随机选择节点使用的意思，如需使用 Auto 在 Proxy 分组下选择 Auto 即可。

**在 Proxy 分组下选择其他节点就表示不会使用 Auto 分组所显示节点**。

## 6. 浏览器扩展
如果在第五步中开启了客户端的 系统代理 后仍然无法使用，或是不希望使用系统代理功能，请参考

[Chrome / Edge / Firefox 安装扩展使用](../browser/proxy-switchyomega-setup-guide.md) 

请注意 Clash Verge Rev 的默认端口是 **7897**

