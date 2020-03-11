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
OOA: Object-oriented analysis is a method of analysis that examines requirements from the perspective of the classes and objects found in the vocabulary of the problem domain

OOD: Object–Oriented Design (OOD) involves implementation of the conceptual model produced during object-oriented analysis. In OOD, concepts in the analysis model, which are technology−independent, are mapped onto implementing classes, constraints are identified and interfaces are designed, resulting in a model for the solution domain, i.e., a detailed description of how the system is to be built on concrete technologies.

SOLID principles of Object Oriented Design:
SRP – Single Responsibility Principle.
OCP – Open/Closed Principle.
LSP – Liskov Substitution Principle.
ISP – Interface Segregation Principle.
DIP – Dependency Inversion Principle

Object Orineted Programming: is a programming paradigm based upon objects (having both data and methods) that aims to incorporate the advantages of modularity and reusability. Objects, which are usually instances of classes, are used to interact with one another to design applications and computer programs

Grady Booch has defined object–oriented programming as “a method of implementation in which programs are organized as cooperative collections of objects, each of which represents an instance of some class, and whose classes are all members of a hierarchy of classes united via inheritance relationships”

Object oriented software design steps:
1. Find relevent objects
2. Factor(include) them into classes at right granularity
3. Define class interfaces and inheritence hierarchies. Then establish key relationship among them.

Key requirements for good design:
1. Reusable (Reuse of objects, functions, designs)
2. Flexible (Design should be specific to the problem and generic enough to future problems and requirments)(easy manintenance)



