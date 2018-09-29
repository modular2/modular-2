# 概述
&ensp;&ensp;在Mbed OS 中，应用程序员不需要对GPIO 端口和处理器芯片做底层初始化和配置。这些都由OS 为你完成了。这是非常方便的。虽然你不再需要了解更多的硬件细节，不过你需要通过MCU的硬件来选择处理器的外围电路。例如：
```
DigitalOut green（PC_6); 
DigitalOut red（PC_7); 
```
选择了PC_6 引脚作为LED的绿灯。选择了PC_7 引脚作为LED的绿灯。 

```
SPI spi(PF_9, PF_8, PF_7); // mosi, miso, sclk
DigitalOut cs(PF_4);
```
选择了STM32F429ZI 的SPI5.
#主板上使用的引脚
+ LED指示灯
+ SD card
+ EEPROM
# IO扩展板引脚定义
modular-2 主板上有2个 16Pin的插座（CN2，CN3)，1个40pin 插座（CN1）,它们构成了72 pin 的连接总线，称为pinBUS。用于IO模块的扩展。  
## 图标
![pinCOMBUS](https://github.com/modular2/modular2/raw/master/images/pinref.png)
## CN2，CN3 的pin定义
![pinBUS](https://github.com/modular2/modular2/raw/master/images/PINBUS.png)
## CN1 的pin定义
![pinCOMBUS](https://github.com/modular2/modular2/raw/master/images/PINBUS2.png)
# 网络扩展板引脚定义
modular2上的网络扩展板有1个10pin 插座（CN4A），和一个12pin（CN4B）。  
![pinCOMBUS](https://github.com/modular2/modular2/raw/master/images/pinCOMBUS.png)
#引脚的引用
 程序设计时，通过pinName 来定义外设。例如： 
```
#include <mbed.h>
DigitalOut green(PC_6);
main()
{
    green=!green
    wait(1);
}
```
每个IO模块都将说明它们所使用的相关pin，只有你了解了pin的定义才能够使用相关外围电路的类。

