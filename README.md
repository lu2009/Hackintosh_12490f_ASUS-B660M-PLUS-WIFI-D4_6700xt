
### ASUS-B660M-PLUS-WIFI-D4 黑苹果OpenCore EFI

### 注意事项
- 不喜欢OCLP补丁，使用的itlwm.kext驱动无线网卡，需下载HeliPort搭配使用  https://github.com/OpenIntelWireless/HeliPort.git
- RX 6700XT显卡需要的NooTRX.kext，如果你要自己更新驱动，暂时请不要用Nightly build版本，会导致睡眠唤醒后卡顿到无法使用只能重启，解决办法为使用 https://github.com/ChefKissInc/NootRX/actions/runs/11941828922 这个12月份的版本，2015-1-17目前测试只有此版本没问题
请替换三码。

### 硬件配置

|  配置|  型号|
|---|---|
|  CPU| 12th Gen Intel(R) Core(TM) i5-12490F |
|  主板| ASUS-TUF-B660M-PLUS-WIFI-D4 |
|  内存| 32 GB 3600 MHz DDR4 |
|  板载网卡|  RTL8125 |
|  网卡+蓝牙| AX201 |
|  声卡| ALC897 |
|  显卡| AMD Radeon RX 6700 XT 12 GB |
|  固态| 西数SN770 1T+SN750 500G|

### 正常
- 睡眠/唤醒
- 显卡
- 声卡
- WIFI
- 蓝牙
- USB
[itlwm](https://github.com/OpenIntelWireless/itlwm)
### 已知问题
系统日志有ACPI Error，但不影响使用，如果知道解决方案请提交[issues](https://github.com/lu2009/Hackintosh_12490f_ASUS-B660M-PLUS-WIFI-D4_6700xt/issues)
2025-01-16 20:32:02.497547+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.497547+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.497548+0800  localhost kernel[0]: (AppleACPIPlatform) Method parse/execution failed
2025-01-16 20:32:02.497548+0800  localhost kernel[0]: (AppleACPIPlatform) Method parse/execution failed
2025-01-16 20:32:02.497549+0800  localhost kernel[0]: (AppleACPIPlatform) [\_SB.PC00.RP09.PXSX] (Node ffffff9039ad99d0)
2025-01-16 20:32:02.497550+0800  localhost kernel[0]: (AppleACPIPlatform) [\_SB.PC00.RP09.PXSX] (Node ffffff9039ad99d0)
2025-01-16 20:32:02.497550+0800  localhost kernel[0]: (AppleACPIPlatform) , AE_NOT_FOUND
2025-01-16 20:32:02.497551+0800  localhost kernel[0]: (AppleACPIPlatform) , AE_NOT_FOUND
2025-01-16 20:32:02.497551+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psparse-632)
2025-01-16 20:32:02.497551+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psparse-632)
2025-01-16 20:32:02.502518+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Warning: \_GPE:
2025-01-16 20:32:02.502519+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Warning: \_GPE:
2025-01-16 20:32:02.502520+0800  localhost kernel[0]: (AppleACPIPlatform) Missing expected return value
2025-01-16 20:32:02.502520+0800  localhost kernel[0]: (AppleACPIPlatform) Missing expected return value
2025-01-16 20:32:02.502521+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/nsrepair-311)
2025-01-16 20:32:02.502522+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/nsrepair-311)
2025-01-16 20:32:02.503774+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.503775+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.503776+0800  localhost kernel[0]: (AppleACPIPlatform) [UHSM]
2025-01-16 20:32:02.503776+0800  localhost kernel[0]: (AppleACPIPlatform) [UHSM]
2025-01-16 20:32:02.503776+0800  localhost kernel[0]: (AppleACPIPlatform)  Namespace lookup failure, AE_NOT_FOUND
2025-01-16 20:32:02.503777+0800  localhost kernel[0]: (AppleACPIPlatform)  Namespace lookup failure, AE_NOT_FOUND
2025-01-16 20:32:02.503778+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psargs-463)
2025-01-16 20:32:02.503778+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psargs-463)
2025-01-16 20:32:02.503780+0800  localhost kernel[0]: (AppleACPIPlatform) [\___] @00042 #002D:
2025-01-16 20:32:02.503780+0800  localhost kernel[0]: (AppleACPIPlatform) [\___] @00042 #002D:
2025-01-16 20:32:02.503782+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503782+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503782+0800  localhost kernel[0]: (AppleACPIPlatform) No Local Variables are initialized for method ["\" ]
2025-01-16 20:32:02.503783+0800  localhost kernel[0]: (AppleACPIPlatform) No Local Variables are initialized for method ["\" ]
2025-01-16 20:32:02.503784+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503784+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503785+0800  localhost kernel[0]: (AppleACPIPlatform) No Arguments are initialized for method ["\" ]
2025-01-16 20:32:02.503785+0800  localhost kernel[0]: (AppleACPIPlatform) No Arguments are initialized for method ["\" ]
2025-01-16 20:32:02.503786+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503786+0800  localhost kernel[0]: (AppleACPIPlatform) <missing message>
2025-01-16 20:32:02.503787+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.503788+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Error:
2025-01-16 20:32:02.503788+0800  localhost kernel[0]: (AppleACPIPlatform) Method parse/execution failed
2025-01-16 20:32:02.503789+0800  localhost kernel[0]: (AppleACPIPlatform) Method parse/execution failed
2025-01-16 20:32:02.503789+0800  localhost kernel[0]: (AppleACPIPlatform) [\] (Node ffffff8012a6cae0)
2025-01-16 20:32:02.503790+0800  localhost kernel[0]: (AppleACPIPlatform) [\] (Node ffffff8012a6cae0)
2025-01-16 20:32:02.503790+0800  localhost kernel[0]: (AppleACPIPlatform) , AE_NOT_FOUND
2025-01-16 20:32:02.503791+0800  localhost kernel[0]: (AppleACPIPlatform) , AE_NOT_FOUND
2025-01-16 20:32:02.503791+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psparse-632)
2025-01-16 20:32:02.503792+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/psparse-632)
2025-01-16 20:32:02.503818+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Warning: \_GPE:
2025-01-16 20:32:02.503819+0800  localhost kernel[0]: (AppleACPIPlatform) ACPI Warning: \_GPE:
2025-01-16 20:32:02.503819+0800  localhost kernel[0]: (AppleACPIPlatform) Missing expected return value
2025-01-16 20:32:02.503820+0800  localhost kernel[0]: (AppleACPIPlatform) Missing expected return value
2025-01-16 20:32:02.503821+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/nsrepair-311)
2025-01-16 20:32:02.503821+0800  localhost kernel[0]: (AppleACPIPlatform)  (20160930/nsrepair-311)



### BIOS 设置
fastboot 关闭

Serial port 关闭

CFG LOCk 关闭


BIOS没有CFG LOCK开关选项，在OC界面使用grubx64.efi 输入 setup_var CpuSetup 0x44 0x00
即可关闭CFG LOCK

