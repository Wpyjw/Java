安装JDK:
1.在ORACLE官网下载对应的JDK
2.将文件解压到D:\JDK路径下
3.键我的电脑->属性->高级->环境变量->系统变量
新建变量名 JAVA_HOME，变量值    D:\JDK
修改变量 Path ，在最前面加上    %JAVA_HOME%\bin;  确定
4.cmd java -version 如果显示版本，则安装成功。

继承：子类拥有父类的所有属性和方法  Private修饰的属性和方法无效
语法规则：

class 子类 extends 父类
class Dog extends Animal{

}

方法的重写： 返回值类型、方法名和参数类型及个数 都要与父类继承的方法相同。
public void eat(){
    System.out.printlv();
}

public void eat(){
  
}


final关键字 可以修饰类、方法、属性和变量
类：不允许被继承
方法：不允许被覆盖
属性：该类的属性不会进行隐式的初始化（类的初始化属性必须有值）或在构造方法中赋值
变量：该变量的值只能赋一次值。

多态：对象的多种形态
1.引用多态 
父类的引用可以指向本类的对象
父类的引用可以指向子类的对象
2.方法多态

多态中的引用类型转换
1.向上类型转换（隐式、自动类型转换），是小类型到大类型的转换
2.向下类型转换（强制类型转换），是大类型到小类型
instanceof运算符，来解决引用对象的类型，避免类型转换的安全性问题 
if(animal instanceof Cat){
}
else{
  System.out.println("无法进行类型转换")
}

JAVA中的抽象类
使用abstract修饰
a.某个父类只是知道其子类应该包含怎样的方法，但无法准确知道这些子类如何实现这些方法
b.从多个具有相同特征的类中抽象出一个抽象类，以这个抽象类作为子类的模板，从而避免了子类设计的随意性。

作用：限制规定子类必须实现某些方法，但不关注实现细节

a.abstract定义抽象类
b.abstract定义抽象方法，只有声明，不需要实现
c.包含抽象方法的类是抽象类
d.抽象类中可以包含普通的方法，也可以没有抽象方法
e.抽象类不能直接创建，可以定义引用变量  

抽象方法没有方法体以分号结束。

接口：接口可以理解为一种特殊的类，由全局常量和公共的抽象方法所组成。
interface关键字
修饰符 interface 接口名 extends  父接口1，父接口2{
    零个到多个常量定义
    零个到多个抽象方法的定义
}

使用接口：一个类可以实现一个或多个接口，实现接口使用implements关键字。Java中一个类只能继承一个父类，是不够灵活的，通过实现多个接口可以做补充。

进程：程序（任务）的执行过程 持有资源（共享内存，共享文件）和线程
线程是系统中最小的执行单元

进程的交互：互斥 同步
java对线程的支持：Thread类  Runnable接口 
线程的创建和启动

线程：
三种实现方式：
1.继承Thread类
public class KillThread extends Thread{
    public KellThread(){
    
    }
    public void run(){
        
    }
}

KillThread Thread1=new KillThread();
Thread1.start();
2.实现Runnable接口
public class Battle implements Runnable{
    public Battle(){
    
    }
    public void run(){
    
    }
}
Battle battle1=new Battle();
new Thread(battle1).start();
3.使用匿名类
Thread t1=new Thread(){
    public void run(){
    
    }
};


try catch
如果文件不存在，try 里的代码会立即终止，程序流程会运行到对应的catch块中
e.printStackTrace() 会打印出方法的调用痕迹

![类](https://github.com/Wpyjw/Java/blob/master/612.png)



作用范围最小原则
private>package>protected>public

当一个属性被static修饰的时候，就叫做类属性，又叫做静态属性 
当一个属性被声明成类属性，那么所有的对象，都共享一个值 


