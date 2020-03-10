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
Model is the application object. View is the model's screen representation. COntroller defines teh way the UI reacts to the user input. MVC decouples Models and Views by establishing a Subscribe/Notify protocol between them. Whenever the model's data changes, the model(Notifier/publisher) notifies the views(subscribers). Each view s get aopportunity to update itself. 

General Problem: decouple objects 
