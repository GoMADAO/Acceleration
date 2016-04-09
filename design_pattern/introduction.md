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
