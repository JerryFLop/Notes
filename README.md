
SOLID Software Design Principles Notes
---------------------------------------------------------------------
- Code Fragility : is the tendency of the software to break in many places everytime it changes.
- Code Rigidity : is when the software is difficult to change, even in simple ways. Changes causes a cascade of subsequent changes in dependenet modules.
- Technical Debt : is the cost of prioritizing fast delivery over quality of code for long periods of time.
----------------------------------------------------------------------
5 software design Principles to help keep technical debt under control
-----------------------------------------------------------------------
<b>Single Responsibility Principle</b>: Every function, class or module should have one and only one reason to change.
Coupling: The level of interdependency between various software components

- <b>Open Closed Principle</b>: Classes,functions, and Modules should be closed for modification, but open for extension. this means its closed new features should modify existing source code and when its open for extension. It should be extendable to make it behave in new ways by creating new code.

- inheritance and design patterns are a good way to add features without modifying existing code.
OCP also applies to packages.

- <b>Liskov Substitution Principle</b>: Any object of a type must be substitutable by objects of a derived typed without altering the correctness ofthat program.
  Make sure that a derived type can substitute its base type completely.
  Empty methods,type checking and hardened preconditions are signs that you are violating the LSP.

- Interface Segregation Principle: Clients should not be forced to depend on methods that they do not use.
  It reinforces other Principles like LSP and SRP.
- The word Interfaces are not just java interface.
- Pay attention to large interfaces and take action.
               
                                               Benefits in using ISP          
- Lean interface minimize dependencies on unused members and reduce code coupling.
- Code becomes more cohesive and focused
- It reinforces the use of the SRP and LSP.


<b>Dependency Inversion Principle:</b>
- High level modules should not depend on low level modules; both should depend on abstractions.
- Abstractions should not depend on details.
  - Details should depend upon abstraction.

 <b>Dependency Injection:</b> Allows the creation of dependent objects outside of class and provides those objects to a class.

- <b>Inversion of Control:</b> control of object Creation,config,and lifecycle is passed to a container or framework.
- Spring Bean: used by your application that are managed by the Spring ioC container.
- Classes should depend on abstractions not implementation details.
- The DIP,DI and ioC are the most effective way to eliminate code coupling and keep systems easy to maintain and evolve.

                                                 High Level Modules
- Written to solve real problems and use cases
- More abstract and map to the business domain
- Tells us what the software should do
                                         
                                                 Low level Modules
- Contain implementation details that are required to execute the business policies
- Considered the "plumbing" or "internals" of application
- Tells us how the software should do various tasks.
______________________________________________________________________
 <b> Design Patterns Notes</b>
---------------------------------------------------------------------


- Reusable and named solution to a recurring problem in a context.
  
                                                 OOP building blocks
- Abstraction
- Encapsulation
- Inheritance
- Polymorphism


                                                     Other Principles
- Don't repeat yourself(DRY).
- Encapsulate what changes.
- Favor composition over inheritance.
- Programming to an interface, not an implementation.
                                             
                                                  Pattern  Classification
- Purpose:
  - Creation
  - Behavioral
  - Structural
- Scope :
  - Class
  - Object
  
                                                  Design Pattern Benefits
- Patterns are about reusability
- Find the appropriate design
- Communication and documentation

                                                       Strategy Pattern
- Changer a Part of a system independently of all other parts
- Swap out behavior at run-time
- its mix of Encapsulation, favoring composition over inheritance, Open-close principle and Programming to interfaces.
  
                                                          Singleton
  - One instance providing a global point of access
  
                                                         Factory Method
- Allows subclasses decide which class to instantiate
 
                                                          Abstract Factory
- Creates hierarchies or families of related object

                                                             Builder
- Separate the construction of an object from its representation


________________________________________________________________________________________________________________________________
__________________________________________________________________________________________________________________________________
Chapter 11 Risky Behavior
----------------------------------------------------------------------------------------
- A method can throw an exception when something goes wrong at runtime.
- An exception is always an object of type exception.
- The compiler does not enforce handling of exceptions that are of type RuntimeException. They do not need to be declared or wrapped in a try/catch block.
- To throw an exception in a method, the "throw" keyword is used, followed by a new exception object.
- Methods that might throw a checked exception (exceptions other than RuntimeException) must declare it in their method signature using the "throws" keyword.
_____________________________________________________________________________________________
Chapter 13a - b Exception
-----------------------------------
- An exception is an unexpected event that occurs at runtime due to an error.
- Exceptions can be handled using the try/catch construct. When an exception is caught, it can be accessed using the stack trace and the `getMessage()` method, which provides the error message without the stack trace.
- The `finally` block is used to execute code that should always run, regardless of whether an exception is thrown or caught.
- Try with resources is a feature that allows you to automatically close resources without explicitly using the `finally` block. It requires the resource to implement the `Closable` or `AutoClosable` interfaces.
- If a method contains code that may throw an exception, it must either catch that exception using try/catch or rethrow it using the `throws` keyword in the method signature.
- The `throws` keyword is used to declare the type of exception that may be thrown by a method.


