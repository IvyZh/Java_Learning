# Java基础第一阶段——04_Java语言基础_for语句&函数&数组&if&while&switch&for语句

* 学习视频：毕向东35天Java基础_毕向东
* 录制时间：2012年2月19日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114932.png)

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114948.png)

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114958.png)
  
* 视频时长：1小时24分钟 + 1小时54分钟 + 1小时13分钟 


		章节 使用 # 
		每日视频 ## 


## 01-Java语言基础(语句-For循环嵌套) 

> 格式

	for(int x = 0;x<3;x++){
		for(int y = 0;y<4;y++){
			sop("Hello world!");
		}//4次循环之后y变量会在内存中消失，再次循环x的时候，会再次生成y变量在内存中。
	}

> 大圈套小圈思想


## 02-Java语言基础(语句-For循环嵌套练习)


	*****
	****
	***
	**
	*


![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123224510.png)

## 03-Java语言基础(语句-For循环嵌套练习2)

	*
	**
	***
	****
	*****

	54321
	5432
	543
	54
	5


	1
	22
	333
	4444
	55555
## 04-Java语言基础(语句-For循环嵌套练习-99乘法表&转义字符)


> 九九乘法表

	1*1=1
	1*2=2 2*2=4
	1*3=3 2*3=6 3*3=9

> 转义字符

	\n:回车：
	\t:制表符。
	\b:退格。
	\r: 按下回车键。

	windows系统中回车符其实是由两个符号组成的 \r\n.
	linux中回车符是 \n.

		
	System.out.println("\\hello world\\");

## 05-Java语言基础(语句-For循环嵌套练习3)

	* * * * * 
	 * * * *
	  * * * 
	   * * 
		*

## 06-Java语言基础(语句-break&continue)

break( 跳出) ，continue( 继续)

break语句：应用范围：选择结构和循环结构。

continue语句：应用于循环结构。

注：

	a,这两个语句离开应用范围，存在是没有意义的。
	b,这个两个语句单独存在下面都不可以有语句，因为执行不到。
	c,continue语句是结束本次循环继续下次循环。
	d,标号的出现，可以让这两个语句作用于指定的范围。


> for循环嵌套的break

	xiaoqiang:for (int x=0; x<3 ;x++ )
	{
		wangcai:for (int y=0; y<4 ; y++)
		{
			System.out.println("x="+x);
			break xiaoqiang;
		}
	}


> break continue 无法执行的语句错误


	continue:继续。
	作用的范围：循环结构。
	continue：结束本次循环，继续下次循环。
	如果continue单独存在时，下面不要有任何语句，因为执行不到。

	break:跳出。
	break作用的范围：要么是switch语句，要么是循环语句。
	记住：当break语句单独存在时，下面不要定义其他语句，因为执行不到。
		break跳出所在的当前循环。
		如果出现了循环嵌套，break想要跳出指定的循环，可以通过标号来完成。

> for循环嵌套的continue

	xiaoqiang:for (int x=0; x<3 ;x++ )
	{
		wangcai:for (int y=0; y<4 ; y++)
		{
			System.out.println("x="+x);
			continue xiaoqiang;
		}
		
	}

## 01-Java基础(函数-定义)
* 什么是函数?
	* 定义在类中，具有特定功能的一段独立小程序
	* 函数也称为方法


## 02-Java基础(函数-格式)

* 格式

    	访问修饰符 返回值 函数名(参数){
    		函数体;
			return 返回值；
    	}

## 03-Java基础(函数-细节-void)

> 特殊情况：
	功能没有具体的返回值。

	这时return的后面直接用分号结束。
	返回值类型怎么体现呢？因为没有具体值，所以不可以写具体的数据类型。
	在java中只能用一个关键字来表示这种情况。关键字是：void.

	总结：没有具体返回值时，返回值类型用void来表示。

	注意：如果返回值类型是void，那么函数中的return语句可以省略不写。

## 04-Java基础(函数-细节-错误格式)

* 定义函数可以将功能代码进行封装

* 便于对该功能进行复用

* 函数只有被调用才会被执行

* 函数的出现提高了代码的复用性

* 对于函数没有具体返回值的情况，返回值类型用关键字void表示，那么该函数中的return语句如果在最后一行可以省略不写。

注意：

	•  函数中只能调用函数，不可以在函数内部定义函数。
	•  定义函数时，函数的结果应该返回给调用者，交由调用者处理。


## 05-Java基础(函数-细节-定义思想错误)
> 定义函数时，函数的结果应该返回给调用者，交由调用者处理。

	sop(add(3,4));// 编译报错

	void add(int x,int y){
	
	}
## 06-Java基础(函数-两个明确)

* 两个明确
	* 明确要定义的功能最后的结果是什么？（返回值 
	* 明确在定义该功能的过程中，是否需要未知内容参与运算（参数


## 07-Java基础(函数-两个明确-练习)

> 定义一个功能，在控制台画一个矩形

* 明确一：这个功能的结果是什么？
	* void
* 明确二：这个功能实现过程中是否需要未知内容参与运算？
	* 有，行和列。

> 定义一个功能，比较两个数是否相等。

> 定义一个功能，获取两个数中较大的那个。

## 08-Java基础(函数-两个明确-练习2)

> 定义功能，打印99乘法表

> 根据考生成绩过去学生分数对于的等级


 	public char getLevel(int s){
        char c;
        if(s>90)
            c = 'A';
        else if(s>80&&s<90)
            c = 'B';
        else if(s<80)
            c = 'C';
        return c;//编译报错
    }


    public char getLevel(int s) {
        char c;
        if (s > 90)
            c = 'A';
        else if (s > 80 && s < 90) {
            c = 'B';
        } else {//这样修改，就可以通过编译了
            c = 'C';
        }
        return c;
    }

## 09-Java基础(函数-内存加载过程)
* javac 启动虚拟机
* main函数进**`栈`**
* 依次执行`进栈出栈`操作
## 10-Java基础(函数-重载)

* 什么是重载（overload）
	* 在同一个类中，允许存在一个以上同名函数明知要他们的参数个数或参数类型不同即可。

## 11-Java基础(函数-重载练习)

> 打印乘法表

	public static void printCFB(int num){
	
	}


## 01-Java基础(数组-概述)
* 概念
	* 同一种数据类型的集合，其实数组就是一个容器。
* 好处
	* 方便操作这些元素
## 02-Java基础(数组-定义)
* 格式1
	* 元素类型[] 数组名 =  new 数组类型[数组长度]
		* 如：int[] arr = new int[5];


## 03-Java基础(数组-内存空间的划分)

* 内存的划分
	* 寄存器
	* 本地方法区
	* 方法区
	* 栈内存
	* 堆内存


## 04-Java基础(数组-栈内存)

* 栈内存
	* 存储的都是局部变量（凡是定义在方法中的变量都是局部变量
	* 变量都有自己的作用域，离开了作用域，该变量就会自动释放
	* 局部代码块
## 05-Java基础(数组-堆内存)
* 堆内存
	* 存储的数组和对象（数组就是对象）
	* 凡是new建立的都在堆上
	* 堆内存中的每一个变量都有默认初始化值，根据类型的不同而不同，整数是0，小数是0.0或0.0f，布尔值是false，char类型是 '\u0000',
	* 释放方式：垃圾回收机制
## 06-Java基础(数组-内存图解)

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161124152350.png)
## 07-Java基础(数组-常见问题)

* 数组越界问题：编译没问题，运行报错，ArrayIndexOutOfBoundsException
* 空指针异常：当引用型变量没有任何实体指向时，还在勇气操作实体，就会发生该异常。
* sop(arr);//[I@c17164-----数组的哈希地址值

---

Day04 End.
