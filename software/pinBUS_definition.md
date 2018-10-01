# 概述
在Mbed OS 中，应用程序员不需要对GPIO端口和处理器芯片做底层初始化和配置。这些都由操作系统为你完成。虽然你不再需要了解更多的硬件细节，但是你需要通过MCU的硬件来选择处理器的外围电路。<br>例如：
```
DigitalOut green（PC_6); 
DigitalOut red（PC_7); 
```
选择PC_6引脚作为LED的绿灯，选择PC_7引脚作为LED的红灯。 

```
SPI spi(PF_9, PF_8, PF_7); // mosi, miso, sclk
DigitalOut cs(PF_4);
```
选择modular-2的SPI5。
# 主板上使用的引脚
+ LED指示灯
+ SD card
+ EEPROM
# I/O扩展板引脚定义
modular-2主板上有2个16Pin的插座(CN2，CN3)，1个40pin插座(CN1),它们构成了72pin的连接总线，称为pinBUS。pinBUS用于I/O接口模块的扩展。  
## 图例
![引脚图例](https://github.com/maximlab/modular-2/blob/master/software/screenshot/Pins_Legend.jpg?raw=true)
## CN1引脚定义
![CN1引脚定义](https://github.com/maximlab/modular-2/blob/master/software/screenshot/CN1_HEADERS.jpg?raw=true)
## CN2引脚定义
![CN2引脚定义](https://github.com/maximlab/modular-2/blob/master/software/screenshot/CN2_HEADERS.jpg?raw=true)
## CN3引脚定义
![CN3引脚定义](https://github.com/maximlab/modular-2/blob/master/software/screenshot/CN3_HEADERS.jpg?raw=true)
# 网络扩展板引脚定义
modular-2的网络扩展板有1个10pin插座(CN4A)，和一个12pin插座(CN4B)。  
![CN4引脚定义](https://github.com/maximlab/modular-2/blob/master/software/screenshot/CN4_HEADERS.jpg?raw=true)
# 引脚的引用
Mbed程序设计时，通过pinName来定义外设。例如： 
```
#include <mbed.h>
DigitalOut green(PC_6);
main()
{
    green=!green
    wait(1);
}
```
每个IO模块都将说明它们所使用的相关引脚定义，只有你了解引脚定义，才能够调用相关外围电路的类。

