:hotel: [Return to Java Home Page](https://github.com/geophydog/Java)

***

```
Firstly, compile the public class when refrencing the public class by another class in the same package, and then compile another class.
```

***

## __example__
### 1. public class referenced by another class in the same package.
```java
package cn.geophydog.polymorphism;

public class Animal {
    String name;

    public void voice() {
        System.out.println("General animal's voice!");
    }
}

class Cat extends Animal {
    @Override
    public void voice() {
        System.out.println("Cat's voice!");
    }
}

class Dog extends Animal {
    @Override
    public void voice() {
        System.out.println("Dog's voidce!");
    }
}

class Pig extends Animal {
    @Override
    public void voice() {
        System.out.println("Pig's voice!");
    }
}

class Test {
    public void animalVoice( Animal a) {
        a.voice();
    }
}
```

### another class referecing the public class
```java
package cn.geophydog.polymorphism;

public class TestAnimal {
    public static void main( String[] args ) {

        Test t = new Test();
        Pig p = new Pig();
        Dog d = new Dog();
        Cat c = new Cat();

        t.animalVoice(p);
        t.animalVoice(d);
        t.animalVoice(c);
    }
}
```
