:hotel: [Return to Home Page](https://github.com/geophydog/geophydog.github.io)

***

### :one: Decription of ArrayList.
```
ArrayList is a class.
```

***

### :two: Declaration of ArrayList class instance.
```java
ArrayList<Type> arr = new ArrayList<Type>();
```

***

### :three: method of ArrayList class

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

- void set(index, element): Set a new element at index.
```java
arr.set(0, "XXXXX");
```

- boolean contain(element): whether "arr" contains element.
```java
boolean bl = arr.contain("XXXXX")
````

***

### :four: Example
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
       
       System.out.println("Before replacing:");
       str.set(0, "XXXXX");
       System.out.println("After replacing:");
       for ( int i = 0; i < str.size(); i ++ ) {
           System.out.println(str.get(i));
       }
       
       boolean bl = str.contains("XXXXX");
       System.out.println("\"str\" contsains string \"XXXXX\": " + bl);
    }
}
```
_Output_
```
Hi!
After removing!
Hello
World
There!
Before replacing:
After replacing:
XXXXX
World
There!
"str" contsains string "XXXXX": true
```
