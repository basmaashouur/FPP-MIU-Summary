# Contents
- [Java Basics](#Java_Basics)
  * [Iterator](#Iterator)
- [Java OOP Consepts](#Java-OOP-Consepts) 
- [UML](#UML) 
  * [Class Diagram](#Class-Digram)
  * [Object Diagram](#Object-Diagram)
  * [Sequence Diagram](#Sequence-Diagram)
- [Polymorphism](#Polymorphism)
   * [Inheritance](#Inheritance)
- [Functional Programming](#Functional-Programming)
- []()
- []()


# Java Basics
## Loops & Iterator
### Itrate over objects list
# Java OOP Consepts
- **Static Binding:** When type of object is detrmined at compile time, The binding which can be resolved at compile time by compiler is known as static or early binding. Binding of all the static, private and final methods is done at compile-time.
- **Dynamic Binding:** When type of object is detrmined at run time, In Dynamic binding compiler doesn’t decide the method to be called. Overriding is a perfect example of dynamic binding.

# [UML](https://creately.com/blog/diagrams/uml-diagram-types-examples/)
![alt text](https://github.com/basmaashouur/MIU-Courses-Summary/blob/main/UML-Diagram-types.png)
## Techniques
- Propagation and Delegation
## [Class Diagram](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/)
### Class
### Class Attributes
### Class Operations
### Class Relations
![alt text](https://github.com/basmaashouur/MIU-Courses-Summary/blob/main/class_diagram_relations.png)
 - Association
   - 
   -  Multiplicity (Cardinality) ![alt text](https://github.com/basmaashouur/MIU-Courses-Summary/blob/main/multiplicity.png)
      -   is an indication of how many objects may participate in the given relationship or the allowable number of instances of the element.
 - Simple Association
 - Reflexive Association
 - Aggregation
   - enum
 - Composition
   - if removed the class cant exist
 - Inheritance (Generalization)
   - 
 - Realization 
   - Interface
 - Dependency
   - 
  
## [Sequence Diagram](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-sequence-diagram/)

# Polymorphism
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
# [Functional Programming](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html)
## [Streams & Lambda](https://winterbe.com/posts/2014/07/31/java8-stream-tutorial-examples/)

### Stream Source
```java
   // read from list, stream() is inside collection class 
   Stream<T> stream = list.stream();
   
   // Create stream from an array using Arrays.stream()
   Stream<T> streamOfArray = Arrays.stream(arr);
   
   // read from a bunch of object references
   Stream.of("A", "good", "day", "to", "write", "some", "Java");
   
   // from range
   IntStream.range(1, 4);
   
   // infinite stream
   Stream<Integer> infiniteStream = Stream.iterate(0, i -> i + 2);
   infiniteStream.limit(20)


```
### Stream Operations
#### Intermediate operations
```java

   // filter, return Stream<obj[]>
   // used to eliminate elements based on a criteria, params : a non-interfering, stateless predicate
   strings.stream().filter(string -> string.isEmpty())
   
   // filter with if condition to print diffent value in case of each case
   .filter(c -> {
     if(!c.getFirstName().startsWith("D")) {
     System.out.println(c);
     return false;
     }
     else return true; 
     })
			
	
   
   // map, return Stream<obj[]>
   //  used to map each element to its corresponding result
   numbers.stream().map( i -> i*i)
   
   // map with if 
     .map(c-> { if(c.getCompanyCity().startsWith("mo")) 
          c = new Company(c.getCompanyName(), c.getCompanyCity().toUpperCase());
        return c;
        })
   
   // mapToInt, return Stream<Int>
   mapToInt(e -> (int)e.getSalary())
     
   // mapToLong, return Stream<Long>
   mapToLong(e -> (long)e.getSalary())
    
   // mapToDouble, return Stream<Double>
   mapToDouble(e -> (Double)e.getSalary())
   
   // flatMap
   // flatMapToLong
   // flatMapToInt
   // flatMapToDouble
   
   // distinct, return Stream<obj[]>
   // Returns a stream consisting of the distinct elements
   distinct()
   
   //sorted, return Stream<obj[]>
   // used to sort the stream
   sorted();
   sorted(Comparator.comparing(e -> e.getSalary()))
   
   // limit, return Stream<obj[]>
   // used to reduce the size of the stream
   limit(10);
   
   // skip, , return Stream<obj[]>
   skip(n);
   
  // concat, 
  Stream<String> stream1 = list1.stream();
		Stream<String> stream2= list2.stream();
		
		rStream.concat(stream1, stream2) 
				.filter()

```
#### Terminal Operations
```java
  // forEach,
  // used to iterate each element of the stream
  .forEach(System.out::println);
  .forEach(e -> {
	      if (e.getLastName().startsWith("B")) {
	          e.setLastName(e.getLastName().toUpperCase());
	          } 
       System.out.println(e);
	      });
       
       // max, min, count, average 
       // we have to convert the stream first to mapToInt or mapToDouble to be able to use them
       
       // peek
       
       // reduece
       // combines all elements of the stream into a single resul
       reduce(0, (subtotal, element) -> subtotal + element);
       
       // collect
       .collect(Collectors.toList());
       .collect(toSet());
```
### Stream return
```java
   // print
   .forEach(value -> System.out.printf("%d ", value));

   // collect in a list
   // primitive value 
```
