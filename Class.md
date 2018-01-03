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

### :two: Class with parameters
```java
public class ClassName {
  public ClassName(type1 para1, type2 para2, type3 para3,...) {
    ...
  }
}
```
#### Example,
```java
public class Animal {
  String name;
  String color;
  int id;
  public Animal(String anname, String ancolor, int anid) {
    this.name = anname;
    this.color = ancolor;
    this.id = anid;
  }
  
  public void breathe() {
    System.out.println("Animal can breathe!");
  }
}
```

***

###  :three: Class inherit form
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
#### Example,
```java
// Super-class
public class Father {
  String color;
  int age;
  double height;
  double weight;
  
  public void speak() {
    System.out.println("Father speaks English very well!");
  }
}

// Inherit
class Child extends Father {
  String name;
  String grade;
  public void walk() {
    System.out.println("Aha, this little child can walk!");
  }
}
```

***

###  :four:Sub-class inherit super-class with parameters
