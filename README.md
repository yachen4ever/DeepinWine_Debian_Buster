# DeepinWine_Debian_Buster

这是一个为Debian Buster x64重新打包的Deepin Wine，打包时间为2019-5-3，Deepin Wine相关版本为2.18-18~rc2

安装方法：

0. KDE额外步骤
```
$ apt install gnome-settings-daemon
```
并建立$HOME/.config/autostart-scripts/gsd-xsettings.sh文件，内容
```
#!/bin/bash
/usr/lib/gnome-settings-daemon/gsd-xsettings
```

1. 增加32位运行环境
```
$ dpkg --add-architecture i386 && apt update
```

2. 安装deepinwine2.18-18~rc2_debian_buster目录下所有deb包
```
$ dpkg -i deepinwine2.18-18~rc2_debian_buster/*.deb
```

3. 补全32位运行库依赖
```
$ apt install -f
```
4. 自行安装Deepin Wine移植应用（下载deb包dpkg -i安装）

[QQ轻聊版](https://mirrors.aliyun.com/deepin/pool/non-free/d/deepin.com.qq.im.light/)

[微信](https://mirrors.aliyun.com/deepin/pool/non-free/d/deepin.com.wechat/)

感谢[wszqkzqk移植的适用于ubuntu 18.04的deepinwine](https://github.com/wszqkzqk/deepin-wine-ubuntu)，本repo移植过程中参考了很多，另外一些问题也可看该repo的FAQ。

---------------
2019.5.7 Update：
Deepin打包的应用中没有启用Cleartype，看着很难受，我给我自己常用的微信和QQ解包后，按照[arch wiki wine页面](https://wiki.archlinux.org/index.php/Wine#Enable_font_smoothing)修改了下user.reg，开启了Cleartype后重新打包，为避免冲突在包名后加了.yac上传。
