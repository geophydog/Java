:hotel: [Return to JAVA Home Page](https://github.com/geophydog/Java)
***

### :one: Constructor method of class

```
当一个类初始化时会自动调用该类的构造函数，子类会调用父类的构造函数。
```
```java
class A {
    int a;
    String string;
    public A() {
        System.out.println("Class A!");
    }
}

class B extends A {
    public B() {
        System.out.println("Class B!");
    }
}

class C extends B {
    public C( int a, String string ) {
        this.a = a;
        this.string = string;
        System.out.println("Class C!");
    }
}

class D {
    int a;
    String string;
}

public class Constructors {
    public static void main( String[] args ) {
        A a = new A();
        B b = new B();
        C c = new C(10, "CLASS C");
        System.out.println(c.a + " " +  c.string);
    }
}
```
#### output:
```
Class A!
Class A!
Class B!
Class A!
Class B!
Class C!
10 CLASS C
```

***

### :two: Java特殊写法： 给类的字段赋值
```java
class D {
    int a;
    String string;
}

public class Constructors {
    public static void main( String[] args ) {
        D d = new D(){{a = 20; string = "CLASS D";}};
        System.out.println(d.a + " " + d.string);
    }
}
```
#### output:
```
20 CLASS D
```
