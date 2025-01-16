
### ASUS-B660M-PLUS-WIFI-D4 黑苹果OpenCore EFI

请替换三码。

硬件配置

|  配置|  型号|
|---|---|
|  CPU| 12th Gen Intel(R) Core(TM) i5-12490F |
|  主板| ASUS-TUF—B660M-PLUS-WIFI-D4 |
|  内存| 32 GB 3600 MHz DDR4 |
|  板载网卡|  RTL8125 |
|  网卡+蓝牙| AX201 |
|  声卡| ALC897 |
|  显卡| AMD Radeon RX 6700 XT 12 GB |
|  固态| 西数SN770 1T+SN750 500G|

正常
- 睡眠/唤醒
- 声卡
- WIFI
- 蓝牙
- USB
### 已知问题


### BIOS 设置
fastboot 关闭

Serial port 关闭

CFG LOCk 关闭


BIOS没有CFG LOCK开关选项，在OC界面使用grubx64.efi 输入 setup_var CpuSetup 0x44 0x00
即可关闭CFG LOCK




记录

RX 6700XT显卡需要添加 NOOTRX.kext 驱动 ，注意不要用Nightly build版本，会导致睡眠唤醒后卡顿到无法使用只能重启，解决办法为使用https://github.com/ChefKissInc/NootRX/actions/runs/11941828922 这个12月份的版本，测试只有此版本没问题
