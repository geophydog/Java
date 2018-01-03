:hotel:[Return to Home Page](https://github.com/geophydog/geophydog.github.io/blob/master/README.md)
***
## Java Class and sub-class inherit super-class
***
### :one: Class form
```java
public class ClassName {
  Attributes;
  ...
  Methods;
  ...
}
```
#### Example,
```java
public class Animal {
  String color; // Attribute 1
  String name; // Attribute 2
  public void eat() { // Method 1
    System.out.println("Animal will eat something!");
  }
  
  public void breathe() { // Method 2
    System.out.println("Animal can breathe!");
  }
}
```

***

###  :two: Class inherit form
```java
class SubClass extends SuperClass {
  Attribute;
  ...
  Method;
  ...
}
```
```
sub-class will inherit all attributes and methods of super-class.
```
