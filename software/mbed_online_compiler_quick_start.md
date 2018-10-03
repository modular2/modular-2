## Mbeb在线编译器使用指南
Mbed OS的在线Mbed编译环境实现使用浏览器进行Mbed的云端开发。对于初学者而言这是十分方便的，免去了许多开发环境的安装和配置，而且能方便地实现软件更新和发布，分享。<br />
### 开始
#### 申请Arm Mbed账号
前往[os.mbed.com](https://os.mbed.com/)，注册申请[Arm Mbed账号](https://os.mbed.com/account/signup/)。<br />
#### 设置开发平台环境
前往[https://os.mbed.com/compiler](https://os.mbed.com/compiler)，使用注册账号登录。在下图中，可以在底部设置界面显示语言。在红框中，点击进入硬件平台添加界面，点击Add Board进入[https://os.mbed.com/platforms/](https://os.mbed.com/platforms/)，进入使用相同CPU的NUCLEO_F429ZI详细页面，点击右侧![Add to your Mbed Compiler]()，完成硬件平台的添加。
### 第一个程序
如上图所示，在平台编译环境中，点击左上角红框中的[import]，点击显示页面里绿框中的[Click here]链接，弹出Import Program对话框，Source URL中输入https://github.com/modular2/helloworld，其他如下图所示，点击Import导入。打开hellowolrd中的main.cpp，点击Compile，开始编译，编译成功后自动下载生成的bin文件。 <br><br>
### 联机烧录
1. 将modular-2设备通过USB(DAPLink接口)连接开发电脑。
2. 将生成的bin文件复制到modular-2生成的存储盘符中。
3. 按复位键启动嵌入式程序。

### 导出为其他IDE工具项目
如果你需要进一步进行调试工作，你可以将源文件导出为其他IDE工具的项目文件。在平台编译环境中，右键点击项目名称，点击弹出菜单中Export Program，在弹出的对话框中，选择Export Toolchain后，点击Exportn确认导出，浏览器将自动下载其他IDE工具项目zip包。例如导出为uVision时，你可以根据下图操作。 



## 其他事项
更多modular-2源码例程: https://github.com/modular2  <br>
更多Mbed在线编译器内容：https://os.mbed.com/docs/v5.10/tutorials/quick-start-online.html
