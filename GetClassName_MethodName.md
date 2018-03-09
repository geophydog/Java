:hotel: [Return to JAVA Home Page](https://github.com/geophydog/Java/blob/master/README.md)

***

## Get ClassName or MethodName

### :one: 适用于非静态方法：this.getClass().getName()

***

### :two: 适用于静态方法：Thread.currentThread().getStackTrace()[1].getClassName()


__获取类名：__
```
1、在类的实例中可使用this.getClass().getName();但在static method中不能使用该方法；

2、在static method中使用方法:Thread.currentThread().getStackTrace()[1].getClassName();
 ```
 
__获取方法名：__
```
Thread.currentThread().getStackTrace()[1].getMethodName();
```

__获取代码行号：__
```
Thread.currentThread().getStackTrace()[1].getLineNumber();
```
