# OO design theory

Two commonly used approaches in Object-Oriented Analysis and Design (OOAD):

**1. Noun-Verb Analysis (Class-Responsibility Mapping)**
- Write a problem statement describing the system.
- Identify nouns → These often become classes.
- Identify verbs → These often become methods.

**2. CRC (Class-Responsibility-Collaboration) Approach**
- Focus on what each class is responsible for (Responsibility).
- Determine which other classes it interacts with (Collaboration).
- Use CRC Cards (physical or digital) to represent Class, Responsibility, and Collaboration.

![5_oo_design.png](images%2F5_oo_design.png)

## Key Concepts in OO Design

- **Encapsulation (Hiding data)**
  - The practice of hiding an object's internal state and requiring all interactions to be performed through well-defined 
  methods.
- **Abstraction (Hiding Implementation details), Data abstraction**
- **Inheritance (Code Reusability & Hierarchies), Composition, Parametrized Types, Delegation**
  - **Class inheritance** means that a class inherits from another class (a parent/base class). It provides a way to 
  share implementation details between classes. Subclasses are tightly coupled to their parent.
  - **Interface inheritance** (or subtyping) enables polymorphism, to use one object in place of another if it 
  follows the expected interface (contract).
- **Polymorphism (One Interface, Many Implementations), Dynamic binding**

## Reusability

- **Inheritance:** Share common logic across multiple classes.
- **Composition:** Combine multiple objects to create reusable components.
- **Modular design:** Separate concerns into different classes/modules. Separation of Concerns (SoC) Principle.
- **Design patterns:** Apply reusable solutions 

## Performance 
OO design focuses on how efficiently a system runs.

- **Memory efficiency:** Avoid unnecessary object creation.
- **Lazy loading:** Load resources only when needed.
- **Avoid deep inheritance:** Excessive subclassing can slow down method resolution.

**Use caching:** Store frequently used values to reduce recomputation.

**Algorithm optimization:** Use efficient data structures (dict, set instead of list where applicable).

## Dependency

- **Tightly coupled** dependencies make code hard to modify and test.
- **Loosely coupled** dependencies improve maintainability and flexibility. **Dependency Injection (DI)** can reduce 
coupling.

# My OO design check list

Principles from algorithms project
SOLUTION
Don't forget to check:
- Correct Naming conventions
- Optimization of Time and Space Complexity
- if Refactoring required (existing not only new code)
- if Documentation and/or Decision-Comment required

TESTS
Three Laws of TDD (Test-Driven Development)
- ✔ Does the test exist before the implementation? (Ensures proper TDD flow)
- ✔ Does the test fail before implementation? (Prevents false positives)
- ✔ Does the implementation only include the necessary code to pass the test? (Avoids over-engineering)

Don't forget to check:
- if Unit Test fixtures required
- if SetUp and TearDown required
- if Parametrized tests required
- if Context Managers required
- if Documentation/Decision-Comment required
- if Build Operate Check pattern applied
- if Test Double or Mock Object Pattern required
- if When-Given-Then convention and/or Template Method required
- if Behavior Driven Development (extends TDD) required
- F.I.R.S.T principles violation

-encapsulation (hiding data)
-abstraction (Hiding Implementation details)
-Inheritance(Code Reusability & Hierarchies):
extending other classes, making it easy to define families 
define families of objects with 
identical interfaces (usually by inheriting from an abstract class) is also important. Why? Because polymorphism depends on it.
-Polymorphism (One Interface, Many Implementations)

dependency, loosely coupled, DI

performance
- Avoid unnecessary object creation
- lazy loading
- avoid deep inheritance
- caching

reusability
- inheritance
- composition
- modular design - classes/modules
- design pattens

Objects, data, procedures (methods/behaviors)
getters, setters

DAO
Data Access Object
access to data source (interact with databases, aPIs).

Data structures, DTOs
especially when communicating with
databases or parsing messages from sockets

🔹 DAO = Works with the database
Primarily used for databases (to interact with a database) or APIs (to interact with external services).
🔹 DTO = Just holds data for transfer
typically when transferring data across layers or systems (e.g., databases to application layer, or 
through network communication like sockets).

regular class vs dao, dto ?

inheritance vs. composition
Composition - get all the functionality you need just by assembling existing components
Inheritance and object composition work together

Inheritance - Reuse by subclassing is often referred to as white- box reuse
Object composition requires that the objects being composed have well-defined interfaces. 
This style of reuse is called 
black- box reuse,

“inheritance breaks encapsulation”.
inherit only from abstract classes, since they usually provide little or no implementation
In composition, Because objects are accessed solely through their interfaces, we don’t break encapsulation.

Composition - Any object can be replaced at run-time by another as long as it has the same type.

Composition - because an object’s implementation will be written in terms of object interfaces, there are substantially 
fewer implementation dependencies.

inheritance vs. parametrized types
give us a third way (in addition to class inheritance and object composition) to compose behavior 
in object-oriented systems.

(at run-time) Object composition lets you change the behavior being composed at run-time, but it also requires 
indirection and can be less efficient.
(not at run-time) Inheritance lets you provide default implementations for operations and lets subclasses 
override them. 
(not at run-time) Parameterized types let you change the types that a class can use.

Delegation
a receiving object delegates operations to its delegate
the receiver passes itself to the delegate to let the delegated operation refer to the receiver.

Relationships between objects - aggregation and association (acquaintance, "using" relationship)

Association is a general relationship between objects.
Aggregation is a specific type of association representing a whole-part relationship, but the parts can 
exist independently of the whole.

Object vs. DSA
Procedural code (code using data structures) makes it easy to add
new functions without changing the existing data structures. OO
code, on the other hand, makes it easy to add new classes without
changing existing functions.

Objects expose behavior and hide data. This makes it easy to add new
kinds of objects without changing existing behaviors. It also makes it hard
to add new behaviors to existing objects. 

Data structures expose data and have no significant behavior. 

the Law of Demeter that says a
module should not know about the innards of the objects it manipulates.

abstract classes and interfaces are closely related concepts, but they have distinct roles in 
Object-Oriented Programming (OOP). 

Abstract class (also INTERFACE?)
To define a common interface for its subclasses.
The operations that an abstract class declares but doesn’t implement are called abstract operations. 
Classes that aren’t abstract are called concrete classes.
Creational patterns ensure that your system is written in terms of interfaces, not implementations.

INTERFACE
Every operation declared by an object specifies the operation’s name, the objects it takes as parameters, 
and the operation’s return value. This is known as the operation’s signature. The set of all signatures 
defined by an object’s operations is called the interface to the object. 

Dynamic binding and polymorphism
The run-time association of a request to an object and one of its operations.
Dynamic binding lets you substitute objects that have identical interfaces for each other at run-time. This 
substitutability is known as polymorphism.
