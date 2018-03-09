:hotel:[Return to High-level-tutorial Home Page](https://github.com/geophydog/Java/blob/master/High-level-tutorial/README.md)

***

>假定我们有这样一个需求：写一个排序方法，能够对整型数组、字符串数组甚至其他任何类型的数组进行排序，该如何实现？
>答案是可以使用 Java 泛型。
>使用 Java 泛型的概念，我们可以写一个泛型方法来对一个对象数组排序。然后，调用该泛型方法来对整型数组、浮点数数组、字符串数组等进行排序。

__实例1__
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

__output1__

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

__实例2__
```
public class GenericsTest2 {
    public static < T extends Comparable<T>> T maximum( T x, T y, T z ) {
        T max = x;
        if ( y.compareTo( max ) > 0 ) max = y;
        if ( z.compareTo( max ) > 0 ) max = z;

        return max;
    }

    public static void main( String[] args ) {
        System.out.printf("The maximum of %d, %d and %d is %d\n", 3, 4, 5, maximum( 3, 4, 5 ));

        System.out.printf("The maximum of %.1f, %.1f and %.1f id %.1f\n", 3.3, 4.4, 5.5, maximum( 3.3, 4.4, 5.5) );

        System.out.printf("The maximum of '%s', '%s' and '%s' is %s\n", "apple", "orange", "pear", maximum( "apple", "orange", "pear" ));
    }
}
```

__output2__
```
The maximum of 3, 4 and 5 is 5
The maximum of 3.3, 4.4 and 5.5 id 5.5
The maximum of 'apple', 'orange' and 'pear' is pear
```
