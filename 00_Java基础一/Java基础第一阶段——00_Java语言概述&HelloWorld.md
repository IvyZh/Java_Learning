# Java基础第一阶段——Java语言概述&HelloWorld

Tags ： Java基础

>   记得最初在学习Java的时候，也是学习黑马视频，看的毕向东老师的基础视频。印象当中，学习Java基础知识不下3遍，后来反思下，其实走过了不少冤枉路，也“浪费”了不少的时间在这些基础知识上面，本身是知道基础知识的重要性，但是一遍遍的去学习基础知识，总觉得还是“没劲”、“徒劳”。与其这样，倒不如一次性巩固好这些必要的知识点，然后再投入时间可以学其他的知识领域。也希望这是最后一次来巩固Java基础知识了。


思来想去像是参看毕向东老师的视频学习吧，之前毕向东和刘意老师的视频都从头到尾的学过一遍，毕向东老师的视频看了应该有3遍了吧。。。╮(╯▽╰)╭


既然这是我希望最后的一遍Java基础知识复习，所以要务必做到严谨、完整，以免到后来还要再做一遍。



---

* 学习视频：毕向东35天Java基础_毕向东
* 录制时间：2012年2月19日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161120183500.png)

  
* 视频时长：3小时03分钟



		章节 使用 # 
		每日视频 ## 



# 第一章 Java概述

## 01-计算机语言概述
* 基础常识
	* 软件开发
	* 人机交互
	* 常用的DOS命令


* 软件开发
	* 什么是软件开发？
		* 软件：一系列按照特定顺序组织的计算机数据和指令的集合。
		* 常见的软件：
			* 系统软件
				* DOS、Windows、Linux等
			* 应用软件：
				* QQ、微信
	* 什么是开发？
		* 制作软件


* 人机交互
	* 软件的出现实现了人与计算机之间的更好的交互。
	* 交互方式：
		* 图形化界面（Graphical User Interface）这种方式简单直观，使用者易于接受，容易上手。
		* 命令行方式（Command Line Interface） 需要有一个控制台，输入特定的指令，让计算机完成一些操作。较为麻烦，需要记住一些命令。



* 什么是计算机语言？
	* 语言：是人与人之间用于沟通的一种方式。
	* 计算机语言:人与计算机交流的方式。
		* 如果人要与计算机交流，那么就要学习计算机语言。计算机语言有很多种，如C、C++、Java等。


* Java语言概述
	* 是SUN(Stanford University Network，斯坦福大学网络公司)1995年推出的一门高级编程语言。
	* 是一种面向Internet的编程语言。
	* 随着Java技术在web方面的不断成熟，已经成为Web应用程序的首选开发语言。
	* 是简单易学，完全面向对象，安全可靠，与平台无关的编程语言。


* Java语言的三种技术架构

> 所谓技术架构就是解决不同领域的问题

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161120211630.png)

## 02-Java语言的跨平台原理(JVM)


* Java语言的特点（跨平台性）

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161120212145.png)

虚拟机:虚拟出来的机器，来解析某种程序语言。

JVM：Java 虚拟机，可以用来解析Java程序语言的机器（软件），虚拟机是操作系统和Java程序的桥梁。

虚拟机跨平台么？虚拟机不跨平台。


## 03-Java语言(JDK&JRE)


* Java语言的环境搭建
	* JRE、JDK


* 什么是JRE、JDK？
	* JRE（Java Running Environment Java运行环境）
		* 包括Java虚拟机（JVM）和Java程序所需的核心类库等，如果想运行一个开发好的Java程序，计算机只需要安装JRE即可。
	* JDK（Java Development Kit Java开发工具包）
		* JDK是提供给Java开发人员使用的，其中包含了java的开发工具，也包括了JRE。所以安装了JDK，就不用在单独安装JRE了。其中的开发工具：编译工具(javac.exe) 打包工具(jar.exe)等

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161120213025.png)


## 04-Java语言(JDK的下载与安装)

* JDK的下载
	* oracle官网
* JDK的安装（1.6）
	* 安装好了，其实就是一个绿色版本，最好装在其他盘符下面
	* 安装完毕之后，会弹出一个JRE安装选择框，但是可以不必装，因为JDK会有一个自带的运行时环境。

* JDK的安装（1.7）
	* 注意：JavaFX SDK 设置，是一种脚本语言，更便捷的展现图形界面能力，因为不做这方面的技术开发，所以不需要安装了。



## 05-Java语言(JDK中的命令行工具)


* jdk\bin 
	* 存放Java开发的一些工具
		* javac.exe ：是一个命令行程序，双击执行效果是一闪而过


> 打开DOS命令行，如果想在命令行界面执行命令，必须也要进入该指令所在目录

常见DOS指令

- d: 进入d盘
- cd e:\java 进入 e盘 java目录


## 06-Java语言(命令行简介)

* 常见的DOS命令
	* e:
	* dir  查看当前目录下的文件目录列表
	* cd 改变某个目录(change direct)
		* cd java*  进入第一个java开头的目录
		* cd.. 退到上一级目录
		* cd\ 直接退到根目录
		* cd a\b\c 
	* md 创建目录
	* rd 删除目录
		* rd abc
			* 目录不是空，必须把该目录下面的东西都删除之后，才能删除整个。
		* rd /s abc 删除目录树
		* rd /q abc 安静删除
	* del 1.txt 删除文件
		* del `*.txt`
		* del `*.*  * 是通配符`
	* exit
		* 退出命令行
	* help
		* help cd
		* Linux的命令也有类似的指令 问号？
	* cls


## 07-Java语言(环境变量配置)

* 如何让javac.exe 这个指令可以在任何目录下都可以执行？
	* 比如notepad这个指令
	* 原理
		* > d:notepad 首先会在d盘下面找有没有这个指令，有的话就会执行，没有的话，就在配置好的环境变量中去找，再没找到就会报找不到该执行的提示
	* 因此就可以把JDK的bin目录的路径放在Windows的环境变量里面，记得用路径分隔符“;”分号来区分，环境变量的配置成功之后，需要重新开启一个DOS窗口来测试。


## 08-Java语言(环境变量配置-技巧)

* JDK改了盘符或者目录发生了变化，需要对path需要修改。
	* 这样的方式就存在修改系统路径的风险
	* 可以使用如下方式来避免

			新增一个
			JAVA_HOME系统变量
			JAVA_HOME D:\develop\Java\jdk1.8
			
			Path:
			%SystemRoot%\system32;%SystemRoot%;%SystemRoot%\System32\Wbem;;%JAVA_HOME%\bin;%ADB_PATH%;


## 09-Java语言(环境变量配置-临时配置方式)

* 临时环境变量配置
	* set命令:会列出来本机中所有的环境变量
		* set path 查看path的环境变量，只在当前命令行有效 查看
		* set path=hahaha 修改
		* set path=  删除
		* set path=D:\develop\Java\jdk1.8
		* set path=D:\develop\Java\jdk1.8;%path%  建议配置在前面


## 10-Java语言(Hello World)

* Java程序开发步骤
1.  将Java代码编写到扩展名为.java的文件中。
2.  通过javac命令对该java文件进行`编译`。
3.  通过java命令对生成的class文件进行运行。

			   javac 1.java	          java Demo
		1.java--------------->1.class------------->运行



1.java文件的内容


    class Demo{
    	public static void main(String[] args){
    		System.out.println("Hello World");
    	}
    }


阅读第一位，功能第二位

## 11-Java语言(Hello World细节)

* public static void main(String[] args){ 能保证该类的正常运行
* 任何程序都有一个入口，这个入口就是主函数
* javac 123.java 编译，检查语法正确性
* java Demo 这个时候才会启动虚拟机，找到这个程序，加载到内容，检查是否有主函数，如果有就会执行

## 12-Java语言(Hello World常见问题)

* main-->mian javac不会编译出来这个问题，java运行的时候会报NoSuchMethod保存
* 123.java-->123.java.txt

## 13-Java语言(classpath环境变量)
* NoClassDefFoundError
	* 要么classpath配置错误
	* 要么就是这个类名写错了
* 问题描述，如何在当前路径下运行非当前期路径下的.class文件
	* set classpath=c:\myclass
		* 如果没设置classpath，模拟器就会在当前路径下找
	* set classpath=c:\myclass;
		* 如果在结尾处加上分号，就现在指定目录下找，如果找到就执行，如果没有就会在当前目录下面找。
	* set classpath=.;c:\myclass
		* 显式的设置
	* set classpath=.;%classpath%



* 保证类名和文件名一致性

> 可以在类名前面加上public关键字，这样就提升了类的权限，就会要求类名必须要和文件名一样

	   public class Demo{
	    	public static void main(String[] args){
	    		System.out.println("Hello World");
	    	}
	    }



---

Day01 End.