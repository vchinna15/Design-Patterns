# Design-Patterns
Design pattern is a solution to a common problem that occurs during design. It has 1. Pattern Name, 2. Problem, 3. Solution, 4. Consequences(results and trade-offs of applying the pattern).

Simplest and most common patterns:
1. Absolute Factory 
2. Factory Method
3. Adapter
4. Composite
5. Decorator
6. Observer
7. Strategy
8. Template Method

Design Patterns in Smalltalk MVC:

Model is the application object. View is the model's screen representation. COntroller defines teh way the UI reacts to the user input. Feature 1:MVC decouples Models and Views by establishing a Subscribe/Notify protocol between them. Whenever the model's data changes, the model(Notifier/publisher) notifies the views(subscribers). Each view s get aopportunity to update itself. 

General Problem: decouple objects so that changes to one object can affect other objects without requiring changed object to know other objects. Solution: Observer pattern

Feature 2: the views can be nested. a control panel of buttons can be implemented as a complex view that contains nested button views. Button is represented as View class. Nested Buttons View is represented as CompositeView class, a subclass of View class.

General problem: We want to group objects and treat the group like an individual object. Solution: Composite Pattern 

Feature 3: MVC lets us change the way a View responds to user input(command key in keyboard input or pop-up menu input using mouse) without changing it's visual representation. there is a class hierarchy of controllers. A view uses controller subclass to implement a particular response strategy. Solution: Strategy pattern (straegy means an object that represents an algorithm)

Other patterns used in MVC:
Faactory method to specify teh default controller class for a view
Decorator to add scrolling to a view

Beofre deep diving, let's focus on basics of Object Oriented SOftware:
OOAD(Object Oriented Analysis and Design:
OOA: Object-oriented analysis is a method of analysis that examines requirements from the perspective of the classes and objects found in the vocabulary of the problem domain.

The main difference between object-oriented analysis and other forms of analysis is that by the object-oriented approach we organize requirements around objects, which integrate both behaviors (processes) and states (data) modeled after real world objects that the system interacts with. Outputs will be Use Cases and Object Models. In other or traditional analysis methodologies(Structured Analysis and Design Methodology), the two aspects: processes and data are considered separately. For example, data may be modeled by ER diagrams, and behaviors by flow charts or structure charts.

OOD: Object–Oriented Design (OOD) involves implementation of the conceptual model produced during object-oriented analysis. In OOD, concepts in the analysis model, which are technology−independent, are mapped onto implementing classes, constraints are identified and interfaces are designed, resulting in a model for the solution domain, i.e., a detailed description of how the system is to be built on concrete technologies.

SOLID principles of Object Oriented Design:
1. SRP – Single Responsibility Principle (A class should have one and only one reason to change, meaning that a class should have only one job)
2. OCP – Open/Closed Principle (Objects or entities should be open for extension, but closed for modification)
3. LSP – Liskov Substitution Principle ( every subclass/derived class should be substitutable for their base/parent class)
4. ISP – Interface Segregation Principle (clients shouldn't be forced to depend on methods in an interface that they do not use)
5. DIP – Dependency Inversion Principle (the high level module must not depend on the low level module, but they should depend on abstractions)

Object Orineted Programming: is a programming paradigm based upon objects (having both data and methods) that aims to incorporate the advantages of modularity and reusability. Objects, which are usually instances of classes, are used to interact with one another to design applications and computer programs

Grady Booch has defined object–oriented programming as “a method of implementation in which programs are organized as cooperative collections of objects, each of which represents an instance of some class, and whose classes are all members of a hierarchy of classes united via inheritance relationships”

Principles of OOP:
1. Abstraction (show only relevent details and hide the unnecessary/complex details)
2. Encapsulation (keeping data and methods together)
3. Inheritence (acquire properties and functions from another object)
4. Polymorphism (perform a single operation in multiple way based on the context)


Object oriented software design steps:
1. Find relevent objects
2. Factor(include) them into classes at right granularity
3. Define class interfaces and inheritence hierarchies. Then establish key relationship among them.

Key requirements for good design:
1. Reusable (Reuse of objects, functions, designs)
2. Flexible (Design should be specific to the problem and generic enough to future problems and requirments)(easy manintenance)

Classification of design pattern by scope:
1. Object patterns (deals with object relationships which are dynamic(changed at run-time). the relationship is established by association, composition, aggregation)
2. Class Patterns(deals with class relationships between class and their subclasses established by inheritence. they are static)

Classification of design pattern by purpose:
1. Creational (how objects can be instantiated)
2. Structural (how objects/classes can be combined to deliver a fumctionality)(It enables client code to modify interface, extend behaviour, restrict access and unify access)
3. Behavioural (how objects/classes interact each other and distribue responsibility)

Cra\eational Class patterns defer some part of object creation to subclasses, while Creational Object patternd defer it to another object.

Structural Class Patterns use inheritence to compose classes, while Structurl Object patterns use composition to assemble objects.

Behavioral Class patterns use inheritence to describe algorithm and flow of control. Behavioral Object patterns describe how a group  of objects cooperate to perform a task that no single object can carry out alone.

How design patterns solve design problems?
Design patterns help to 
1. find ppropriate objects
2. determine object granularity
3. specify object interfaces (type - subtype, dynamic binding, polymorphism)
4. secify object implementation ( class inheritence-parentclass-subclass, abstract class, concrete class, Class Inheritence Vs Interface Inheriteince, programming to an interface not an implementation)
5. putting reuse mechanism to work (class inheritence(white box reuse), object composition(black bocx reuse), Favor Object composition over class inheritence, Delegation-is a way of making object composition as powerful for reuse as inheritence)
6. Design for change (if you don't consider change into account, you might need to redesign in future. those changes are class redefinition, class reimplementation, client modificarion and retesting)
  Some common causes of redesign:
    creating an object by specifying class explicitly: specifying class name hen you create oject commits to you a particular implementation. better to use interface. Abstract Factory, Factory Method, Prototype
    Dependence on specific operation: When you specify a particular operation, you commit to one way of satisfying a request. Avoid hard-coded request and wrap the request to an object and pass it to operation. Chain of responsibility, COmmand
  Dependence on hardware/software platform: Limit platform dependence: Abstract Factory, Bridge
  Dependence on Object implementation: CLient that knows how object is created, stored or implemented might need to be changed when Object is changed. Hide these details from client. ABstract Factory, bridge, memento, proxy
  Algorithmic dependencies: ALgorithms are often extended, optimised or replaced during development and reuse. So algorithms that are likely to be changed should be isolted. Builder, Iterator, Strategy, Template Method, Visitor
  Loose coupling over Tight Coupling: Techniques like abtract coupling and layering promote loose coupling in system. Abstract Factory, Bridge, chain of responsibility, command, facade, mediator, observer.
  Extending functionality by subclassing: this approach is not easy. Even new class has a fixed implementation. Instead, we can use Object COmposition and Delegation to provide flexible extension than Inheritence. New functionality can be added by composing existing objects differently. Bridge, chann of responsibility, composite, decorator, observer, stategy
  Inability to alter the class conviniently: One reason is that yuo don't own the class that needs to be alternated. Adaptor, Decorator, Visitor
  
Three broad categories of softtware:(Design patterns can be used for all these)
1. Application Programs(internal reuse, maintainability, extensibility)
2. Toolkits(Libraries)(COde Reuse)
3. Frameworks (Design reuse)

How to select a design pattern:
1. Choose pattens based on the design objective of your application: Reusability, maintainability, extendability
2. to avoid teh causes of redesign in your appliction
3. Consider what you want to change in yuor design without redesign
    Abstract Factory - families of product objects
    Builder - How a composite object gets created
    Factory Method - Subclass of object that is instantiated
    Prototype -class of object that is instantiated
    Singleton - the single instance of a class
    Adapter - Interface to an object
    Bridge - Implementation of an object
    Composite - Structure and composition of an object
    Decorator - Responsibilities of an object without subclassing
    Facade - Interface to a sub-system
    Flyweight - storage costs of objects
    Proxy - how an object is accessed
    Chain of Responsibility - object that can fulfill a request
    Command - when and how a request is fulfilled
    Interpreter - grammar and interpretation of a language
    Iterator - how an aggregate's elements are accessed,traversed
    Mediator - how and which objects interact with each other
    Memento - what private information is stored outside an object, and when
    Observer - number of objects that depend on another object; how the dependent objects stay up to date
    State - states of an object
    Strategy - an algorithm
    Template Method - steps of an algorithm
    Visitor - operations that can be applied to object(s) without changing their class(es)

    

How to use design pattern:
1.  Make sure you understand the classes and objects in the pattern and how they relate to one another
2. choose meaningful names for pattern participants
3. Define the classes, declare teh interfaces, establish their inheritence relationships, and define instance variables(for data and object references).
4. 






