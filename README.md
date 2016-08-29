# CoreJavaTheories
Nite : Giving example of bank and finance is the best
http://tutorials.jenkov.com/java-concurrency/java-memory-model.html

1-3 yrs http://www.instanceofjava.com/ java exp

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

Heap vs Stack (Imp)
-----------------
http://www.journaldev.com/4098/java-heap-space-vs-stack-memory

Heap = larger size, created for object, slower memory
Stack= smaller size, created for function, variables, objects references are ketp, faster memory
Each thread gets a stack.

STACK=localvariable+functions
HEAP=objects+ static+ instance variable

Variables defined inside methods, constructors or blocks are called local variables

Instance variables are given default values, ie null if it's an object reference, 0 if it's an int.

Local variables don't get default values, and therefore need to be explicitly initialized (and the compiler usually complains/warns if you fail to do this).



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
Serialization in java is a mechanism of writing the state of an (object into a byte stream). It is mainly used in Hibernate, RMI, JPA, EJB, JMS technologies. The reverse operation of serialization is called deserialization(byte stream to object). so that objects(file,classes) can be transfered to wire. The String class and all the wrapper classes implements java.io.Serializable interface by default.To travel object's state on the network (known as marshaling)

If a serializable class does not explicitly declare a serialVersionUID, then the serialization runtime will calculate a default serialVersionUID value for that class based on various aspects of the class, as described in the Java(TM) Object Serialization Specification. However, it is strongly recommended that all serializable classes explicitly declare serialVersionUID values, since the default serialVersionUID computation is highly sensitive to class details that may vary depending on compiler implementations, and can thus result in unexpected InvalidClassExceptions during deserialization. Therefore, to guarantee a consistent serialVersionUID value across different java compiler implementations, a serializable class must declare an explicit serialVersionUID value. It is also strongly advised that explicit serialVersionUID declarations use the private modifier where possible, since such declarations apply only to the immediately declaring class--serialVersionUID fields are not useful as inherited members.

private static final long serialVersionUID = -7467864054698729101L;


COLLECTION FRAMEWORK
--------------------
I=interface
1.Collection(I)  //to represent group of objects to identify as single entity collection inerface is used
1.1  List (I)// allowed duplicate, insertion order maintained of objects 
    1.1.1 ArrayList(C) 
    1.1.2 LinkedList(C)
    1.1.3 Vector
    1.1.4 Stack 
    
1.2  Set(I) //not allowed duplicate, order of insertion not required
    1.2.1 HashSet -> LinkedHashSet
    1.2.2 SortedSet(I)->NavigableSet(I)->TreeSet(C)
1.3  Queue //before processing if wants collection then queue (eg: SMS queue before sending)
    1.3.1 PriorityQueue
    1.3.1 BlockingQueue
    
2.Map(I)  //if want to store group of objects as not single entity but KEY,VALUE pair Map is used
2.1 Hasmap  -> LinkedHashMap
2.2 SortedMap ->NavigableMap(I) -> TreeMap
2.3 HashTable (Dictionary is parent for HashTable)

THREADS/SYNCHRONIZATION
-----------------------
Thread safety in java is the process to make our program safe to use in multithreaded environment, there are different ways through which we can make our program thread safe.

-Synchronization is the easiest and most widely used tool for thread safety in java.
-Use of Atomic Wrapper classes from java.util.concurrent.atomic package. For example AtomicInteger
-Use of locks from java.util.concurrent.locks package.
-Using thread safe collection classes, check this post for usage of ConcurrentHashMap for thread safety.
-Using volatile keyword with variables to make every thread read the data from memory, not read from thread cache.
