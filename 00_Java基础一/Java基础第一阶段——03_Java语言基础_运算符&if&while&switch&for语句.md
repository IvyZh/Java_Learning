# Java基础第一阶段——03_Java语言基础_运算符&if&while&switch&for语句

* 学习视频：毕向东35天Java基础_毕向东
* 录制时间：2012年2月19日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161122153706.png)

  
* 视频时长：4小时55分钟



		章节 使用 # 
		每日视频 ## 

## 01-Java语言基础(比较运算符&逻辑运算符)

* 比较运算符
> `==、!=、 >、 <、 >=、 <=`

* 逻辑运算符（用于连接两个布尔类型的表达式

> `&、|、^、 &&（短路）、||（短路）、!`

## 02-Java语言基础(逻辑运算符)

> 内容同上

## 03-Java语言基础(位运算符)

* 用于二进制数的运算

> `<<、>>、>>>、&、|`


Demo1:

	6 & 3

	  0000-0000 0000-0000 0000-0000 0000-0110
	& 0000-0000 0000-0000 0000-0000 0000-0011
	-----------------------------------------
	  0000-0000 0000-0000 0000-0000 0000-0010  --> 2


	6 | 3
	  0000-0000 0000-0000 0000-0000 0000-0110
	| 0000-0000 0000-0000 0000-0000 0000-0011
	-----------------------------------------
	  0000-0000 0000-0000 0000-0000 0000-0111  --> 7


	6 ^ 3
	  0000-0000 0000-0000 0000-0000 0000-0110
	^ 0000-0000 0000-0000 0000-0000 0000-0011
	-----------------------------------------
	  0000-0000 0000-0000 0000-0000 0000-0101  --> 5
 

> 一个数异或同一个数两次，结果还是这个数

> `~` 反码

	sop(~6);//-7


	 0000-0000 0000-0000 0000-0000 0000-0110

	 1111-1111 1111-1111 1111-1111 1111-1001 --> -7!!!!! 这是6的反码，和
	                                  

* 一个负数在计算机的表现形式？
	* 对应的正数，取反再加一。

> -5 在计算机中表达为：11111111 11111111 11111111 11111011。转换为十六进制：0xFFFFFFFB。 

	5的二进制：
		0000-0000 0000-0000 0000-0000 0000-0101
	取反：
		1111-1111 1111-1111 1111-1111 1111-1010
	加1：
		1111-1111 1111-1111 1111-1111 1111-1011

> 看到一个二进制字符串如何知道它的十进制？

	* 第一位是0开头
		* 表示是正数，直接按位对应的权重求出来即可
	* 第一位是1开头
		* 表示是负数，举例说明。


> 二进制 11111111 11111111 11111111 11110110 对应的十进制是多少？

	先取反：
		11111111 11111111 11111111 11110110
		00000000 00000000 00000000 00001001
	再加1：
		00000000 00000000 00000000 00001010 -->10
	结论：
		对应的十进制是 -10

## 04-Java语言基础(移位运算符)

*　左移　<<
	*　最高位舍弃，末尾补0
	* 2的次幂运算
* 右移 >
	* 最高位是什么，空位就补什么
	* 除以2的运算

* 无符号右移 >>>
	* 空位统一用0补


## 05-Java语言基础(位运算符练习-1)

* 最快的速度算出2乘以8的结果


## 06-Java语言基础(位运算符练习-2)

* 两个变量的值互换

		int a = 3,b = 4;
		
		// ...
	
		sop(a+","+b);// 期望得到4,3的结果


- 方法1：
	 - 引入temp值
	 
- 方法2：(不建议这样使用，容易越界)
	 
		a = a+b;
		b = a-b;
		a = a-b;
- 方法3：
	
		a = a^b;
		b = a^b;
		a = a^b;
## 07-Java语言基础(三元运算符)

格式：

	(条件表达式)?x:y;

## 08-Java语言基础(三元运算符-举例)

> 获取两个数中的较大值。

 	int max = a>b?a:b;

> 三个整数中的最大值

	int max = a>b?(a>c?a:c):(b>c?b:c);

## 09-Java语言基础(语句-if格式一)

> 程序的流程控制

* 顺序
* 判断
* 选择
* 循环


- if 的三种表现形式

> 1

	if(条件表达式){
	
	}

> 2

	if(条件表达式){
	
	}else{
	
	}

> 3

	if(条件表达式1){
	
	}else if(条件表达式2){
	
	}else if(条件表达式3){
	
	}else{

	}


## 10-Java语言基础(语句-if格式二)

	int a = 3,b;
	
	if(a>1)
		b = 100;
	else
		b = 200;

	sop(b);

> 三元运算符就是if...else语句的简写格式

## 11-Java语言基础(语句-if格式三)

	if(条件表达式1){
	
	}else if(条件表达式2){
	
	}else if(条件表达式3){
	
	}else{

	}

> 只有一个语句块会执行

## 12-Java语言基础(局部代码块)

> 局部代码块：定义在主函数里面


> 作用？

	凡在主函数定义的变量，都叫做局部变量。
	离开了局部代码块的变量，外部是不能访问到的，因此，可以作为节省内存空间来使用。

## 13-Java语言基础(if语句练习-星期)

> 根据用户输入的数据，判断数据对应的星期一

编写代码的流程：

> 需求-->思路-->步骤-->代码


## 14-Java语言基础(if语句练习-季节)

> 输入月份，输出对应的四季

## 15-Java语言基础(语句-switch)

格式：

	switch(表达式){
		case 取值1：
			执行语句;
			break;
		case 取值2：
			执行语句;
			break;
		...
		default:
			执行语句;
			break;
	}

> swicth 一加载，所有的case语句都会加载到内存

swicth的表达式值有以下几种取值：

	> byte short int char String 枚举


Demo:

	int x = 2;
	switch(x){
		default:
			sop("d");
		case 4:
			sop("a");
		case 3:
			sop("b");
			break;
		case 1:
			sop("c);
			break;
	}// 输出结果：dab


## 16-Java语言基础(语句-switch-练习)

> 使用switch改写 日期和季节的示例.

## 17-Java语言基础(if语句和switch语句的区别)

> if 和 switch 的使用场景

	* switch 针对固定的值，因为switch语句会讲具体的答案都加入内存，所以效率会高一点

## 18-Java语言基础(语句-while)

* 格式

		while(条件表达式){
			执行语句;
		}

## 19-Java语言基础(语句-dowhile)


* 格式

		do{
			执行语句;
		}while(条件表达式)；



## 20-Java语言基础(while练习-累加思想)

> 练习：求1到10这个10个数字的和。

> 主要掌握这种累加的思想

## 21-Java语言基础(while练习-计数器思想)

> 1-100之间6的倍数出现的次数。



## 22-Java语言基础(语句-for)

> 格式

	for(初始化表达式;循环条件表达式;循环后的操作表达式){
		执行语句;//循环体
	}

变形1：

	int x = 1;
	for(sop(a);x<3;sop(c)){
		sop(d);
		x++;
	}// 输出结果 a d c d c


变形2：

	for(int a = 0,b= 1;a<3;a++,b--){
		执行语句;//循环体
	} 


## 23-Java语言基础(for练习&for和while的区别)

> 用for完成累加

for 循环可以节省内存空间，因为会释放循环变量，如果这个变量要使用就可以使用while了

* 无限循环

		while(true){
		
		}

		for(;;){//中间不写，默认是true
		
		}

## 24-Java语言基础(循环结构的使用场景)

> 什么时候使用循环结构？

	当对一个条件进行一次判断时，可以使用if
	当对一个条件使用多次判断时，可以使用while
	注意:要明确哪些语句是需要参与循环的
	条件+循环次数


---

Day03 End.



