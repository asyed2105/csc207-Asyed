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
