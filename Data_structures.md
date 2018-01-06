:hotel:[Return to Home Page](https://github.com/geophydog/geophydog.github.io/blob/master/README.md)

***

- Enumeration
- BitSet
- Vector
- Stack
- Dictionary
- Hashtable
- Properties

***

### :one: Enumeration
- boolean hasMoreElements()
    - to test whether containing more lements.
- nextElement()
    - to get a next element
    
    _Example_
    ```java
    import java.util.Enumeration;
    import java.util.Vector;
    public class ClassName {
      public static void main(String[] args) {
        Enumeration<String> days;
        Vector<String> daysName = new Vector<String>();
        
        daysName.add("Sunday"); // Add string element to "daysName".
        daysName.add("Monday");
        daysName.add("Tuesday");
        daysName.add("Wednesday");
        daysName.add("Thursday");
        daysName.add("Friday");
        daysName.add("Saturday");
        
        days = daysName.elements(); // Assign elements of "daysName" to days.
        
        while ( days.hasMoreElements() ) { // Test whether has at least one element.
          System.out.println(days.nextElement()); // Print element(s) of "days" one by one in right order.
        }
      }
    }
    ```
