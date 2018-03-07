## JAVA 修饰符

***

### 1. 访问控制修饰符 default, private, public, and protected
- #### 1.1 default (即缺省，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。

- #### 1.2 private : 在同一类内可见。使用对象：变量、方法。 注意：不能修饰类（外部类）

- #### 1.3 public : 对所有类可见。使用对象：类、接口、变量、方法

- #### 1.4 protected : 对同一包内的类和所有子类可见。使用对象：变量、方法。 注意：不能修饰类（外部类）。

*** 

### 2. 非访问限制修饰符 static, final, abstact, synchronized, transient and volatile
- ### 2.1 static
```
2.1.1 静态变量：
static 关键字用来声明独立于对象的静态变量，无论一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。

2.1.2 静态方法：
static 关键字用来声明独立于对象的静态方法。静态方法不能使用类的非静态变量。静态方法从参数列表得到数据，然后计算这些数据。

对类变量和方法的访问可以直接使用 classname.variablename 和 classname.methodname 的方式访问。
```
