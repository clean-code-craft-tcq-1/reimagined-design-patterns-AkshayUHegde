# Reimagined Design patterns
## **Activity**:

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  
Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries 
say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather 
> think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while 
> drinking coffee.

## **Submission**:

The four design patterns I have chosen to summarise are Decorator, Observer, State and Prototype design pattern. I have 
selected one creational, one structural and two behavioral design patterns.

### 1. Prototype:
- _**Use case**_: Prototyping basically provides a cloning mechanism to clone an object when the inner workings of the 
  class interface of the object cannot be known. This is generally achieved by a cloning method which returns a new 
  cloned object. An example where prototyping is used is when third party libraries are used in the project and the 
  objects need to be cloned but the underlying abstract class implementation is not known. It is akin to cloning a 
  helper robot provided the core robot mechanism is provided by a third party.
- _**Working**_: Prototype design pattern is implemented through extensions of abstract classes (whose inner code may
  or may not be available to us) and then implementing a cloning function which essentially has the interfaces of the
  abstract class with some additional implementations. It adheres to the classic definition of a prototype and is 
  similar to class inheritance except for the cloning method.
- _**Pros and cons**_: An advantage of prototyping is that it eliminates the need for the source code of a third party 
  class implementation. A disadvantage is that circular references are more difficult to identify and debug.
### 2. Decorator:
- _**Use case**_: Decorator design pattern is mostly used when the core logic of a particular software implementation 
  remains the same while variants perform different pre or postprocessing on the data. A relevant example is
  our past assignment to generate different notifications for high or low temperatures in the battery management farm.
  Decorators give the flexibility to add new notification systems easily and the freedom to choose the combination of 
  notifications to the client.
- _**Working**_: Decorator works on the principle of recursive composition. What that means is that it works on the
principle of enhancing a class interface through composition rather than inheritance while retaining the interface 
definition. This follows the Abstraction -> Accumulation flow of design patterns.
- _**Pros and Cons**_: Advantage is that it allows different compositions of required behavior at the client while retaining
class hierarchy simplicity. Disadvantage is that decorators cannot break the flow of the request since they are
recursive.
### 3. Observer:
- _**Use case**_: Observer design pattern is used when the change in state of one object needs a functions to be called in
  another object with minimal overhead. A relevant example is from my workplace wherein, if there is a change in input
  file content, it should trigger a different build mechanism as opposed to when the input files are unchanged. Observers
  are useful when you want to add multiple handlers for a state change of an object which only activate when there is a
  state change.
- _**Working**_: It works on a publisher, subscriber mechanism where the publisher maintains a list of subscribers with an
  interface to add and remove subscribers. The change of state of the publisher results in a call to notify all
  subscribers in the subscribers list - this means that each subscriber should have a uniform interface for notification
  from the publisher.
- _**Pros and cons**_: An advantage is that it allows addition of subscribers during run-time and isn't static. A 
  disadvantage is that the order in which the subscribers are notified cannot be controlled.
### 4. State:
- _**Use case**_: State design pattern is used when the problem you are trying to solve takes the form of a Finite State
  Machine(FSM) with a large number of states. It is implemented in lieu of an if-else chain or a switch case block for 
  easier extensibility and minimum code duplication. A suitable example is a video game where a huge number of state
  machine are applied to each component of the game, including enemy AI, player character, environment characteristics,
  etc.
- _**Working**_: State design pattern works by abstraction of each state of the FSM into a separate object. All of the 
  different objects are implementations of a common state interface and are set as the current state through pseudo
  accumulation on any state transition. The new state object is handed over during context change.
- _**Pros and cons**_: An advantage is that it allows addition of new state without any changes to the original state
  classes. A disadvantage is that it is overkill in case of small state machines which can be handled by if else or
  switch statements.
