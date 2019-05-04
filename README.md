# DeepinWine_Debian_Buster

这是一个为Debian Buster x64重新打包的Deepin Wine，打包时间为2019-5-3，Deepin Wine相关版本为2.18-18~rc2

安装方法：
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

[迅雷极速版](https://mirrors.aliyun.com/deepin/pool/non-free/d/deepin.com.thunderspeed/)

[百度网盘](https://mirrors.aliyun.com/deepin/pool/non-free/d/deepin.com.baidu.pan/)
