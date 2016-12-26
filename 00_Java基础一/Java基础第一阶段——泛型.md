## 泛型概述

	ArrayList al = new ArrayList();
	al.add("abc");
	al.add("abc2");
	al.add("abc3");
	al.add(4);//al.add(new Integer(4)) 自动装箱
	
	Iterator it = al.iterator();
	while(it.hasNext()){
		String s = (String) s.next();
		sop(s);// 编译ok，运行报错：class cast Exception
	}

问题：如何在编译的时候就可以检查呢？

JDK1.5之后出现的新特性——泛型，用来解决安全问题，是一个安全机制。

定义集合的时候就要明确类型。

ArrayList<String> al = new ArrayList<String>();//定义了一个容器，这个容器要存放的对象类型是String。将运行时出现的问题ClassCastException转移到了编译时期，方便于程序员解决问题，让运行时期问题减少，安全。

	Iterator<String> it = al.iterator();// 迭代器也要使用泛型就可以直接取出字符串了。
	while(it.hasNext()){
		String s =  s.next();
		sop(s);// 编译ok，运行报错：class cast Exception
	}


## 泛型使用

泛型格式：通过<>来定义要称作的引用数据类型。

在使用java提供的对象时，什么时候写泛型呢？

通常在集合框架中和常见，只要见到<>就要定义泛型。

当使用集合时，将集合中要存储的数据类型作为参数传递到<>即可。


Comparator<T>

	class LenComparator implements Comparator<String>{
	
		public int compare(String s1,String s2){
			int num =  new Integer(s1.length()).compare(new Integer(s2.length()));//倒叙的话，把是s1和s2位置互换
			if(num==0)
				return s1.compareTo(s2);//倒叙的话，把是s1和s2位置互换
			return num;
		}
	}

	TreeSet<String> ts = new TreeSet<String>(new LenComparator());


Comparable<T>


## 泛型类

	class Student{}
	
	class Woker{}
	
	class Tool{
	
		private Object obj;
			
		public void setObj(object o){
			obj = o;
		}
		
		public Object getObj(){
			return obj;
		}
	
	}
	
	class Demo{
	
		public void static main(String[] args){
			Tool t = new Tool();
			t.setObject(new Student());
			Worker w = (Worker)t.getObject();// 早期做法，编译ok，运行报错。
		}
	
	}


修改(泛型类)：

	class Tool<T>{
	
		private T obj;
			
		public void setObj(T o){
			obj = o;
		}
		
		public T getObj(){
			return obj;
		}
	
	}


	Tool<Worker> t = new Tool<Worker>();
	t.setObject(new Student());// 编译报错
	Worker w = t.getObject(); 


什么时候定义泛型类？

> 当类中要称作的引用数据类型不确定的时候，早期定义Object来完成扩展，现在定义泛型类来完成拓展。

### 泛型方法

泛型也可以定义在方法中，


	class Tool<T>{
		public void print(T o){//泛型也可以定义在方法中
			sop(o)
		}
		
		public void show(T o){
			sop(o)
		}
	}

	Tool t = new Tool<String>();
	t.print("12");
	t.show("21");

> 泛型类定义的泛型，早整个类中有效，如何被方法使用，那么泛型类的对象明确要操作的具体类型后，所有要操作的类型就已经固定了。

> 为了让不同方法可以操作不同类型，而且类型还不确定。那么可以将泛型定义在方法上。


	class Tool2{
		public void<T> print(T o){//泛型也可以定义在方法中
			sop(o)
		}
		
		public void<Q> show(Q o){
			sop(o)
		}
	}

	Tool2 t = new Tool2();
	t.show(12);
	t.print("12");
	t.show("12");

> 集合就是泛型类。


## 静态方法泛型

既有泛型方法又有泛型类。

	class Tool2<T>{
		public void print(T o){//泛型也可以定义在方法中
			sop(o)
		}
		
		public void<Q> show(Q o){
			sop(o)
		}
	}

	Tool2<String> t = new Tool2<String>();
	t.print(12);// 编译报错
	t.print("12");//ok
	t.show("12");//ok
	t.show(12);//ok

特殊之处：

	class Tool2<T>{
		public void print(T o){//泛型也可以定义在方法中
			sop(o)
		}
		
		public <Q> void show(Q o){
			sop(o)
		}
		
		public static void print2(T o){// 无法从上下文
			sop(o)
		}
	}

> 静态方法不可以访问类上定义泛型。如果静态方法存在的应用数据类型不确定，可以定义在方法上，

	class Tool2<T>{
		public void print(T o){//泛型也可以定义在方法中
			sop(o)
		}
		
		public void<Q> show(Q o){
			sop(o)
		}
		
		public static <W> void print2(W o){// ok
			sop(o)
		}
	}

	Tool2.print2(123);//ok

位置：放在方法的返回值前面，修饰符后面。


## 泛型接口

	interface Inter<T>{
		show(T t);
	}
	
	class InterImpl implements Inter<String>{
		
		show(String s){
			sop(s);
		}
	}

	new InterImpl().show("hhh");

code2:

	class InterImpl<T> implements Inter<String>{
		
		show(T s){
			sop(s);
		}
	}

	new InterImpl<Integer>().show(123);


## 泛型限定

	public static void main(String[] args){
	
		ArrayList<String> al  = new ArrayList<String>();
		...
		ArrayList<Integer> al1  = new ArrayList<Integer>();
		...
		
		print(al);
		print(al1);
	}
	
	
	public static void print(ArrayList<?> al){
		
		Iterator<?> it = al.iterator();
		while(it.hasNext()){
			sop(it.next());
		}
	
	}


	public static <T> void print(ArrayList<T> al){
		
		Iterator<T> it = al.iterator();
		while(it.hasNext()){
			// T t = it.next(); 区别就是可以操作
			sop(it.next());
		}
	
	}

> ?的应用:泛型限定

class Person{

}

class Student extends Person{

}


main(){
	ArrayList<Student> al = new ArrayList<Student>();
	...
	print(al)；
}

public static void print(ArrayList<Person> al){//ArrayList<Person> al = new ArrayList<Student>();//error
	Iterator<Person> it = al.iterator();
}

public static void print(ArrayList<? extends Person> al){//ok
	Iterator<? extends Person> it = al.iterator();
	...
}


> ?通配符，可以理解为占位符

> 泛型的限定
> ? extends E : 可以接收E类型或者E的子类型。向上限定
> ? super E: 可以接收E类型或者E的父类型。向下类型
