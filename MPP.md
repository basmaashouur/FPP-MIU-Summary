# Contents


## Java OOP Consepts
- **Static Binding:** When type of object is detrmined at compile time, The binding which can be resolved at compile time by compiler is known as static or early binding. Binding of all the static, private and final methods is done at compile-time.
- **Dynamic Binding:** When type of object is detrmined at run time, In Dynamic binding compiler doesn’t decide the method to be called. Overriding is a perfect example of dynamic binding.

## UML
![alt text](https://github.com/basmaashouur/MIU-Courses-Summary/blob/main/UML-Diagram-types.png)

## Inheritance
- The idea of inheritance you want to create a new class and there is already a class that includes some of the code that you want, you can derive your new class from the existing class. In doing this, you can reuse the fields and methods of the existing class without having to write (and debug!) them yourself.


```java
   class Student {…}
   class Undergraduate extends Student {…}
   class Graduate extends Student {…}
   
   Student st1,st2, st3;
   Graduate st4;

   st1 = new Student();         // okay
   st2 = new Undergraduate();   // okay
   st3 = new Graduate();        // okay
   st2 = new Graduate();        // okay
   st4 = new Student();         // compilation error

````
