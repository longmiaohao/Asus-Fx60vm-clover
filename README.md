# 核心配置信息
---

|品牌|型号|cpu|显卡|有线网卡|无线网卡|触摸板接口|
|--|--|--|--|--|--|
|AUSU|飞行堡垒FX60vm|i7 6700hq|gtx1060 3g|Realtek|dw1820a|i2c|



## High Sierra 10.13.6 2020年最新web驱动文件

| 系统版本号         | web驱动版本         |
| ------------------ | ------------------- |
| 10.13.6 (17G11023) | 387.10.10.10.40.134 |
| 10.13.6(17G12034)  | 387.10.10.10.40.135 |
| 10.13.6(17G13033)  | 387.10.10.10.40.136 |
| 10.13.6(17G13035)  | 387.10.10.10.40.137 |
| 10.13.6(17G14019)  | 387.10.10.10.40.138 |

# 能做什么

---
- 声音

    > 进入win10后再切如mac会出现没有声音的情况，一般情况只需要手动睡眠一下再打开就好，如果睡眠还不行，那就关机重新进macos，肯定是可以成功的，具体原因不明, 用万能声卡时, 可能会出现声音小或者抱音的情况，这里我提供了一个大佬编译的主要修复这两个问题的万能声卡驱动，里面有三个，自己试合适自己的那个，亲测有效，声音大小基本和win10没区别，而且没有失真，偶尔会出现轻微的爆音(我只试了一个驱动），但是并不影响体验

- dw1820a 蓝牙+wifi+handoff 

    > 电脑接力iphone/ipad不稳定，甚至不能成功，但是反过来iphone/ipad接力mac是可以成功的，蓝牙/wifi工作稳定，但是接力这个情况我怀疑和蓝牙有关，但是我又没有证据

- 电池电量 

    > DSDT补丁修复的，如果不能正常用，君还得自己去给DSDT打补丁，之所以要搞好这个，是为了不想开机出现白底苹果，虽然打好了也不怎么看电量状态,但是这个过程还是学会了DSDT的操作，推荐自己去躺躺坑

- 独立显卡（10.13.6完美，跑过大型游戏，没有问题）

- 触摸板

    > 完美支持手指姿势, 有些时候在偏好设置里面看不到触摸板程序设置，但是这并不影响使用，我之前折腾一天，发现可能是电源的问题，只要把电源线拔了，过会插上，那个触摸板设置就出来

- usb3.1/usb3.0

- 摄像头

- Siri/Icloud

    > 一定要注意重新去换一下三码，序列号，SmUUID，主板序列号，不然早晚有坑等着你，Siri使用需要将有线网卡设置位en0，不然Siri会变成人工智障

- HDMI（这个可以用，但是声音好像有问题，我虽然后面修复了下的，但是没有测试，君可自行测试/解决）

- 键盘灯(可亮不可调)

# 不能做什么
---
- 屏幕背光（我怀疑和没有核显有关)
- AirPlay（(因为CPU无核显，声音可以投）
- 耳机不能用麦克风（因为我用的万能声卡，感觉AppleALC可以成功，但是懒得折腾了）

# 工具功能说明
---
|名称|功能|
|--|--|
|Clover Configurator|clover config.list文件配置|
|CloverThemeManager|clover引导主题下载安装器|
|KCPM Utility Pro|权限修复，重建缓存及其kext安装|
|MaciASL|DSDT反编译|
|NVIDIA® WebDriver Updater|独立显卡驱动下载器，适合那种不好找的独显驱动，尤其是系统升级后无法老驱动无法使用，新驱动又不好找的情况, 下载速度还可以|
|Hackintool|配置信息及其系统接口检测，同时也可以更新驱动和一些efi文件|

# 建议
---
​	建议将系统装到固态里面，看具体需求分大小，我100G够用了，固态加载会快很多，开机20秒内（带自动登陆），给自己一个macos的极致体验，win10和macos可以双系统，只是安装的macos时候可能会把win的引导给干掉，但是可以用pe修复下, 系统完善后，强烈建议用时光机备个份，自己分一个机械硬盘分区出来就好，反正你一般用不完1T的机械，那种1T+的同学就完全可以不担心空间了，备份好后就可以使劲折腾了，折腾进不去系统了重新还原下就好，还有就是EFI也记得要备份，不然后面驱动有得你找的。
