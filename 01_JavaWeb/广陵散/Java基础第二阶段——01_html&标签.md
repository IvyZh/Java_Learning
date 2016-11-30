# Java基础第二阶段——01_html&标签

Tags ：Html 标签


---


> 写在前面：之前是学习的黑马74期web，然后看了差不多第一天视频的一半，发现课程结构比较少，不如之前学过的广陵散老师讲的详细。印象当中学web的时候，好像第一个学习也不是gls老师了，总想找到当初的感觉，翻看之前写的blog，应该是在2014年8月12日开始接触学习的web了，时间过得好快啊。只可惜找不到之前学的是哪位老师的了，反正觉得当时学的很稳，不像类似这样二刷的时候有点耐不住性子了。


先总体的截下课程目录的图：

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161123121026.png)

传智播客-广陵散老师的视频


> 接下来开始第一天的学习了

* 学习视频：JavaWeb 广陵散
* 录制时间：2015年4月14日


* 视频目录：

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161123121121.png)

  
* 视频时长：4小时24分钟

		章节 使用 # 
		每日视频 ## 



## 01-html的简介

* Day01 思维导图

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161124010624.png)

* 学一个知识，怎么来学？一般都是如下三个步骤.
	- 是什么？
	- 能做什么？
	- 怎么做？

- 学Java基础的时候，毕向东老师说过学语言只需要关注两点就好
	- 表现形式（格式）
	- 什么时候用

> 资料：HtmlHelp.chm

> 工具：EditPlus


* 标签
	* font
		* 属性 color：取值 red green blue
		* 属性 size：取值 5



* HTML介绍
	* 什么是html？
		- HyperText Markup Language：超文本标记语言，网页语言
			* 超文本：超出文本的范畴，使用html可以轻松实现这样操作
			* 标记：html所有的操作都是通过标记实现的，标记就是标签，<标签名称>
			* 网页语言：
	* 第一个html程序。
		- 创建java文件.java
			* 先编译，然后再运行（jvm）
		- html后缀是 .html .htm
			* 直接通过浏览器就可以运行
		- 代码
			* `这是我的<font size="5" color="red">第一个html程序！</font>`
	* html的规范（遵循）
		1. 一个html文件开始标签和结束的标签  `<html>  </html>`
			- 定义一个java方法 { }
		* html包含两部分内容 
			- `<head> 设置相关信息</head>` ,在这个标签里面可以设置title标签
			- `<body> 显示在页面上的内容都写在body里面</body>`
		* html的标签有开始标签，也要有结束标签
			-` <head></head>`
		* html的代码不区分大小写的
		* 有些标签，没有结束标签 ，在标签内结束
			- `比如 换行  <br/>  <hr/>`


## 02-html的操作思想

> 操作思想很重要

**网页中有很多数据，不同的数据可能需要不同的显示效果，这个时候需要使用标签把要操作的数据包起来（封装起来），通过修改标签的属性值实现标签内数据样式的变化。
一个标签相当于一个容器，想要修改容器内数据的样式，只需要改变容器的属性值，就可以实现容器内数据样式的变化。**

## 03-文字标签和注释标签

### 常用的标签

* 文字标签：修改文字的样式
	* `<font></font>`
	* 属性	
		* color:文字颜色 取值范围 1-7,超出了7，默认还是7
		* size：文字大小
			* 两种表示方式
				* 英文单词：red  green  blue  black  white  yellow   gray......
				* 使用十六进制数表示 #66cc66、RGB

* 注释标签
	- java注释几种？三种
	- html的注释 ： `<!--  html的注释  -->` 源码里面会有，但是页面显示的时候不会有


## 04-标题标签和水平线标签和特殊字符

### 常用的标签

* 标题标签
	- `<h1></h1>  <h2></h2>  <h3></h3> .......<h6></h6>`
	- 从h1到h6，大小是依次变小，同时会自动换行

* 水平线标签
	- `<hr/>`
	- 属性
		* size: 水平线的粗细 取值范围 1-7
		* color: 颜色
	- 代码
		`<hr size="5" color="blue"/>`


* 特殊字符:显示特殊字符的时候就需要用到转义
	* 比如想在网页上显示：`<html>:是网页的开始！` 这段文字，该怎么操作呢？
	* 需要对特殊字符进行转义
		* <    `&lt;`
		* >    `&gt;`
		* 空格：`&nbsp;`
		* &  :` &amp;`


## 05-列表标签

### 常用的标签

* 列表标签
	* 比如现在显示这样的效果


			传智播客
				  财务部
				  学工部
				  人事部


		- `<dl> </dl>`: 表示列表的范围
			* 在dl里面  `<dt></dt>`: 上层内容
			* 在dl里面  `<dd></dd>`：下层内容
		- 代码(为了md编译器显示，我做了特殊字符的转义
			
			&lt;dl&gt;
	
			&lt;dt&gt;传智播客&lt;/dt&gt;
	
			&lt;dd&gt;财务部&lt;/dd&gt;	
		
			&lt;dd&gt;学工部&lt;/dd&gt;
	
			&lt;dd&gt;人事部&lt;/dd&gt;
	
			&lt;/dl&gt;

	* 想要在页面上显示这样的效果
	
			  1. 财务部
			  2. 学工部
			  3. 人事部
		
			  a. 财务部
			  b. 学工部
			  c. 人事部
		
			  i. 财务部
			  ii. 学工部
			  iii. 人事部

		- `<ol></ol>` : 有序列表的范围
			- 属性 type：设置排序方式 1(默认)  a  i
		   	- 在ol标签里面 `<li>具体内容</li>`
			- 代码（需要看源代码

				<ol>
					<li>财务部</li>
					<li>学工部</li>
					<li>人事部</li>
				</ol>

	* 想要在页面上显示这样的效果
	
			特殊符号（方框） 财务部
			特殊符号（方框） 学工部

		- `<ul></ul>` : 表示无序列表的范围
			属性： type: 空心圆circle 、实心圆disc 、实心方块square ，默认disc
			在ul里面  `<li></li>`
		- 代码（需要看源代码
			<ul type="circle">
				<li>财务部</li>
				<li>学工部</li>
				<li>人事部</li>
			</ul>


## 06-图像标签

### 常用的标签

* 图像标签
	* `<img src="图片的路径"/>`
		- src: 图片的路径
		- width：图片的宽度
		- height：图片的高度
		- alt: 图片上显示的文字，把鼠标移动到图片上，停留片刻显示内容,如果图片加载不出来，可以作为提示文字
			* 有些浏览器下不显示（没有效果）

## 07-路径的介绍

* 路径的分类
	* 绝对路径：
		* C:\Users\asus\Desktop\0413\day01\code\a.jpg 
		* http://www.baidu.com/b.jpg
	* 相对路径：一个文件相对于另外一个文件的位置
		* 三种
			* html文件和图片在一个路径下，可以直接写文件名称
				- `<img src="b1.jpg" alt="这是一个美女"/>	`	
			* 图片在html的下层目录,在html文件中，使用img文件夹下面的a.jpg
				- C:\Users\asus\Desktop\0413\day01\code\   4.html
				- C:\Users\asus\Desktop\0413\day01\code\   img\a.jpg
				* 在html中使用图片 4.html和img在一个路径下
				
					img\a.jpg
			* 图片在html文件的上层目录
				- C:\Users\asus\Desktop\0413\day01\   code\4.html
				- C:\Users\asus\Desktop\0413\day01\   c.png

				* html文件所在的目录和图片是一个目录
					* 图片和html文件是什么关系？
						- 图片在html的所在目录的上层目录 day01
					* 怎么表示上层路径  `../`
					* `../` : day01
						- `../c.png`
					* 想要表示上层的上层 `../../`

## 08-案例一列表标签使用

实现如下效果：
	[效果图](http://w)



要点：

* 标签可以嵌套
* 注意转义字符

## 09-超链接标签一

* 超链接的两种（链接资源、定位资源）
	* 链接资源
		* `<a href="链接到的资源地址">显示到网页面上的内容</a>`
		* 属性：href 链接到的资源地址
		* 属性：target 设置打开方式，默认是在当前页打开
			* _blank：在新的窗口使用
			* _self：在当前页面打开
		* `<a href="">显示到网页面上的内容2</a>`
			* 会打开页面所在文件目录
		* `<a href="">显示到网页面上的内容3</a>`
			* 当超链接不需要到任何的地址 在href里面加#



## 10-超链接标签二

* 超链接的两种
	* 定位资源
		* 如果想要定位资源：定义一个位置 
			* `<a name="top">顶部</a>`
		* 回到这个位置
			* `<a href="#top">回到顶部</a>`

* 原样输出标签 `<pre>内容</pre>`


## 11-表格标签一（重要

* 表格标签的作用
	* 可以对数据进行格式化，使数据显示更加清晰

* 用到的标签
	* `<table></table>`: 表示表格的范围
	* 在table里面 `<tr></tr>`
	* 在tr里面 `<td></td>`

![分析](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161125133839.png)


* 步骤
	* 首先定义一个表格的范围使用table
		* caption ：写在table里面，表示表格的标题
	* 定义一行使用 tr
	* 定义一个单元格使用 td
	

> 操作技巧：首先数有多少行 ，数每行里面有多少个单元格


* table属性
	* border="1" 表格线
	* bordercolor="blue"
	* cellspacing="0" 单元格的间隙
	* width
	* height
* tr属性
	* align：left right center

> 使用`th`也可以表示单元格：自带居中和加粗效果

## 12-表格标签二

* 单元格合并（td的属性
	* rowspan：跨行
		* `<td rowspan="3">人员信息</td>`
	* colspan：跨列
		* `<td colspan="3">人员信息</td>`



## 13-上午内容总结

重点：

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161124010624.png)


---
下午。

## 14-表单标签一

1. 表单标签是什么？能做什么？怎么做？
	1. 可以提交数据到开心网的服务器，这个过程可以使用表单标签实现

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161130013552.png)


* 表单标签
	* `<form></form>`: 定义一个表单的范围
	* `<input type="输入项的类型"/>`：可以输入内容或者选择内容的部分,**在输入项里面需要有一个name属性**
		* `<input type="输入项的类型"/>`
			* `<input type="text"/>`
			* `<input type="password"/>`
			* `<input type="radio"/>`
				* 在里面需要属性 **name**，name的属性值必须要相同
				* 必须有一个**value**值
				* 实现默认选中的属性 `checked="checked"`
			* `<input type="checkbox"/>`
				* 在里面需要属性 name，name的属性值必须要相同
				* 必须有一个value值
				* 实现默认选中的属性 `checked="checked"`
			* `<input type="file"/>`
	* `<select name="birth">`：下拉输入项（不是在input标签里面的）
		* 默认选择:`selected="selected"`
	
				<select name="birth">
					<option value="1991">1991</option>
					<option value="1992">1992</option>
					<option value="1993">1993</option>
				</select>

	* `<textarea cols="10" rows="10"></textarea>`：文本域
	* `<input type="hidden" />` : 隐藏项（不会显示在页面上，但是存在于html代码里面,具体应用呢？）
	* `<input type="submit" value="注册"/>` ：提交按钮


			- file:///C:/Users/asus/Desktop/0413/day01/code/10-表单标签一.html
			 ?sex=on&love=on&love=on&birth=1991
			
			当在输入项里面写了name属性之后 
			- file:///C:/Users/asus/Desktop/0413/day01/code/10-表单标签一.html
			?phone=2222&pwd=3333&sex=on&love=on&birth=1993&tex=aaaaaaaa&hid=


			- file:///C:/Users/asus/Desktop/0413/day01/code/10-表单标签一.html?
			phone=130111111&pwd=123456&sex=nv&love=y&love=p&love=pp&birth=1992&tex=good+love&hid=

			** ?输入项name的值=输入的值&
			** 参数类似于key-value形式

> 如果不设置form表单的action，那么数据就会提交到当前页面

- `<form></form>`: 定义一个表单的范围
	- 属性
		- action： 提交到地址，默认提交到当前的页面，`<form action='01-hello.html'></form>`

## 15-表单标签二

- `<form></form>`: 定义一个表单的范围
	- 属性
		- action： 提交到地址，默认提交到当前的页面，`<form action='01-hello.html'></form>`
		- method: get和post，默认是get请求
			- 面试题目： get和post区别
			
					1、get请求地址栏会携带提交的数据，post不会携带（请求体里面。在第七天时候讲http协议时候）
					2、get请求安全级别较低，post较高
					3、get请求数据大小的限制，post没有限制
		- enctype：一般请求下不需要这个属性，做文件上传时候需要设置这个属性（第22天时候讲文件上传）

- `<input type="image" src="图片路径"/>`：使用图片提交
- `<input type="reset"/>`：重置按钮： 回到输入项的初始状态
- `<input type="button" value=""/>` ：普通按钮(和明天讲js在一起使用的)

## 16-案例使用表单标签实现注册的页面

![](https://github.com/IvyZh/Java_Learning/blob/master/01_JavaWeb/%E5%B9%BF%E9%99%B5%E6%95%A3/imgs/QQ%E6%88%AA%E5%9B%BE20161130233759.png)

- 使用表格实现页面效果
		- 超链接不想要他有效果 `href="#"`
		- 如果表格里面的单元格没有内容， 使用空格作为占位符 `&nbsp`;
		- 使用图片提交表单 `<input type="image" src="图片的路径"/>`


Code:

	<html>
	 <head>
	  <title>HTML示例</title>
	 </head>
	 <body>
		<h2>注册传智播客的账号</h2>
		<form action="01-hello.html">
		<table  width="100%">
			<tr>
				<td align="right">注册邮箱：</td>
				<td><input type="text" name="mail"/></td>
			</tr>
			<tr>
				<td>&nbsp;</td>
				<td>你可以使用 <a href="#">账号</a>注册或者使用 <a href="#">手机号</a>注册</td>
			</tr>
			<tr>
				<td align="right">创建密码：</td>
				<td><input type="password" name="pwd"/></td>
			</tr>
			<tr>
				<td align="right">真实姓名：</td>
				<td><input type="text" name="realname"/></td>
			</tr>
			<tr>
				<td align="right">性别：</td>
				<td><input type="radio" name="sex" value="nv"/>女 <input type="radio" name="sex" value="nan"/>男</td>
			</tr>
	
			<tr>
				<td  align="right" >生日：</td>
				<td>
					<select name="year">
						<option value="1945">1945</option>
						<option value="1931">1931</option>
						<option value="1949">1949</option>
					</select>年
					<select name="month">
						<option value="10">10</option>
						<option value="11">11</option>
						<option value="12">12</option>
					</select>月
					<select name="day">
						<option value="30">30</option>
						<option value="10">10</option>
						<option value="25">25</option>
					</select>日
	
				</td>
			</tr>
	
			<tr>
				<td  align="right">我现在：</td>
				<td>
					<select name="now">
						<option value="study">我正在上学</option>
						<option value="work">我已经工作</option>
					</select>
	
				</td>
			</tr>
	
			<tr>
				<td>&nbsp;</td>
				<td><img src="verycode.gif"/> <a href="#">看不清换一张?</a></td>
			</tr>
	
			<tr>
				<td align="right">验证码：</td>
				<td><input type="text" name="verycode"/></td>
			</tr>
	
			<tr>
				<td>&nbsp;</td>
				<td><input type="image" src="btn_reg.gif"/></td>
			</tr>
		</table>
	</form>
	 </body>
	</html>


## 17-其他标签的使用

	b : 加粗
	s ：删除线
	u ：下划线
	i ：斜体
	
	pre ：原样输出
	
	sub : 下标
	sup : 上标

	p ：段落标签 比br标签多一行
	
	====明天css时候一直使用
	div ：自动换行
	span：在一行显示,不会换行


## 18-html的头标签的使用


- html两部分组成 head和body
	- 在head里面的标签就是头标签
		- title标签：表示在标签上显示的内容
		- `<meta>`标签：设置页面的一些相关内容，早期的关键词
			- `<meta name="keywords" content="毕姥爷，熊出没，刘翔">`
			- `<meta http-equiv="refresh" content="3;url=01-hello.html"/>`:3秒中定时跳转
		- base标签：设置超链接的基本设置（可以统一设置超链接的打开方式 
			-  `<base target="_blank"/>`
		- link标签：引入外部文件
			-  明天css，可以使用link标签引入css文件

## 19-框架标签的使用(会用
- 其实这个是过时的，但是还是要了解下，会用就可以
	- 工具：HTML Help

	* `<frameset>`
		- rows:按照行进行划分
			* `<frameset rows="80,*">`

		- cols:按照列进行划分
			* `<frameset cols="80,*">`
	* `<frame>`
		- 具体显示的页面
			- `<frame name="lower_left" src="b.html"> `

> 使用框架标签时候，不能写在body里面，使用了框架标签，需要把body去掉

Code:

	<html>
	 <head>
	  <title>HTML示例</title>
	 </head>
		<frameset rows="80,*">
				<frame name="top" src="a.html"/>
	
				<frameset cols="80,*">
					<frame name="left" src="b.html"/>
					<frame name="right"/>
				</frameset>
				
		</frameset>
	
	</html>

b.html

	<html>
	 <head>
	  <title>HTML示例</title>
	 </head>
	 <body>
	
		<h1>bbbbbbb</h1>
	
		<a href="01-hello.html" target="right">超链接1</a>
		<a href="02-标题和水平线和特殊字符.html" target="right">超链接2</a>
		<a href="03-列表标签.html" target="right">超链接3</a>
	 </body>
	</html>

分析：

	<frameset rows="80,*">                        //把页面划分成上下两部分 
	     <frame name="top" src="a.html">             //上面页面
	
		<frameset cols="150,*">                     //把下面部分划分成左右两部分
			<frame name="lower_left" src="b.html">  //左边的页面
			<frame name="lower_right" src="c.html"> //右边的页面
		</frameset> 
	</frameset> 

## 20-html文件中文乱码

* EditPlus
	* 备份去掉
	* Html模板
	* 乱码：使用系统默认编码就不会出现中文乱码的情况


> 扩展知识：

	a标签的扩展（了解）
		- 百度是网络资源
		- 当a标签里面访问网络资源时候，必须要加一个协议 http：表示一个网络的公共协议，
		 如果加上http协议之后，自动识别访问资源是一个网络资源
	
		- 当浏览器里面找到相关协议，首先看这个协议是不是公共协议http。
		如果不是公共协议，会去本地电脑找支持这个协议的应用程序。


## 21-今天内容的总结

	1、html操作思想（****）
		* 使用标签把要操作的数据包起来，通过修改标签的属性值，来实现标签内数据样式的变化
	2、font标签 属性：size 取值范围 1-7  color：英文单词，十六进制数 #ffffff
	3、标题标签 <h1></h1>.....<h6></h6> : 从h1到h6越来越小，自动换行
	4、注释 <!-- html的注释 -->

	5、列表标签
		** <dl> <dt></dt> <dd></dd></dl>
		** 有序 <ol><li></li></ol>
		** 无序 <ul><li></li></ul>
	
	6、图像标签(******)
		<img src="图片的路径" width="" height="" alt=""/>
		**  alt:浏览器兼容性很差
	
	7、路径（相对路径）(****)
		** 在同一级目录 ：直接写
		** 在下一层目录： images/1.jpg
		** 在上层目录： ../
	
	8、超链接标签（*****）
		<a href="路径">显示在页面上的内容</a>
		- 打开方式 target="_self  _ blank"
		- 默认是在当前页面打开
	
	9、表格标签（*****）
		<table>
			<tr>
				<td></td>
				<th></th>  //加粗和居中
			</tr>
		</table>
		- 技巧：先数有多少行，数每行里面有多少个单元格
	
	10、表单标签（*** 今天最重要的标签***）
		* <form></form>: 
			- action: 提交到地址
			- method：提交方式 ：常用的有两种 get和post
			- get和post区别

			- enctype属性（上传时候使用）
		* 输入项
			* 输入项里面写name属性
			* 普通输入项 <input type="text"/>
			* 密码：password
			* 单选框：radio
			* 复选框：checkbox
			* 下拉框
				<select name="">
					<option value=""></option>
				</select>
			* 文本域
				<textarea cols="" rows="" name=""></textarea>
			
			* 文件 file

			* 提交按钮 submit
			* 重置  reset
			* 使用图片提交 <input type="image" src=""/>

			* 隐藏项 hidden
			* 普通按钮 button
		
	11、div和span(******)

	12、框架标签（会用）
---

Day01 End.

 