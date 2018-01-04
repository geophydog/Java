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
  public ClassName(type1 para1, type2 para2, type3 para3,...) { // formal parameters
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
    this.name = anname; // instance parameter1 assignment
    this.color = ancolor; // // instance parameter2 assignment
    this.id = anid; // // instance parameter3 assignment
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
  
  public void eat() {
    System.out.println("Animal will eat something!");
  }
}

class Monkey extends Animal {
  int age;
  public Monkey(String anname, String ancolor, int anid) {
    super(anname, ancolor, anid); // super function should exist in the first line.
    this.age = 10;
  }
}
```

***

### :five: Method of sub-class overriding that of super-class
```java
// super-class
public class Father {
  public void run() {
    System.out.println("Just try to run it!");
  }
}

// sub-class
class Child extends Father {
  public void run() {
    System.out.println("Run it again!");
  }
}
```

- output
```
Run it again!
```
```
"run" method in class "Child" overrides that in class "Father".
```
