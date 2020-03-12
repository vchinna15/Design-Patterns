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

The main difference between object-oriented analysis and other forms of analysis is that by the object-oriented approach we organize requirements around objects, which integrate both behaviors (processes) and states (data) modeled after real world objects that the system interacts with. In other or traditional analysis methodologies(Structured Analysis and Design Methodology), the two aspects: processes and data are considered separately. For example, data may be modeled by ER diagrams, and behaviors by flow charts or structure charts.

OOD: Object–Oriented Design (OOD) involves implementation of the conceptual model produced during object-oriented analysis. In OOD, concepts in the analysis model, which are technology−independent, are mapped onto implementing classes, constraints are identified and interfaces are designed, resulting in a model for the solution domain, i.e., a detailed description of how the system is to be built on concrete technologies.

SOLID principles of Object Oriented Design:
1. SRP – Single Responsibility Principle.
2. OCP – Open/Closed Principle.
3. LSP – Liskov Substitution Principle.
4. ISP – Interface Segregation Principle.
5. DIP – Dependency Inversion Principle

Object Orineted Programming: is a programming paradigm based upon objects (having both data and methods) that aims to incorporate the advantages of modularity and reusability. Objects, which are usually instances of classes, are used to interact with one another to design applications and computer programs

Grady Booch has defined object–oriented programming as “a method of implementation in which programs are organized as cooperative collections of objects, each of which represents an instance of some class, and whose classes are all members of a hierarchy of classes united via inheritance relationships”

Principles of OOP:
1. Abstraction
2. Encapsulation
3. Inheritence
4. Polymorphism


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
1. Creational (deals with the process of object creation)
2. Structural (deals with composition of classes or objects)
3. Behavioural (deals with how classes or objects interact each other and distribue responsibility)

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
6. Design for change

three broad categories of softtware:
1. Application Programs
2. Toolkits
3. Frameworks




