## DOL的配置 14353313##

###描述

>分布式操作层（DOL）是一个软件开发框架编程并行应用程序。DOL允许指定的基础上计算的Kahn过程网络模型应用程序和功能的基础上的SystemC模拟引擎。此外，DOL提供了一个基于XML的规范格式来描述在一个多处理器系统，包括绑定和映射并行应用程序的执行。

###安装过程

####安装必要环境
>1. $ sudo apt-get update
2. $ sudo apt-get update
3. $ sudo apt-get install openjdk-7-jdk
4. $ sudo apt-get install unzip

####下载文件

>1. $ sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
2. $ sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

####解压文件

* 新建dol的文件夹
>$ mkdir dol  

* 将dolethz.zip解压到dol文件夹中
>$ mkdir dol  

* 解压systemc
>$ mkdir dol

####编译systemc

* 解压后进入systemc-2.3.1的目录下
>$ cd systemc-2.3.1

* 新建一个临时文件夹objdir
>$ mkdir objdir

* 进入该文件夹objdir
>$ cd objdir

* 运行configure（能根据系统的环境设置一下参数，用于编译)
>$ ../configure CXX=g++ --disable-async-updates

![aaa](http://p1.bpimg.com/567571/3694d76582bc1cb6.png)

* 编译

![aaa](http://p1.bpimg.com/567571/e4bf59e1456a93c6.png)

* 记录当前的工作路径
>$ pwd

####编译dol
* 进入刚刚的dol文件夹，修改build.xml文件
>property name=”systemc.inc” value=”YYY/include” 
property name=”systemc.lib” value=”YYY/lib-Linux/libsystemc.a”/

* 编译
>$ ant -f build_zip.xml all

* 运行第一个例子

    进入路径

    运行

    成功结果如下图

![aaa](http://p1.bpimg.com/567571/8410370e1e7423f7.png)

w