# Code Design

### General

* Use immutable data whenever practical
  * Use pure functions
  * Some recursive algorithms are simpler to implement using mutating loops
    * Such cases are fine as long as the only variables being mutated are variables that do not exist outside of the function's scope
* Minimize function call depth
  * A deep call stack can often be cleanly refactored into a flatter sequence of chained functions

#### ECS

* Code should be structured using [ECS  (Entity Component System)](https://en.wikipedia.org/wiki/Entity_component_system)
* Minimize appending variable names with `Id`
  * By default entity variables should be a scalar id and not a data structure
* If two variables exist in the same namespace where one is an id and one is the record for that id, such as a user id and a user record, they should be named `user` and `userRecord` respectively
* Minimize nested data objects, especially for persistent data

