# IO pinBUS 定义
modular-2 主板上有2个 16Pin的插座（CN2，CN3)，1个40pin 插座（CN1）,它们构成了72 pin 的连接总线，称为pinBUS。用于IO模块的扩展。 程序设计时，通过pinName 来定义外设。例如
```
#include <mbed.h>
DigitalOut LED(PC_6);
main()
{
    LED=!LED
    wait(1);
}
```
每个IO模块都将说明它们所使用的相关pin，只有你了解了pin的定义才能够使用相关外围电路的类。 
## CN2，CN3 的pin定义
![pinBUS](https://github.com/modular2/modular2/raw/master/images/pinBUS.png)
## CN1 的pin定义
# 网络扩展板的pinCOMBUS 定义
modular2上的网络扩展板有1个10pin 插座（CN4A），和一个12pin（CN4B） 
![pinCOMBUS](https://github.com/modular2/modular2/raw/master/images/pinCOMBUS.png)
