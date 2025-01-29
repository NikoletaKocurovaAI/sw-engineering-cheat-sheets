# Object oriented design

## Organizing the catalog of design patterns

**Purpose criterion**
- creational purpose: Creational patterns concern the process of object creation. 
- structural purpose: Structural patterns deal with the composition of classes or objects.
- behavioral purpose: Behavioral patterns characterize the ways in which classes or objects interact and distribute 
responsibility.

**Scope criterion**

Specifies whether the pattern applies primarily to classes or to objects.

class pattern
- deals with relationships between classes and their subclasses
- these relationships are established through inheritance, so they are static—fixed at compile-time.
- creational defers some part of object creation to subclasses
- structural uses inheritance to compose classes
- behavioral uses inheritance to describe algorithms and flow of control

object pattern
- deal with object relationships, which can be changed at run-time and are more dynamic
- creational defers object creation to another object
- structural describes ways to assemble objects
- behavioral describes how a group of objects cooperate to perform a task that no single object can carry out alone


![design_patterns.png](images%2F6a_design_patterns.png)

Source:
Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). Design Patterns: Elements of Reusable Object-Oriented Software. Addison-Wesley.