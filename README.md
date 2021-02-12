## Action OpenWrt IPKs

------

利用GitHub Actions实现全自动的 **OpenWrt** ipk软件包在x86-64平台上进行自动编译

### 特性

> * 自动触发，每天检查源码是否存在更新，若更新就自动编译和打包ipk包并发布到Release；
> * 包含Luci绝大多数常用插件；
> * 所有软件包均包含依赖ipk，不用再去为了一个依赖ipk东奔西找。

### 食用方法

 1. 去Release下载zip文件；
 2. 下载后打开压缩包，进入目录 `\packages\x86_64\base` ，将里面所有ipk文件解压到桌面；
 3. 寻找需要的软件包并复制软件包全名；
 4. 使用WinScp登录OpenWrt，切换到tmp目录下，将需要的软件包拖入此目录；
 5. 登录OpenWrt SSH，输入 `cd /tmp` 切换到tmp目录；
 6. 输入`opkg install 刚刚你复制的软件包名.ipk` ，回车；
 7. 若提示缺少依赖，复制软件包名去解压的那个文件夹查找，把依赖软件包装上，具体过程同上，然后再装你需要的软件包；
 8. 安装完成登入后台进行使用。

### 提醒

* 不建议安装后台主题软件包，可能会导致后台Web页面瘫痪，若非要使用请做好备份。
* **非X86-64架构请勿使用本软件包！**
* 折腾必有风险，所以建议在安装任何一个软件包折腾前务必做好备份工作，以免出现不必要的麻烦。出现任何后果概不负责。
 

##致谢
本项目是站在巨人的肩膀上完成的，没有他们不可能有这个项目，他们是：

- [P3TERX](https://p3terx.com/archives/build-openwrt-with-github-actions.html)
- [Microsoft](https://www.microsoft.com)
- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub](https://github.com)
- [GitHub Actions](https://github.com/features/actions)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cisco](https://www.cisco.com/)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [Cowtransfer](https://cowtransfer.com)
- [WeTransfer](https://wetransfer.com/)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)