# SOLID

## S (SRP) - Single Responsibility Principle
- Class should have only one reason to change.
  - A function or class should be responsible for only one task (or responsibiliity).
    - Gather together the things that change for the same reason and separate things that change for different reasons.
       - Keep **ONLY** related stuff together.

```Write classes so that your code "fits in your head".```

## O (OCP) - Open Close Principle
- Class should be open for extension but closed for modification.
  - You should be able to chnage what a class does, without changing its code.
    - **Try** to imagine the future changes you will most likely need to make and designe the class to allow these changes without needing to modify the class itself.

```Design your classes so that you can change their behavior without changing their code. TAKE IT EASY!```

## L (LSP) - Liskov Substitution Principle
- Subtypes (class that extends a base class) must be substitutable for their base types.
  - You should be able to substitute a class for a sub-class without breaking your app or needing to change any code.
    - In other words, a class should behave in a way that most users expect: it should behave like its parent class or interface intended.
#### More: **(First three baked into PHP syntax)**
- One: you cannot change the type of a protected property.
- Two: you can't narrow the type hint of an argument. Like, if the parent class uses the object type-hint, you can't make this narrower in your subclass by requiring something more specific, like a DateTime object.
- Three, which is both similar and opposite to the previous rule, you can't widen the return type. If the parent class says a method returns a DateTime object, you can't change this in the subclass to suddenly return something wider, like any object.
- Four, you should follow your parent class's - or interface's - rules around whether or not you should throw an exception under certain conditions.

```If a class extends a base class or implements an interface, make your class behave like it is supposed to.```

## I (ISP) - Interface Segregation Principle
- Clients should not be forced to depend on interfaces (also abstract aka public methods) that they do not use.
  - Don't force clients of your class to depend on interfaces - in other words, methods - that they do not need.
    - Build small, focused classes instead of big, giant classes.

```If a class has a large interface - so a lot of methods - and you often inject the class and only use some of these methods - consider splitting your class into smaller pieces.```

## D (DIP) - Dependency Inversion Principle
- High level modules should not depend on low level modules, both should depend on abstractions - for example, interfaces.
  - Classes should depend on interfaces instead of concrete classes.

- Abstractions should not depend on details. Details - meaning concrete implementations - should depend on abstractions.
  - Those interfaces should be designed by the class that uses them, not by the classes that will implement them.

```Prefer type-hinting interfaces and allow each interface to be designed for the "high level" class that will use it, instead of for the low-level class that will implement it.```
