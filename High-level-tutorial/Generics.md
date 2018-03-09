:hotel:[Return to High-level-tutorial Home Page](https://github.com/geophydog/Java/blob/master/High-level-tutorial/README.md)

***

>假定我们有这样一个需求：写一个排序方法，能够对整型数组、字符串数组甚至其他任何类型的数组进行排序，该如何实现？
>答案是可以使用 Java 泛型。
>使用 Java 泛型的概念，我们可以写一个泛型方法来对一个对象数组排序。然后，调用该泛型方法来对整型数组、浮点数数组、字符串数组等进行排序。

__实例__
```java
public class GenericsTest {
    public static < E >  void generics ( E [] inputArray ) {
        for ( E element: inputArray ) {
            System.out.println(element);
        }
    }

    public static void main( String[] args ) {
        Integer[] in = {1, 2, 3, 4, 5};
        Character[] ch = {'a', 'b', 'c', 'd', 'e'};
        Double[] d = {1.1, 2.2, 3.3, 4.4, 5.5};

        generics( in );
        generics( ch );
        generics( d );

    }
}
```

__output__

```
1
2
3
4
5
a
b
c
d
e
1.1
2.2
3.3
4.4
5.5
```
