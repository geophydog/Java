:hotel: [Return to Home Page](https://github.com/geophydog/geophydog.github.io)

***

```
ArrayList is a class.
```

***

### Declaration of ArrayList class instance.
```java
ArrayList<Type> arr = new ArrayList<Type>();
```

***

### method of ArrayList class

- void add(i): Add a element to arr.
```java
arr.add(Type element);
```

- void get(i): Get the element of index "i".
```java
arr.get(i);
```

- void remove(element): Remove a element.
```java
arr.remove(element);
```

- int size(): Get the size of arr.
```java
int n = arr.size();
```

***

### Example
```java
import  java.util.*;
public class TestArrayList {
    public static void main(String[] args) {
        ArrayList<String> str = new ArrayList<String>();

        str.add("Hello");
        str.add("World");
        str.add("There!");
        str.add("Hi!");

        System.out.println("Before removing:");
        for ( int i = 0; i < str.size(); i ++ ) {
            System.out.println(str.get(i));
        }

        str.remove("Hi!");
        System.out.println("After removing!");

       for ( int i = 0; i < str.size(); i ++ ) {
            System.out.println(str.get(i));
       }
    }
}
```
