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


PassBy Value vs PassByRefernce
------------------------------
if primitive variables are passed eg: ind i=10; add(i);  is passed by value

if object is passed then reference is passed eg: 
classTest{int i}
Test t=new Test(), t.i=10; add(t);


Instance and Class
------------------
if a object is created then its a instance of a class eg: Bank nbl=new Bank(); nbl is an instance

Instance vs Static variable
---------------------------
static variable is in class level. it can be accessed with class name it self. do not need instance for class 
to be created to use it.

instance variable if not declared any variable without static it can be accesed through instance

eg: class Bank{
static int name;
}
Bank.name="nbl"; ok can be done

Access Modifiers
----------------
Variables or methods have access modifiers

1.default : int a; //can be access to classes and sub-classes in same packages.
2.public : public int a; //can be access to all classes  in all packages
3.private : private int a; //can't access from out side the class
4.protected: //can be access to classes and sub-classes in in all packages.

Final (variable, method, class)
----------------------------
varaible can' be changed the value
method can't be overriden
class can't be extended

INTERFACE (represent actions, but class represent noun)
--------
-represent common actions,method in between classes
to implement classes own way.

-implemented class for interface should write all its methods
- public static final is default for interface and methods signature are only there, can't implement them in interface

eg: class aeroplane implements fly{
    @override // the interface fly
    void dofly(){
     //aeroplane flying
    }
    }

    class bird implements fly{
    @override // the interface fly
    void dofly(){
     //bird flying
    }
    }
    
    interface fly{//as both aeroplane and bird can fly
        void dofly();
     }

eg: Runnable, 

-multiple iterfaces can be implemeted by class


ABSTRACT CLASS
--------------
- its instance can't be created, means new keyword can't used to instantiated abstract class
- public static final are allowed
- in a class only one class can be extended at a time. 
- can have abstract or general methods defined. if abstract method it cant be implemented just defined like interfaces
but for normal methods it can be implemented.

ANONYMOUS CLASS
---------------
class which are inner class can that is used just for once, then u don't have to provide name for the class.
there is ; in the end fo class structure is anonymous class


class ProgrammerInterview  {
 public void read() {
  System.out.println("Programmer Interview!");
 }
}
class Website {
/*  This creates an anonymous inner class: */
ProgrammerInterview pInstance = new ProgrammerInterview() {
  public void read() {
   System.out.println("anonymous ProgrammerInterview");
  }
 };
}
Well, the main thing is that it is quicker to just create an anonymous inner class rather than create a new separate class.Anonymous inner classes are especially useful when you only need to override a small amount of functionality (like just one method) in a superclass, and don’t want to deal with the overhead of creating an entire class for something so simple.

WRAPPER CLASSES  (immutable like String)
--------------
class representing the primitive date type.

if you want to use no,float using srting use WRAPPER classes.
named Camel case to primitive data type.

eg: Integer for int, Float for float

Integer ten=new Integer(10);
ten++; //valid statement

Variable Arguments passsing
--------------------------
3 dots used
public int sum(int... numbers)

SERIALIZATION
-------------
Serialization in java is a mechanism of (writing the state of an object into a byte stream). It is mainly used in Hibernate, RMI, JPA, EJB, JMS technologies. The reverse operation of serialization is called deserialization(byte stream to object). so that objects(file,classes) can be transfered to wire. The String class and all the wrapper classes implements java.io.Serializable interface by default.
