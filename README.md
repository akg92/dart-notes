# dart-notes

## Data Types
* String
* int
* double
All data types are objects unlike java.

## Type inference
* Unlike java type can be infered.
    * Eg var i = 10; int i = 0 not required.

## String 
* Interpolation. Eg: "My name is $name and length is ${name.length}". 
    *  $<var_name> or ${\<expression\>}

## final vs const
* Both are same in functionality but const is set compile time.
* Const should be static if it is a class member.

## Control flow
### If null shortcut
* This can be used for null check.
    * Eg. name ?? "hello"
### Normal if, else, terinary operator, switch-case


## Loops
### For
* Java syntax for(initilization; condition; inc/dec)
### Java while, do-while syntax.

## Functions
### Syntax
* Normal syntax: ret_type function_name(var_type var_name){} 
* Return type is optional.
## Short-hand notation
* =>. only single expression is allowed.last statement is return.
* Eg int area(int length, int breadth) => length*breadth;
### Parameters
* Optional paramters  between[]
    * Eg. int hello(String name, [int age, String from]). here age and from are optional.
* Named parameters between {}
    * int hello(String name, {int age, String from}). here age and from are named.
    * Can call this as hello(name, from: milkiway, age: 10)
* Default value for parameters
    * Assign value in declaration. Eg. int hello(name ="Booo")
### Information
* Functions are object.
* function by default return null, even void

## Exception 
### Hadling
* try-catch --use when you don't know the type 
    * Eg try{ 10/0} catch(e){}
* try-catch for stack
    * catch(e,s) : s is stack trace
* try-on try {10/0} on DivisionByZero {}
* finally {} -- similar to java.
### Custom
* implements Exception 



# OOPS
## Constructor
* Default constructor and prameterized constructors are not allowed together.
    * Use named constructor.
* new is not required to create new object. eg: var student = Student()
* Assignment can be trimmed Student(this.name, this.age);.
    * Automatically assign to object value.
    * Doesn't require body.
* Named constructor
    *  how to declare Student.custom() { this.name = "boo"}
    * Usage : var s = Student.custom();  s.age = 10;


## Getter and Setter
* Each property has default setter and getter. :).  wieredo...
* cutome set
    * void set name(String firstName, String lastName) => this.name = firstName + " " + lastName;
* getter
    * String get name {return "Hello $this.name"}

## Inheritence
* Super class contructor
    * class Dog(String breed, String color): super(color){}
    * incase of named constructor: Dog(String breed, String color): super.custom(color){}

## Interface
* No interface keyword.
* Use class for interface. implements to implement.
* We have to override all the method in the interface.

## Callable class
* implement call()
    * call of object will execute it.


## Functional Prorgamming
* Function is the type for function similar to java.
### Anonymous function declaration/Lambda function declaration.
* same as typescript syntax.
    * Function fun1 = (int first, int second) => first+second;
### Higher order function
*  Return or accept another function.
### Closure
*  Similar to JS


# Classes
### List -- fixed length
    * fixed length List(size) 
    * list[index] to access.
    * list.foreach(Function)
### List -- Growable
    * list = List(); // no size is passed.
    * list.remove(value)
    * list.removeAt(index)
    * list.clear
### Set
    * Set<int> set = Set()
    * Set<int> set = Set.from(["hello"])
### Map
    * Map<String,String> map = Map();
    * map["hello"] = "hi";
    * map["hello"]; // access
    * map.keys : get all keys