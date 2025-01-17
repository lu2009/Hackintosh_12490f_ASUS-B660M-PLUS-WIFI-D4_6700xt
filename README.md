
### ASUS-B660M-PLUS-WIFI-D4 黑苹果OpenCore EFI

### 注意事项
- 不喜欢OCLP补丁，使用的[itlwm.kext](https://github.com/OpenIntelWireless/itlwm)驱动无线网卡，需下载[HeliPort](https://github.com/OpenIntelWireless/HeliPort.git)搭配使用，也可以编辑itlwm.kext包内的Info.plist文件，添加或修改ssid和password使用。
- RX 6700XT显卡需要的NooTRX.kext，如果你要自己更新驱动，暂时请不要用[Nightly build](https://chefkissinc.github.io/applehax/nootrx/)版本，会导致睡眠唤醒后卡顿到无法使用只能重启，解决办法为使用 [build: Bump deps #219](https://github.com/ChefKissInc/NootRX/actions/runs/11941828922) 这个12月份的版本，2025-1-17目前测试只有此版本没问题
- 请替换三码。
- BIOS版本2024/11/01 3601 没有CFG LOCK开关选项，在OC界面使用grubx64.efi 输入
```bash
setup_var CpuSetup 0x44 0x00
```
即可关闭CFG LOCK

### 硬件配置

|  配置|  型号|
|---|---|
|  CPU| 12th Gen Intel(R) Core(TM) i5-12490F |
|  主板| TUF GAMING B660M-PLUS WIFI D4 |
|  内存| 32 GB 3600 MHz DDR4 |
|  板载网卡|  RTL8125 |
|  网卡+蓝牙| AX201 |
|  声卡| ALC897 |
|  显卡| AMD Radeon RX 6700 XT 12 GB |
|  固态| 西数SN770 1T+SN750 500G|

### 正常
- CPU睿频
- 睡眠/唤醒
- 显卡
- 声卡
- WIFI
- 蓝牙
- USB
### 已知问题
系统日志有ACPI Error，但不影响使用，如果知道解决方案请提交[issues](https://github.com/lu2009/Hackintosh_12490f_ASUS-B660M-PLUS-WIFI-D4_6700xt/issues)



### BIOS 设置
fastboot 关闭

Serial port 关闭

CFG LOCk 关闭
### 一些备忘
查看用户唤醒历史
```bash
pmset -g log|grep -v "DarkWake"|grep -E  "Wake from"
```

查看所有睡眠和唤醒历史
```bash
pmset -g log|grep -E  "Entering Sleep state|Wake from"
```

什么是DarkWake
在 macOS 中，“DarkWake” 和 “Wake” 代表了两种不同类型的唤醒状态：

Wake: 当你听到 “Wake from Sleep”，这意味着系统从睡眠状态完全唤醒。在这种状态下，所有硬件和系统服务都将完全启动，屏幕将被打开，用户可以与系统进行交互。

DarkWake: 这是一种特殊类型的唤醒状态，其中系统会部分唤醒来执行某些任务，但不会完全唤醒，屏幕通常保持关闭，用户界面不可用。这种状态常用于例如电邮或日历更新、Time Machine 备份、网络连接的维护等后台任务。DarkWake 的优势是它允许系统执行必要的任务，同时消耗的电源更少，并保持了大部分的睡眠状态。

总体来说，“DarkWake from Sleep” 和 “Wake from Sleep” 的主要区别在于唤醒的级别和目的。DarkWake 是一种低电量的、部分唤醒状态，用于后台任务，而普通的 Wake 则是完全的唤醒，用于用户交互。
