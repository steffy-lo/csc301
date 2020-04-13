# Unit Testing

* Testing one single \(and small\) unit of code \(e.g., method, functionality, etc.\)
* Runs fast \(usually less than 1s\)
* Large number of tests \(one single method may have multiple unit tests\)
* Tests different ways a unit of code may be used

Types of Unit Tests

Black Box

* Tests are designed and executed without knowledge of implementation details
* Practical black box testing involves testing against the method signature and method documentation

White Box

* Tests are designed and executed with knoweledge of implementation details
* Why isn't black box enough?
  * BB doesn't guarantee 100% code coverage
  * Certain parameter combinations may have unique combinations
  * Not everything is documented

Design for Ease of QA

* SOLID principles
* OO best practices are usually meant to promot modifiability but they also have an equally profound impact on testability
  * For example, the single responsibility principle \(much easier to test; large parameter lists also cause a combinatorial explosion in complexity\) and encapsulation \(limiting exposure of internatl state limits how the outside world can break the code\)

Test Doubles \(Mocks\)

* Test Double is a general name for various patterns
  * **Dummy** - No implementation, passed around, but not used - usually just to fill parameter requirements
  * **Fake** - Has a working implementation, but not suitable for production use \(e.g., in-memory test database\)
  * **Stub** - Somewhat similar to Fake, but only behaviour needed for testing is implemented \(i.e., has no logic, returns pre-programmed answer for testing\)
  * **Spy** - A stub that also records information about how it was called
  * **Mock** - A spy that expects to be used a certain way, can be used to test object interactions
    * E.g., can throw an exception if it receives a call it doesn't expect and is checked during verification to ensure it got all the calls it was expecting

Test Driven Development \(TDD\)

* Writing test before writing code
* Write code to pass the test and repeat the cycle to add more tests or refactor earlier code
* Pros:
  * Helps with **automating tests** and **enables CI/CD**
  * Helps focus the development efforts \(on the important features\)
  * Thinking about **how the code will be used**, before writing it, leads to **better design**
  * Tests serve as **clear specifications**
  * **Increase confidence** in functionality and **minimizes technical debt** increase
* Cons:
  * Not always cost-effective: testing infrastructure/scaffolding can be very expensive and/or complex to build
  * Too many unit tests, not enough system tests
  * Writing tests takes more time initially



