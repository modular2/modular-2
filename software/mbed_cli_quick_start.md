## 前言
Mbed OS的在线Mbed编译环境实现使用浏览器进行Mbed的云端开发。对于初学者而言这是十分方便的，免去了许多开发环境的安装和配置，而且能方便地实现软件更新和发布，分享。但是在线编译的缺点也十分明显，就是需要良好的网络环境，当网络不通畅时，体验非常糟糕。<br />
如果不使用在线编译，你可以有两个选择：<br />
### 在线IDE导出为第三方编译工具项目
在线编译环境中建立应用程序的代码，通过export导出成第三方编译工具的项目，比如keil uvision项目。浏览器将转换好的项目自动下载下来，然后解压，使用keil工具编译。<br />
### 使用Mbed CLI命令行工具
Mbed CLI是Arm Mbed OS的命令行工具，它可以代码仓库版本控制、依赖管理、代码发布、从其他地方获取代码、调用编译系统及其他。Mbed CLI可以管理多项目，也就是多个项目可以分享同一个Mbed OS的源代码。如果你采用github代码仓库的话，你只需要上传应用程序的代码，而不需要上传几百兆的Mbed OS在github上，同样可以实现代码分享和版本控制。<br />我们在modular-2应用程序的开发过程中，采取将代码保存在github上，使用Mbed CLI实现程序编译的方法。
### Mbed CLI 安装
Windows安装比较简单，官网（https://os.mbed.com/docs/latest/tools/installation-and-setup.html) 直接下载安装。下载链接http://mbed-os.s3-eu-west-1.amazonaws.com/builds/Mbed_installer_v0.4.7.exe
### LINUX安装
需要先安装以下工具
+	Python - mbed CLI 是用Python写的，并且在 version 2.7.13 上做过完整测试，不兼容Python3.x
+ Git - version 1.9.5 or later
+ Mercurial - version 2.2.2 or later
+ GNU ARM - ARM GCC交叉编译工具
<pre><code>$ git clone https://github.com/ARMmbed/mbed-cli
$ python setup.py install'
</code></pre>
参考链接https://docs.mbed.com/docs/mbed-os-handbook/en/5.1/dev_tools/cli/ 
## Windows Mbed CLI运行 
WIN键+R键，cmd回车进入命令行，输入mbed运行，将显示Mbed CLI的常见参数。
<pre><code>C:\>mbed
usage: mbed [-h] [--version]             ...

Command-line code management tool for ARM mbed OS - http://www.mbed.com
version 1.7.2

Use 'mbed <command> -h|--help' for detailed help.
Online manual and guide available at https://github.com/ARMmbed/mbed-cli

optional arguments:
  -h, --help   show this help message and exit
  --version    print version number and exit

Commands:

    new        Create new mbed program or library
    import     Import program from URL
    add        Add library from URL
    remove     Remove library
    deploy     Find and add missing libraries
    publish    Publish program or library
    update     Update to branch, tag, revision or latest
    ......
</code></pre>

mbed config –L检查配置
<pre><code>C:\>mbed config -L
[mbed] Global config:
GCC_ARM_PATH=C:\Program Files (x86)\GNU Tools ARM Embedded\6 2017-q2-update\bin

[mbed] Local config (C:\):
Couldn't find valid mbed program in C:\</code></pre>
如果没有配置下GCC的路径（你安装GNU ARM的路径），请按如下命令设置：
<pre><code>mbed config --global GCC_ARM_PATH "C:\Program Files （x86）\ GNU Tools ARM Embedded\6 2017-q2-update\bin"</code></pre>

## 快速例子
<pre><code>mbed import https://github.com/modular2/helloworld
</code></pre>
<pre><code>cd helloworld
mbed compile –S //检查一下支持列表</code></pre>
