# Java基础第一阶段——05_Java语言基础_数组操作&排序&查找

* 学习视频：毕向东35天Java基础_毕向东
* 录制时间：2012年2月19日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114932.png)
 
![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114948.png)

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161123114958.png)
* 视频时长：1小时24分钟 + 1小时54分钟 + 1小时13分钟 


		章节 使用 # 
		每日视频 ## 


## 01-Java基础(数组-第二种定义格式)
* 第一种格式：不知道具体的值
	* int[] arr = new int[3];
* 第二种格式：知道具体的值
	* int[] arr = new int[]{1,2,3,4,5};
	* int[] arr = {1,2,3,4,5};
## 02-Java基础(数组-常见操作-遍历)
* for循环
* 数组的一个属性
	* length

> 倒序遍历

## 03-Java基础(数组-常见操作-最值)

* 两种方式
	* 取脚标index
	* 取值element
## 04-Java基础(数组-常见操作-选择排序)

* 排序
	* 选择排序
	* 冒泡排序


- 选择排序
	> 选择排序（Selection sort）是一种简单直观的排序算法。它的工作原理是每一次从待排序的数据元素中选出最小（或最大）的一个元素，存放在序列的起始位置，直到全部待排序的数据元素排完。 选择排序是不稳定的排序方法（比如序列[5， 5， 3]第一次就将第一个[5]与[3]交换，导致第一个5挪动到第二个5后面）。


code:


![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161128152700.png)

## 05-Java基础(数组-常见操作-冒泡排序)


- 冒泡排序
	- 比较相邻的元素。如果第一个比第二个大，就交换他们两个。
	- 对每一对相邻元素作同样的工作，从开始第一对到结尾的最后一对。在这一点，最后的元素应该会是最大的数。
	- 针对所有的元素重复以上的步骤，除了最后一个。
	- 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。


code:

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161128154638.png)


> Java类中自带的排序：Arrays.sort(arr);

> 最快的排序：希尔排序

## 06-Java基础(数组-常见操作-排序位置置换代码提取)

抽取swap方法：交换数组中两个数据的位置swap(int[] arr,int x,int y)

## 07-Java基础(数组-排序的性能问题)


	public static void selectSort(int[]a)
	{
	    if((a==null)||(a.length==0))
	        return;
		int minIndex=0;
	    int temp=0;// 可以改为temp = a[0];
	    for(int i=0;i<a.length-1;i++)
	    {
	        minIndex=i;//无序区的最小数据数组下标
	        for(intj=i+1;j<a.length;j++)
	        {
	            //在无序区中找到最小数据并保存其数组下标
	            if(a[j]<a[minIndex])
	            {
	                minIndex=j;
	            }
	        }
	        if(minIndex!=i)
	        {
	            //如果不是无序区的最小值位置不是默认的第一个数据，则交换之。
	            temp=a[i];
	            a[i]=a[minIndex];
	            a[minIndex]=temp;
	        }
	    }
	}

code:

![](https://github.com/IvyZh/Java_Learning/blob/master/00_Java%E5%9F%BA%E7%A1%80%E4%B8%80/imgs/QQ%E6%88%AA%E5%9B%BE20161128160955.png)

## 08-Java基础(数组-常见功能-查找)

- 基础：for循环实现+判断

## 09-Java基础(数组-常见功能-折半查找)

> 二分查找又称折半查找，优点是比较次数少，查找速度快，平均性能好；其缺点是要求待查表为有序表，且插入删除困难。因此，折半查找方法适用于不经常变动而查找频繁的有序列表。首先，假设表中元素是按升序排列，将表中间位置记录的关键字与查找关键字比较，如果两者相等，则查找成功；否则利用中间位置记录将表分成前、后两个子表，如果中间位置记录的关键字大于查找关键字，则进一步查找前一子表，否则进一步查找后一子表。重复以上过程，直到找到满足条件的记录，使查找成功，或直到子表不存在为止，此时查找不成功。

## 10-Java基础(数组-常见功能-折半查找练习)

code:

	public static int halfSearch(int[] arr,int key)
	{
		int max,min,mid;
		min = 0;
		max = arr.length-1;
		mid = (max+min)/2;
		
		while(arr[mid]!=key)
		{
			if(key>arr[mid])
				min = mid + 1;
			else if(key<arr[mid])
				max = mid - 1;

			if(max<min)
				return -1;

			mid = (max+min)/2;
		}
		return mid;
	}

code2:

	public static int halfSearch_2(int[] arr,int key)
	{
		int max,min,mid;
		min = 0;
		max = arr.length-1;

		while(min<=max)
		{
			mid = (max+min)>>1;

			if(key>arr[mid])
				min = mid + 1;
			else if(key<arr[mid])
				max = mid - 1;
			else
				return mid;
		}
		return -1;
	}


> 给定一个有序的数组，如果往该数组中存储一个元素，并保证这个数组还是有序的，
那么个元素的存储的角标为如何获取。
{13,15,19,28,33,45,78,106};


code1:

	public static int halfSearch_2(int[] arr,int key)
	{
		int max,min,mid;
		min = 0;
		max = arr.length-1;

		while(min<=max)
		{
			mid = (max+min)>>1;

			if(key>arr[mid])
				min = mid + 1;
			else if(key<arr[mid])
				max = mid - 1;
			else
				return mid;
		}
		return min;
	}

> int index = Arrays.binarySearch(arr,45);//如果存在返回的具体的角标位置，不存在返回的是  -插入点-1


	public static int halfSearch_2(int[] arr,int key)
	{
		int max,min,mid;
		min = 0;
		max = arr.length-1;

		while(min<=max)
		{
			mid = (max+min)>>1;

			if(key>arr[mid])
				min = mid + 1;
			else if(key<arr[mid])
				max = mid - 1;
			else
				return mid;
		}
		return -min-1;//如果存在返回的具体的角标位置，不存在返回的是  -插入点-1
	}



## 11-Java基础(进制转换_1)

> 获取一个整数的16进制表现形式。

code1:

	public static void toHex(int num)
	{

		for(int x=0; x<8; x++)
		{
			int temp = num & 15;
			if(temp>9)
				System.out.print((char)(temp-10+'A'));
			else
				System.out.print(temp);
			num = num >>> 4;
		}
		/*
		int n1 = num & 15;
		System.out.println("n1="+n1);

		num = num >>> 4;
		int n2 = num & 15;
		System.out.println("n2="+n2);
		*/
	}


## 12-Java基础(进制转换_2-查表法)


	什么时候使用数组呢？
	如果数据出现了对应关系，而且对应关系的一方是有序的数字编号。并作为角标使用。
	这时就必须要想到数组的使用。
	
	就可以将这些数据存储到数组中。 
	根据运算的结果作为角标直接去查数组中对应的元素即可。

	这种方式：称为查表法。


code2:

	public static void toHex_2(int num)
	{

		if(num==0)
		{
			System.out.println("0");
			return ;
		}
		//定义一个对应关系表。
		char[] chs = {'0','1','2','3',
						'4','5','6','7',
						'8','9','A','B',
						'C','D','E','F'};
		/*
		一会查表会查到比较的数据。
		数据一多，就先存储起来，在进行操作。
		所以定义一个数组。 临时容器。
		*/
		char[] arr = new char[8];
		int pos = arr.length;

		while(num!=0)
		{
			int temp = num&15;
			arr[--pos] = chs[temp];
			num  = num >>> 4;
		}

		System.out.println("pos="+pos);
		for(int x=pos ;x<arr.length; x++)
		{
			System.out.print(arr[x]);
		}


	}


## 13-Java基础(进制转换_整合)

> 二进制 八进制 十六进制


	class ArrayTest3 
	{
		public static void main(String[] args) 
		{
	//		toHex(26);
			toBinary(-6);// 注意负数
	//		toOctal(26);
			System.out.println(Integer.toBinaryString(-6));
		}
	
		//十进制-->十六进制。
		public static void toHex(int num)
		{
			trans(num,15,4);
		}
		//十进制-->二进制。
		public static void toBinary(int num)
		{
			trans(num,1,1);
		}
		//十进制-->八进制。
		public static void toOctal(int num)
		{
			trans(num,7,3);
		}
	
		public static void trans(int num,int base,int offset)
		{
	
			if(num==0)
			{
				System.out.println("0");
				return ;
			}
			//定义一个对应关系表。
			char[] chs = {'0','1','2','3',
							'4','5','6','7',
							'8','9','A','B',
							'C','D','E','F'};
			/*
			一会查表会查到比较的数据。
			数据一多，就先存储起来，在进行操作。
			所以定义一个数组。 临时容器。
			*/
			char[] arr = new char[32];
			int pos = arr.length;
	
			while(num!=0)
			{
				int temp = num & base;
				arr[--pos] = chs[temp];
				num  = num >>> offset;
			}
	
			for(int x=pos ;x<arr.length; x++)
			{
				System.out.print(arr[x]);
			}
			System.out.println();
	
		}
	
	}




## 14-Java基础(查表法练习)


code:

	class ArrayTest4 
	{
		public static void main(String[] args) 
		{
			String week = getWeek(71);
			System.out.println(week);
		}
		/*
		使用查表法。
		星期。
		String s = "abc";
		int x = 4;
		*/
		public static String getWeek(int num)
		{
	
			if(num>7 || num<1)
			{
				return "错误的星期";
			}
			String[] weeks = {"","星期一","星期二","星期三","星期四","星期五","星期六","星期日"};
	
			return weeks[num];
		}
	
	}



--------------

Day05 End.
