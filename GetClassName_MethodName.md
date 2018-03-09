:hotel: [Return to JAVA Home Page](https://github.com/geophydog/Java/blob/master/README.md)

***

## Get ClassName or MethodName

### :one: 适用于非静态方法：this.getClass().getName()

***

### :two: 适用于静态方法：Thread.currentThread().getStackTrace()[1].getClassName()


__1. 获取类名：__
```
1.1 在类的实例中可使用this.getClass().getName();但在static method中不能使用该方法；

2.1 在static method中使用方法:Thread.currentThread().getStackTrace()[1].getClassName();
 ```
 
__ 2. 获取方法名：__
```
在static与非static方法中都用此方法获取方法名
Thread.currentThread().getStackTrace()[1].getMethodName();
```

__ 3. 获取代码行号：__
```
Thread.currentThread().getStackTrace()[1].getLineNumber();
```


__代码示例__
```java
class ClassTest {
    public void printClassName1() {
        System.out.println(this.getClass().getName());
    }

    public void printMethodName1() {
        System.out.println(Thread.currentThread().getStackTrace()[1].getMethodName());
        System.out.println(Thread.currentThread().getStackTrace()[1].getLineNumber());
    }

    public static void printClassName2() {
        System.out.println(Thread.currentThread().getStackTrace()[1].getClassName());
    }

    public static void printMethodName2() {
        System.out.println(Thread.currentThread().getStackTrace()[1].getMethodName());
        System.out.println(Thread.currentThread().getStackTrace()[1].getLineNumber());
    }

}


public class LogicTest {
    public static void main( String[] args ) {
        if ( args.length != 4 ) {
            System.out.printf("Usage: %s p1 p2 p3\n", Thread.currentThread().getStackTrace()[1].getClassName());
        }

        for ( String element: args ) {
            System.out.printf("%s\n", element);
        }

        ClassTest ct = new ClassTest();
        ct.printClassName1();
        ct.printMethodName1();
        ct.printClassName2();
        ct.printMethodName2();
    }
}
```


```
执行 java LogicTest 1 2 3 4
LogicTest 为public 类名
```
__output__
```
1
2
3
4
ClassTest
printMethodName1
8
ClassTest
printMethodName2
17
```
