# MVC


- M application obj
- V Screen presentation
- C user interface reacts


MVC decouples M and V by using sub/pub (notification/event) method. View reflects the state of model, which is significantly different from the idea of typical DB systems. When Model is changed, model notifies view to change. Then view access value changes in model.


In general, one object change affects any other objects to reflect but the changed objects does not have to know the detail of those others. The general design pattern is called **Observer** design pattern. 


Another about MVC is it uses the idea of composite design pattern. But I dont understand.


### Two criteria for classification

**Purpose** : what a pattern does [creational/structural/behavioural]
-  creational - the process of object creation
-  structual - the composition of objects
-  behavioral - the ways objects interact and distribute 

**Scope** : specifies whether the pattern applies primarily to classes or to objects
- Class patterns - relationship class and subclass [at compile-time]
- Object patterns - object relationship [at run-time]

Creational class patterns defer some part of object creation to subclasses, while Creational object patterns defer it to another object.


### Class versus Interface Inheritance
An object's class defines how the object is implemented. The class defines the object's internal state and the implementation of its operations. In contrast, an object's type only refers to its interface—the set of requests to which it can respond. An object can have many types, and objects of different classes can have the same type.

### Inheritance versus Composition
The two most common techniques for reusing functionality in object-oriented systems are class inheritance and object composition. As we've explained, class inheritance lets you define the implementation of one class in terms of another's. Reuse by subclassing is often referred to as white-box reuse. The term "white-box" refers to visibility: With inheritance, the internals of parent classes are often visible to subclasses.


Object composition is an alternative to class inheritance(containing object reference). Here, new functionality is obtained by assembling or composing objects to get more complex functionality. Object composition requires that the objects being composed have well-defined interfaces. This style of reuse is called black-box reuse, because no internal details of objects are visible. Objects appear only as "black boxes."

- Disadvantage of inheritance
the implementation of its parent class that any change in the parent's implementation will force the subclass to change
===> use abstract class they usually provide little or no implementation.

- 











# Creational Pattern

Two recurring themes in these pattern. 1. encapsulate knowledge about which concrete calsses the system uses. 2. hide how instance of these classes are created and put together.

- Problems with simple or standard object creation
Maze example: Hard-codes maze layout. 

- Difference ways to **remove explicit reference** to concrete classes

**Factory Method**
CreateMaze calls Virtual functions instead of constructor to create wall,rooms,doors

**Abstract Factory Method**
CreateMaze is passed an obejct as a parameter to create rooms,walls,doors to create difference class 

**Builder**
CreateMaze is passed object that create a new maze in its entirety using operations for adding rooms,doors,walls

**Prototype**
CreateMaze is parameterized by varirous prototypical room,door,walls,


