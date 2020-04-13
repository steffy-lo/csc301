# Design Patterns

### Adapter Design Pattern

The adapter design pattern allows, for instance, to:

* Convert the interface of a class into another interface clients expect
* Create a new class, **Adapter**, to convert the interactions of the available class, **Adaptee**, to the required class, Target, without changing it
* Clients will not know if they work with a Target directly or through an Adapter with a class without the Target interface
* Cleans up code, helps decouple modules and separate concerns

Example: [https://github.com/TechPrimers/structural-design-pattern-example/tree/master/src/main/java/com/techprimers/designpatterns/adapter](https://github.com/TechPrimers/structural-design-pattern-example/tree/master/src/main/java/com/techprimers/designpatterns/adapter)

Designing Interfaces 

Why is it good to design your application in terms of interfaces?

* To focus on the domain problem and ignore implementation details
* Can use different implementations
  * Gradual improvements
  * Support different integrations
* Easier to test \(we can inject test doubles for testing purposes\)

**Construction vs. Use**

Construction: Creating an instance of some concrete class

Use: Calling methods on an object

* Generally good design \(especially for large systems\)
* Most of the application is written in terms of interfaces
* Introduce objects whose sole responsibility is constructing other objects
* Make the boundary between construction and use clear
  * Ensure it is easy to swap in different implementations

### Factory Method

1. The application invokes the constructors of different implementations of T
2. Application depends on factory objects to construct instances of type T. Factory objects invoke the constructors of different implementations of T
3. Application depends only on the factory interface. Any factory implementation can be used to construct instances of type T

![](.gitbook/assets/image%20%285%29.png)

* Delegate responsibility
  * Don't construct objects of type T yourself
  * Ask a factory object to do it for you
* Make the factory an interface
  * With a single method that returns T
  * Different implementations of the factory interface return different implementations of T

### Dependency Injection

* A class should be avoiding instantiating its own dependencies
* Instead, let someone else inject these dependencies
  * By passing them as constructor arguments, or using setter methods
  * Dependencies are declared using interfaces not concrete implementations
* Who is that "someone else" that inject dependencies?
  * Could be another method
  * Dependency Injection container \(e.g., Spring, Guice\)

### Telescoping Constructor

* A constructor with many arguments \(possible of the same type\)
* Error prone
  * Correctness might depend on argument order
  * Developers might get it wrong \(or waste time double-checking\)
  * Compiler can't save you
* Harder to test
  * More arguments --&gt; Even more combinations to test
* Ugly code

### Builder Pattern

* Break construction into two separate tasks
  * Collecting arguments
  * Creating the instance
* Solve the telescopic constructor problem by collecting the arguments one at a time
* Improves code quality
* Can implement quality checks during construction

### Singleton

* Ensures that only one instance of a certain class can be created



