# VPS环境部署之Cobalt  Strike

### 0X00  安装JDK

下载地址 https://www.oracle.com/technetwork/java/javase/downloads/index.html  



在 /etc/profile 文件下 添加JAVA环境变量，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-java1.png" style="zoom: 67%;" />

保存退出后，输入 source /etc/profile  加载文件

安装完成后查看java 版本，命令 java -version，是否安装成功

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-java-v.png" style="zoom: 67%;" />





### 0X01 运行 Cobalt Strike



将Cobalt Strike 工具上传到VPS系统上，如下图：

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs1.png" style="zoom: 67%;" />



查看一下运行程序的权限，是否有X 执行权限，如图：

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs3.png" style="zoom: 67%;" />

运行服务端  ./teamserver   VPS-IP地址     密码   

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs4.png" style="zoom: 67%;" />



客户端程序与服务器程序一样，这里用的是windows客户端，需运行windows版本程序

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs2.png" style="zoom: 67%;" />



这里需在CMD命令行下运行 cobaltstrike.bat程序，不能双击运行，如下图：

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs5.png" style="zoom: 67%;" />



<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs6.png" style="zoom: 67%;" />



连接后，显示操作界面，如下图：

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs7.png" style="zoom: 67%;" />

在日志控制台上方便不同地方的团队人员之间沟通

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-2.png" style="zoom: 67%;" />

环境准备完成



### 0X02 基本用法

共有三个功能区组成

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-1.png" style="zoom: 67%;" />

首先，建立一个监听器，用来接收反弹信息，如下图：

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-3.png" style="zoom: 67%;" />

添加监听器功能，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-4.png" style="zoom: 67%;" />



共有9个payload 选项，选择beacon-https payload， 端口号选择 9999 

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-5.png" style="zoom: 67%;" />

显示创建完成

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-6.png" style="zoom: 67%;" />



生成可执行木马文件 EXE，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-7.png" style="zoom: 67%;" />



将生成的可执行木马EXE 上传到目标系统中，并运行木马文件demo.exe,

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-8.png" style="zoom: 67%;" />



在管理界面中可以看到目标系统已上线，显示了外网的IP地址，内网的IP地址，登陆的用户名，PC机名称

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-9.png" style="zoom: 67%;" />

选中目标，右键选择 进入beacon功能，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-10.png" style="zoom: 67%;" />

在beacon命令提示符下，可以输入系统命令，如  ipconfig 查看IP地址等

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/cs-11.png" style="zoom: 67%;" />