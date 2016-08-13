# CoreJavaTheories
Nite : Giving example of bank and finance is the best


platform independent
-------------------
The .java file is written once in a windows can be compiled 
with JVM for linux, unix, windows any platform to generated its .class
and can be run any where.  for .class it has to be environment specific.



Diff between c++ and Java
--------------------------
-java do not have pointers to memory.
-java to not have structures,unions but class and objects.
-java has JVM to deallocate memories but in c++ u have to do it.
-java does not have multiple inheritance, but support it through interfaces.


is java pure object oriented language?
--------------------------------------
Java is not because it supports Primitive datatype such as int, byte, long... etc, to be used, which are not objects.

There are seven qualities to be satisfied for a programming language to be pure Object Oriented. They are:

1. Encapsulation/Data binding (using private to properties of class to bound the properites,methods to that class only)
Technically, Encapsulation is defining private variables and provide public getter and setter methods to access them. 
Encapsulation is a process of binding or wrapping the data and the codes that operates on the data into a single entity. This keeps the data safe from outside interface and misuse.

2. Inheritance (sharing properties and methods of classes)
3. Polymorphism (same code,method diff behaviour, eg:- saving,current  account, but getMinBal() will give diff output)
4. Abstraction (hiding the complexities showing only the method,interface)
5. All predefined types are objects (int i=0; is not valid but not in java)
6. All operations are performed by sending messages to objects
7. All user defined types are objects.

Polymorphism
-------------
http://www.javahelps.com/2015/02/oop-polymorphism.html
2 types
1. method overloading(compile time), change in  method parameters
2. method overriding(run time), needs inheritence to support, here the parents methods are written in child class with @override annotion for child implementation.


