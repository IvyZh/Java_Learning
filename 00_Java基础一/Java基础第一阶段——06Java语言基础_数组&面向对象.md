# Java基础第一阶段——06Java语言基础_数组&面向对象

* 学习视频：毕向东35天Java基础_毕向东
* 录制时间：2012年2月19日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161128152699.png)
 
* 视频时长：45分钟 + 2小时44分钟


		章节 使用 # 
		每日视频 ## 


## 01-Java基础(二维数组-定义方式&内存图解)
* 一维数组：箱子里面放格子
* 二维数据：箱子里面放小箱子，小箱子里面放格子

格式：


	int[] arr = new int[3];// 一个箱子里面有3个小格子
	
	int[][] arr2 = new int[3][4];// 一个箱子里面有3个小箱子，每个小箱子里面4个格子


打印：
	sop(arr2);
	sop(arr2[0])
	sop(arr2[0][0])

二维数组初始化过程：
![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161204144805.png)

## 02-Java基础(二维数组-内存图解2)

另一种定义二维数组的方法：

	int[][] arr = new int[3][];//只定义了二维数组中的个数，每个二维数组中存放以为数组的长度是不确定的。

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161204151348.png)


	int[] arr = new int[3];  
	System.out.println(arr);//[I@1fb8ee3  @左边是实体的类型。 @右边是实体的哈希值。

	int[][] arr = new int[3][2];//创建一个二维数组，该数组中有3个一维数组，每一个一维数组中有2个元素。
	System.out.println(arr);//直接打印二维数组。   [[I@c17164
	System.out.println(arr[0]);//直接打印二维数组中的角标0的一维数组。 [I@1fb8ee3
	System.out.println(arr[0][0]);//直接打印二维数组中的角标0的一维数组中角标为0的元素。 0



	int[][] arr = new int[3][];
	System.out.println(arr);//直接打印二维数组。   [[I@c17164
	System.out.println(arr[0]);//直接打印二维数组中的角标0的一维数组。null
	System.out.println(arr[0][0]);//直接打印二维数组中的角标0的一维数组中角标为0的元素。 **NullPointerException**



## 03-Java基础(二维数组-另一种定义方式)

	int[][] arr = new int[3][2];
	System.out.println(arr.length);//打印二维数组的长度。其实就是一维数组的个数。
	System.out.println(arr[1].length);//打印二维数组中角标为1一维数组的长度。

	int sum = 0;
	int[][] arr = {{3,1,7},{5,8,2,9},{4,1}};

	for(int x=0; x<arr.length; x++)
	{
		for(int y=0; y<arr[x].length; y++)
		{
				System.out.print(arr[x][y]+",");
			sum += arr[x][y];
			
		}
	}
	System.out.println("sum="+sum);

## 04-Java基础(二维数组-应用场景)

	甲：30 59 28 17
	乙；37 60 22 19
	int[] arr = {{30,59,28,17},{37,60,22,19}};
	int[][][] arr = new int[3][2][4];

升级：Map集合

---


# 第三章 面向对象


## 01-面向对象(概述)
## 02-面向对象(举例)
## 03-面向对象(举例2)
## 04-面向对象(类与对象之间的关系)
## 05-面向对象(类与对象体现)
## 06-面向对象(类与对象体现-细节)
## 07-面向对象(对象的内存体现)
## 08-面向对象(成员变量和局部变量的区别)
## 09-面向对象(成员变量和局部变量的同名&显示初始化)
## 10-面向对象(类类型参数)
## 11-面向对象(匿名对象)
## 12-面向对象(基本数据类型参数传递图解)
## 13-面向对象(引用数据类型参数传递图解)
## 14-面向对象(封装-代码示例)
## 15-面向对象(封装-思想)


---

Day06 End.

 
