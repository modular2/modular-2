# 关于modular-2 
Modular2 标准版是一款基于 ARM® Cortex®-M4 内核的模块化物联网微电脑。它采用了模块化的设计理念，硬件部分集成了常用的 10/100M 以太网接口，micro-SD 卡接口，micro-USB（OTG）接口，并创新的预留了可供客户自定义的通讯插槽和 I/O 扩展插槽。软件部分采用了 ARM 最新的基于物联网的开源操作系统 Mbed，并将常用的硬件模块封装成可调用的类，用户可以方便的构建自己的应用程序。  
Modular2 标准版拥有强大的片上处理能力和存储能力，处理器为 32 位的STM32F429，主频 180MHz，内置 FPU 和 DSP 处理器。集成了 DAPLink 接口，方便用户编程与调试。通讯扩展槽支持 WiFi，LoRaNB-IOT 等模块的连接，I/O 扩展槽提供了常用的 UART，SPI，SMbus，I2C，PWM，ADC/DAC 接口，用户可以根据自身产品需求灵活使用。
## 性能指标
+ 内置 32 位处理器 STM32F429ZGT6，主频 180MHz。
+ 符合 IEEE-802.3-2002 标准的 10/100Mbps 以太网接口
+ 支持 OTG 的高速 Micro-AB 接口
+ 支持最高 32GB 的 Micro-SD 卡（SDHC 协议）
+ 支持 DC12~24V 宽电压输入，使用带锁止的插拔式端子
+ 板载 DAPLink 编程/调试接口（Micro-B 接口）
+ 支持 通讯插槽（Communication sockets）
+ 支持 I/O 扩展插槽（I/O expansion sockets）
+ 用户自定义的双色指示灯
+ 1 个复位开关
+ 硬件日历及时钟电池备份功能
+ 使用Arm Mbed OS 5
## 电气规格
| 型号 | Modular2_Standard 
------ | ----------------  
外形尺寸| 158*78*34mm       
外壳材质 |阻燃 ABS|
安装方式 |支持导轨（EN 50022） 
防护等级 | IP20 |
供电电压 | DC12~24V/USB  
最大功耗 |10 Watt（包括接口板最大负载）
工作温度 | -40℃~+55℃
存储温度 |-40℃~+85℃
湿度（40℃）| 最大 93%（无凝露）
通讯方式| WiFi，LoRa，NB-IOT, M2-bus
接口|1x Micro-USB
| |1x Micro-SD
||1x RJ45（10/100Mbit/s）
||SD 卡存储容量 32G（SDHC）
处理器| STM32F429ZGT6（180MHz）
ESD 保护| 4kV/8kV（IEC 61000-6-2）
极性保护| 是
指示灯 |3x 双色 LED
## 设备负载能力
供电来源 |电压范围 |最大电流| 
--------|---------|-------|
USB |+5V 300mA
||+3.3V 300mA
VIN（6P 端子）| +5V 2000mA
||+3.3V 500mA

*建议使用 VIN（6P 端子）供电，这将是最可靠的！* 


