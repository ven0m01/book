##                                                   VPS环境部署之metasploit工具

#### 0X00 基础环境准备

全新 Ubuntu 16.04.6  一台主机   

查看版本

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf1.png" style="zoom: 67%;" />

安装需要的功能，vim ,git 

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf2.png" style="zoom: 67%;" />

安装SSH功能，可以使用SSH工具进行管理，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-ssh1.png" style="zoom: 67%;" />

启动SSH服务，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-ssh2.png" style="zoom: 67%;" />



安装JAVA环境，下载JDK，去官网下载，这里为13.0版本

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-jdk5.png" style="zoom: 67%;" />

下载后，使用XFTP功能将JDK文件上传到系统下，在home目录下建立一个文件夹msf，上传到msf文件夹里，



<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf5.png" style="zoom: 67%;" />



使用xshell工具进行服务器登陆，解压JDK压缩包

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-jdk1.png" style="zoom: 67%;" />

进行JDK安装，新建jdk文件夹，将解压后的文件放到此文件夹下，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-jdk2.png" style="zoom: 67%;" />

打开/etc/profile 文件，将下列代码放到文件最后一行，

export JAVA_HOME=/usr/lib/jdk/jdk-13.0.1
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=.:${JAVA_HOME}/bin:$PATH

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-jdk3.png" style="zoom: 67%;" />

重新加载文件，查看java版本，安装成功

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-jdk4.png" style="zoom: 67%;" />

#### 0X01 安装工具

安装curl 命令，用来下载msf，

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-curl.png" style="zoom: 67%;" />

使用  curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall  命令进行下载，并进行安装

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-install.png" style="zoom: 67%;" />



安装完成后，运行工具，成功完成

<img src="https://github.com/ven0m01/notebook/raw/master/VPS/image/msf-start.png" style="zoom: 67%;" />

