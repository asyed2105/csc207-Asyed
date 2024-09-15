## Numeric TYpes
int --> integer <br>
float --> Float <br>
double --> Double <br>
char --> Char <br>
boolean --> Boolean <br>

### Declaring variables
-  Java is a statically typed language. In a statically typed language the association between a variable and the type of object the variable can refer to is determined when the variable is declared. <br>
- Once the declaration is made it is an ERROR for a variable to refer to an object of any other type.
    - Whenever we introduce a new variable we NEED TO DECLARE ITS DATA TYPE
    - In the code below see:
          - Specifically we are saying that fahr and cel are going to reference objects that are of type Double. <br>
          - The variable in will reference a Scanner object. <br>
          - This means that if we were to try an assignment like fahr = "xyz" the compiler would generate an error because "xyz" is a string and fahr is supposed to be a double.
```
public class TempConv {
    public static void main(String[] args) {
        Double fahr;
        Double cel;
        Scanner in;
    }
```

## Imports
In JAVA you can use any class that is availble WITHOUT hgaving to import the class in with 2 important conditions
1. The javac and java commands must know that the class exists. <br>
2. You must use the full name of the class <br>

### Import Statements
- We can think of import statement in Java like python which is:
```
from module import XXXX
```
- HOWEVER, BEHIND THE SCENES THE TWO STATEMENTS HAVE DIFFERENT MEANINGS FROM PYTHON TO JAVA
- 1. The first important difference to understand is that the class naming system in Java is very hierarchical. <BR>
       - The full name of the Scanner class is really java.util.Scanner.
       - You can think of this name as having two parts: The first part java.util is called the package and the last part is the class
  2. Java class loader’s responsibility to load classes into memory, not the import statement’s.
 
  3. - THE IMPORTMENT STATEMENT tells complier that we are getting shortened version of the class's name
         -  In this example we are going to use the class java.util.Scanner but we can refer to it as just Scanner. <br>
         - We could use the java.util.Scanner class without any problem and without any import statement, provided that we always referred to it by its full name.
      
## Strings
- Strings in JAVA and PYTHON are quite similar
- in java strings are IMMUTABLE ( canNOT be changed without recreation)
- strings do NOT support indexing or slicing operations
    - THAT DOES NOT MEAN YOU CANNOT INDEX AND SLICE JUST SYTAX IS DIFFERENT THAN USUAL

| Python  | Java | Description |
| ------------- | ------------- | ------------- |
| str[3]  | str.charAt(3) | Return character in 3rd position |
| str[2:4]  | str.substring(2,4)  | Return substring from 2nd up to but not including 4th  |
| len(str)  | str.length() | Return the length of the string |
| str.find('x')  | str.indexOf('x')  | Find the first occurrence of x  |
| str.split()  | str.split('\s')  | Split the string on whitespace into a list/array of strings |
| sre.split(',') | str.split(',') | Split the string at ',' into a list/array of strings |
| str + str  | str + str or str.concat(str) | Concatenate two strings together  |
| str.strip()  | str.trim() | Remove any whitespace at the beginning or end  |

## List
- Lets go through this with an example
- Python code first:
```
def main():
    count = [0]*10
    data = open('test.dat')

    for line in data:
        count[int(line)] = count[int(line)] + 1

    idx = 0
    for num in count:
        print(idx, " occured ", num, " times.")
        idx += 1

main()
```
- To do java version of this, we need to go over new shit:
    1. the java equivalent of a list is called: **ArrayList**
    2. Different types of loops. There are 3
       - **while (condition) {code}**
           - The code will be repeatedly executed until the condition becomes false.
       - **for (initialization statement; condition; loop statement) {code}**
           - The code will be repeatedly executed until the condition becomes false.
       - ** for (Type variable : collection) { code }**
           - The code will be executed once for each element in the collection.
           - Each execution, variable will be assigned to the next element of collection.
           -  Known as the “for-each” loop. This form is useful for iterating over members of a collection, similar to how you might use for a in array in Python.

```
import java.util.Scanner;
import java.util.ArrayList;
import java.io.File;
import java.io.IOException;

public class Histo {

    public static void main(String[] args) {
        Scanner data = null;
        ArrayList<Integer> count;
        Integer idx;

        try {
                data = new Scanner(new File("test.dat"));
        }
        catch ( IOException e) {
            System.out.println("Unable to open data file");
            e.printStackTrace();
            System.exit(0);
        }

        count = new ArrayList<Integer>(10);
        for (Integer i = 0; i < 10; i++) {
            count.add(i,0);
        }

        while(data.hasNextInt()) {
            idx = data.nextInt();
            count.set(idx,count.get(idx)+1);
        }

        idx = 0;
        for(Integer i : count) {
            System.out.println(idx + " occured " + i + " times.");
            idx++;
        }
    }
}
```
- Lets see wtf is going on :)
-  Declared the variables
-  In this example we are declaring a **Scanner variable** called data, an **integer** called idx and an** ArrayList ** called count.
    -  However, there is a new twist to the ArrayList declaration.
    -  Unlike Python where lists can contain just about anything, in Java we can let to the _**compiler know what kind of objects our array list is going to contain**_ .
        - the syntax we use to declare what kind of object the list will contain is the <Type> syntax.
              - TECHNICALLY, you don't have to declare the array type list, the complier will just send you warning message
<br>
- Lines 13—20 are** required to open the file**.
    - Why so many lines to open a file in Java?
    - The additional code mainly comes from the fact that Java forces you to reckon with the possibility that the file you want to open is not going to be there. If you attempt to open a file that is not there you will get an error.
<br>
- On line 22 we create our ArrayList and give it an initial size of 10.
    - Strictly speaking, it is not necessary to give the ArrayList any size.
    - It will grow or shrink dynamically as needed, just like a list in Python. On line 23 we start the first of three loops.
-  The for loop on lines 23–25 serves the same purpose as the Python statement count = [0]*10, that is it initializes the first 10 positions in the ArrayList to hold the value 0.
<br>
-FOR LOOP syntax:
    - (Integer i = 0; i < 10; i++) is **exactly equivalent** for i in range(10)
        - first declare datatype of integer and set its value
        - then set for loop condition
        - i++ ensures value in loop increases after each iteration ( i_++ is same as i=i+1 )
<br>
- Line 29 illustrates another important difference between Python and Java.
    - Notice that in Java we can not write count[idx] = count[idx] + 1.
    - This is because in **Java there is no overloading** of operators.
    -  Everything except the most basic math and logical operations is done using methods.
       - So, to set the value of an ArrayList element we use the set method.
       -  The first parameter of set **indicates the index or position in the ArrayList we are going to change**.
       -  The next parameter is the value we want to set.
            - Notice that, once again, we cannot use the indexing square bracket operator to retrieve a value from the list, but we must use the get method.


### Dictionary
- Java is an extra piece of shit and calls dictionaries **maps**
- There are 2 different implementations of maps:
      1. TreeMap
          - uses a balanced binary trees
  importing the TreeMap class
  ```
  import java.util.TreeMap;
  ```
  Creating a TreeMap

  ```
  TreeMap<KeyType, ValueType> map = new TreeMap<>();
  ```
  Adding elements
  ```
  map.put(KeyType key, ValueType value);
  ```
  Accessing elements
  ```
  ValueType value = map.get(KeyType key);
  ```
  Removing elements
```
map.remove(KeyType key);
```
Iterating over elements
```
for (Map.Entry<KeyType, ValueType> entry : map.entrySet()) {
    KeyType key = entry.getKey();
    ValueType value = entry.getValue();
    System.out.println(key + ": " + value);
}
```
Checking if a key/value exists
```
boolean hasKey = map.containsKey(KeyType key);
boolean hasValue = map.containsValue(ValueType value);
```
      2. HashMap
          - uses a hash table
