# C#学习笔记

## 委托

委托相当于函数指针

看上去像抽象方法，但实际上和类是一个级别的，可以写在类外部。

```c#
//声明一个委托
public delegate double  Func(double  x); 

```

创建委托实例：

```c#
Func d1 = new Func(objA.MyMethod); //非静态方法
Func d2 = new Func(ClassA.MyMethod); //静态方法
//简写
Func d1 = objA.MyMethod;
Func d2 = ClassA.MyMethod;//classA为类名
```

调用委托实例：

```c#
//像方法一样调用
double result = d2(8.9)；
```



### 泛型委托

C#内置了两个委托

- Action：返回值为void的委托。

  > 有16个重载Action，Action<T>,Action<T,T>....尖括号中是参数类型，从0到15个参数。

- Func：返回值不为void的委托。

  > Func<T>,Func<T,T>....， 最后一个范型参数是返回值类型。



### 多播委托

- 一个委托实例可以指向多个方法，即“包含”多个函数

- 调用委托就是调用其中多个函数
- 多个函数的先后顺序是没有意义的，只是一个函数集合。返回值也就没有太多意义。
- 运算符“+”，“-”，“+=”，“-=”可以动态的增减其中的函数。提高了程序的灵活性

```C#
//多播委托
Func multiFun = fun1 +fun2;
multiFun += fun3
//调用
multiFun(1.2)
```

实例：

```C#
class Calculator{
	public void add(int a, int b){
		console.WriteLine($"{a} + {b} = {a+b}");
	}
	public void sub(int a, int b){
		console.WriteLine($"{a} + {b} = {a-b}");
	}
	public void mul(int a, int b){
		console.WriteLine($"{a} + {b} = {a*b}");
	};
	public void div(int a, int b){
		console.WriteLine($"{a} + {b} = {a/b}");
	}

}

class Test{
	static void main(){
		calculator cal = new calculator();
		Action<int, int> p = cal.add;
		p += cal.sub;
		p += cal.mul;
		p += cal.div;
		p(5,8);
	
	}

}

output:
5+8=13
5-8=-3
5*8=0
5/8=0
```



### C#中的匿名方法

```C#
// 定义委托类型
delegate int Fun(int x);

//创建委托实例，指向一个匿名方法.
Fun fun = delegate(int k) {
      return k+1; 
};

int x=fun(4); //调用委托，也就是调用匿名方法

```

```C#
或者利用内置的委托类型:

Func<int,int> fun = delegate(int k) {
      return k+1; 
};

int x=fun(4); 

```

```c#
匿名方法可以代码中临时定义，可以直接访问局部变量。
int n = 0;
Func d = delegate() { 
     ++n; //可以直接使用局部变量 
};

```



### 委托的好处

- 委托相当于函数指针
- 但它类型更安全，不会指向非法函数地址。
- 功能更强大，有多播功能



## 事件

- 事件是一种消息机制 
- 事件发布类（事件源）触发事件，别的类可以订阅（监听）事件
- 事件是一种特殊的多播委托实例
  - 事件 ： 委托实例
  - 事件处理函数：委托实例（事件）指向的函数
  - 事件触发：调用委托实例

### 创建过程

- 委托类型定义

  - 全局申请，定义处理函数的格式

  ```
  public delegate void ClickHanlder(object sender, ClickEventArgs args); 
  ```

- 事件的创建（事件发布类）

  - 声明事件（创建委托实例）

  ```
  public event ClickHandler OnClick;
  ```

  - 触发事件

  ```
   某个方法中调用 OnClick(this, args);
  ```

- 事件的订阅

  - 添加事件

  ```
  button1.OnClick += new ClickHandler(Btn_OnClick);                  button1.OnClick += Btn_OnClick2;
  ```

  

### Winform中的事件

例如：按钮点击事件

```C#
//为button1的事件Click，添加事件处理函数
this.button1.Click += new System.EventHandler(this.button1_Click);

```

事件处理函数

```C#
//事件处理函数
private void button1_Click(object sender, EventArgs e) 
{ 
        this.label1.Text = “Hello,World!”;
}
```



### 事件与委托的关系

- 事件是一种特殊的多播委托实例

- 限制条件

  - 使用event 关键词

  - “谁申明，谁触发”（事件发布者）

  - 事件监听者一般不是事件发布者

  - 只能使用+，-来订阅事件



## Lambda表达式

Lambda表达式是一种匿名函数

```c#
delegate void Fun(string n);

Fun printf = delegate (string s){
      Console.WriteLine(s);
};

//简写
Func printf = (string s) => { Console.WriteLine(s); };

//参数类型一般可以省略
Func printf = (s) =>{Console.WriteLine(s);};

//如果只有一个语句，{} 可以省略
Func printf = (s) =>Console.WriteLine(s);

//如果只有一个参数，（）可以省略
Func printf = s => Console.WriteLine(s);

//多个参数和多条语句时，不能省略括号
Func2 print5 = (s, n) => {
        Console.Write(s + ",");
        Console.Write(n);
};
```



Lambda 表达式和委托具有等价的效果。

例如：Array类的ForEach方法有一个委托参数Action，可以传入Lambda 表达式来实现不同遍历操作。

```C#
int[] array = {1, 2, 3, 4};

Array.ForEach(array, action);//Array类的ForEach方法

//遍历打印每一个元素
Array.ForEach(array, m => console.WriteLine(m));

//求和
int sun = 0;
Array.ForEach(array, m => sum += m);
```



## C#中的异常

几种常用的异常类

```C#
System.OutOfMemoryException  ：内存不足
System.StackOverflowException ：栈溢出
System.NullReferenceException ：空指针/空引用
System.InvalidCastException ：转型错误
System.ArrayTypeMismatchException：数组类型不匹配
System.IndexOutOfRangeException ：数组/集合下标越界
System.MulticastNotSupportedException：不支持多播
System.ArithmeticException ：算数运算异常
System.DivideByZeroException ：除0错误
```



### 异常的处理

- 造成异常的原因是什么？
- 用户非法输入、上层调用下层方法使用了不合法的参数
  - 在产生非法输入和非法参数的那个方法去处理。
- 程序的Bug
  - 不用捕获，或者捕获后记录日志，供程序员修改。

- 运行环境的错误
  - 能否通过程序处理？•如果不能处理，向上抛出，通知上层方法。



## 命名空间

- 命名空间的概念  
  - 逻辑划分; 避免类名冲突

- 命名空间的声明
  - namespace xxx.xxxx { } 
  - 可嵌套 

- 命名空间的导入
  - using xxx.xxxx; 

- 使用别名 
  - using 别名 =命名空间或类名;

