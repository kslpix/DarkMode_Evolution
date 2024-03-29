# DarkMode Evolution 23.6.23

## 重要：全新~~次世代版本~~兼容 MIUI14/13，可能出现 自动重启到recovery和卡第一屏 问题
## 支持应用

- 😋兼容良好 😔不尽人意 ？无法确定
- 😋淘宝（com.taobao.taobao）
- 😋学习通（com.chaoxing.mobile）
- 😔闲鱼（com.taobao.idlefish）
- 😋阿里巴巴（com.alibaba.wireless）
- 😔铁路12306（com.MobileTicket）
- 😔支付宝（com.eg.android.AlipayGphone）
- 😋什么值得买（com.smzdm.client.android）
- 😔抖音（com.ss.android.ugc.aweme）
- 😋拼多多（com.xunmeng.pinduoduo）
- ？高德地图（com.autonavi.minimap）
- 更多应用请参见模块目录内置配置文件

## 其他事项

- 全新版本，~~超稳定的~~兼容性

- 详细更新请参见changelog.md

## 已知问题

- 部分应用自MIUI14以来已失效，努力解决中

- 抖音（com.ss.android.ugc.aweme）内测版提供深色模式。

## 如何使用

1.在右侧Releases下载最新zip包

2.进入Magisk软件内安装

3.重启手机

4.进入 设置-显示-更多深色模式设置 打开对应软件开关

## 简明教程

Q : 如何添加自己想深色的应用？

A : MIUI使用两个配置文件来控制应用是否使用深色，其中(ForceDarkAppSettings.json)是必须更改的，当效果不佳或者无法生效才会使用一个增强配置来控制具体效果，其位置在(forcedarkconfig)文件夹内。

假设您需要添加一个应用深色，您首先查询应用包名(如com.dark.demo)，接着在(ForceDarkAppSettings.json)中的[]内添加一行

`{"defaultEnable":false,"overrideEnableValue":0,"packageName":"com.dark.demo","showInSettings":true}`

其中参数defaultEnable意味着默认是否开启，可选(true/false)。参数showInSettings意味着是否在设置中显示开关。

添加之后请验证json合法性 [JSON格式校验器](https://json-online.com/check/ "点我进行验证json")。一般验证之后刷入模块就有效果了，如果没有效果，请尝试进阶教程。

## 进阶教程

Q : 如何编写一个增强应用配置文件？

A : 假设您需要添加一个增强应用深色配置文件，您首先查询应用包名(如com.dark.demo)，首先在(forcedarkconfig)文件夹内，新建一个名为(com.dark.demo.json)的文件，放入如下模板。

`{
  "packageName": "com.dark.demo",
  "forceDark": true,
  "mainRule": 0,
  "forceDarkActivityConfigList": [],
  "forceDarkViewGlobalConfigList": []
}`

其中各个参数可参考 小米深色配置.xlsx 文件自行编辑多次测试。

## 捐赠

致谢：
- 酷安@夜夜夜猫 
- GITHUB@MidNightBlackCat 
- GITHUB@dreamflandre
> https://github.com/dreamflandre/DarkP/releases
- 酷安支持我的小伙伴们

如果你喜欢我这个项目，请多多提交Pr吧，谢谢！

Made with ♥.
