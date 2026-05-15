After the IR has been tagged for optimizations, it can be scanned for ownership.

Before this phase can be fully explained, a brief overview of handedness is required.

Trillia, unlike most languages, has extremely strict rules when it comes to functions that return a value versus functions that mutate a value.
In Trillia, it's always clear whether an operation is mutating or returning, and that is critical for this phase.
In Trillia, we call this property *handedness*.
Handedness is the difference between returning a value `x = factorial(y)`, versus mutating a value `(y)factorial`.
Every single line of code that can be written in Trillia only has one object that gets mutated.

Only because of strict handedness is it at all possible for this phase in compilation to exist.
The compiler can detect exactly which objects get mutated, and which ones are merely part of expressions.
Knowing where each object gets written to and where each object gets read from is very important, as with this knowledge, you have enough for an automatic borrow checker.

In other languages, garbage handling is either automatic at runtime or manual during development.
Languages that have a garbage collector are slower to run because garbage collectors add extra overhead.
Languages that require programmers to manually handle garbage are cognitively complex and full of boilerplate, slowing down development time.
Trillia does neither of these things; instead, opting for a third alternative: compile-time ownership graphing.

What are the benefits and drawbacks of compile-time ownership?
Starting with the cons: it slows down compilation time.
The first pro is that it saves development time by eliminating manual garbage handling and boilerplate.
The second pro is that it makes your code easier to read because it is simpler without boilerplate.
The third pro is that your code runs as fast as if you manually inserted garbage handling.

Each read and write of an object is marked, making it very clear for the next compiler phase to utilize.


