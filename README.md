
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


<b>Dependency Inversion Principle</b>:
-
