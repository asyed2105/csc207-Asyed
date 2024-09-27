Week 2 Lecture Notes
====================
+ From last week's lectures:
1. What is the structure of a Java class? (declaration, variables, ...)
2. What are the possible accessibility modifiers and primitive types in Java?
3. What is the difference between the equals method and the == operator?
4. What will var1 == var2 evaluate to if var1 and var2 have reference types? have
primitive types? Why?
5. All Java classes are subclasses of "Object". We call Java classes "reference
types" as opposed to "primitive types". What is the difference between the two?
6. How is a constructor different from a method? Include information about what
each does as well as the difference in syntax.
+ More Java
7. What does it tell other programers if you include a getter but not a setter for
a variable?
8. Where do the toString and equals methods come from if we didn't write them
ourselves?
9. Can you have more than one constructor?
10. What is a getter method? When do we need one?
11. What is a setter method? When do we need one?
12. What is the benefit of making everything as close to private as possible?
13. Question 3 describes "encapsulation". Why do we consider private variables with
public methods to be better encapsulated than public variables and private methods?
14. Consider the variables x and y, where
Person x = new Person(...);
Student y = new Student(...);
Why can we use y in the place of a Person object, but not use x in the place of a
Student?
15. What does "override" and "shadow" mean?
16. What is "the compiler"? What sorts of issues prevent IntelliJ from compiling?
17. "The compiler does not keep track of object types, only variable types." What
does that mean?
18. Give one of the reasons why it is useful to have all classes inherit from the
Object class.
19. How does the memory model diagram show two aliases for the same object?
20. Consider variable z where
Person z = new Student(...);
If we call z.moogah() but moogah is not a Person method, where will the compiler
check for the moogah method? (In the Object class? In the Student class? etc.)
21. Why do we bother to write Javadoc instead of relying completely on inline
comments?
22. How does inheritance work in Java?
23. Consider the variable stu1, where
Person stu1 = new Student();
If we call stu1.getStudentNumber, do we expect the compiler to be able to find the
"getStudentNumber" method? Why or why not
