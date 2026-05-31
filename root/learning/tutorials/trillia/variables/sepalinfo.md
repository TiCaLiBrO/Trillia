# Chapter 2: Variables

In this chapter, you'll learn about variables.
Variables are the primary way to store data, so they're very important.

## Lesson 1
[/undefined variables](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/undefined%20variables/sepalinfo.md)

You will learn: What variables are and what their default values are.

## Lesson 2
[/variable assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/variable%20assignment/sepalinfo.md)

You will learn: How to assign a value to a variable.

Variables are assigned using a variable name, followed by the `=` sign, then the value you are assigning to it

    x = 10


## Literature 1
[/naming](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/naming/sepalinfo.md)

You will read: The rules for naming variables and some conventions.

## Lesson 3
[/string assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/string%20assignment/sepalinfo.md)

You will learn: How to assign strings of text to variables.

## Lesson 4
[/variables assigning other variables](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/variables%20assigning%20other%20variables/sepalinfo.md)

You will learn: How to use variables to assign values to other variables.

## Lesson 5
[/reassignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/reassignment/sepalinfo.md)

You will learn: How to reassign variables once they have already been given a value.

## Lesson 6
[/snapshot assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/snapshot%20assignment/sepalinfo.md)

You will learn: How assignments are only reflective of the moment that they happen.

## Lesson 7
[/chain assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/chain%20assignment/sepalinfo.md)

You will learn: The precedence and propagation of the assignment operator, as well as its futility when right-handed.

Like many other languages, chaining assignments is unintuitive and not recommended, but a demonstration can give insight.

    a = b = c
This is ***bad code***. This demonstration is just to show how it works.
The `=` sign works identically to all other operations. It takes the right-handed operand as a copy, and alters the left-handed operand, then pipelines the left-handed operand forward.
In the statement `a = b = c`, `a = b` happens first, reading the value of `b` and changing `a`'s value. The expression is now simplified. `a = c` is next. We first put `b`'s value into `a`, and now we're putting `c`'s value into `a`. We do this until the line is finished. Notice that we only ever change `a` and read from `b` and `c`. In Trillia, we call `a` an *Ordinal* component, and `b` and `c` are *Cardinal* components.

> [!CAUTION]
> Beyond this point is currently under rework.
> Use this resource at your own risk.

## Lesson 8
[/ordinal swapping](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/ordinal%20swapping/sepalinfo.md)

You will learn: How to swap two variables' values

Notice, though, that we were only able to change one object per line. If you wish to do multiple assignments on a single line, you should either use `,` or `;` to separate assignments.

    a = b; b = c
This is actually two lines of code just made to look like a single line. It is `a = b`, and then a second line `b = c`. This one has order. We put `b`'s value into `a` first, and then we put `c`'s value into `b`. We read from `b` in the first line, then write to `b` in the second.

## Trial 1
[/ordinal trial](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/ordinal%20trial/sepalinfo.md)

You will test: Your ability to swap variables.

// a more advanced three-variable or four-variable swap.

<!-- The previous lesson is a warm-up before the trial. Have the Trial be an extended version with 4 variables? -->

## Lesson 9
[/cardinal assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/cardinal%20assignment/sepalinfo.md)
(a, b, = b, a)

You will learn: How to swap two variables Cardinally.

To swap two variables, you can use `,` commas on both sides of the `=` sign. This cardinalizes the right-hand operands such that they are snapshots of the objects before the operation is performed. This means that it's able to be parallelized.

    a, b = b, a
This swaps the value of a and b.

The number of arguments on the left side must be the same as the number of arguments on the right side. If they differ, you will get a Pruning Error, telling you that you have wasteful code (something being assigned to nothing, or something not being assigned anything).

## Lesson 10
[/cardinal assignment 1]

You will learn: The basics of Cardinal assignment.

Cardinal assignment, making your code simpler to write, easier to read, and faster to execute.

    a, b = b, c
This puts the value of `b` into `a`, and the value of `c` into `b` at the same time, strictly after b and c are copied to temporary objects. The items to the right of the `=` sign are copies of the original values.

(a, b, c = d, d, d)
(a, b, c = d, e, f)

## Trial 2
[/cardinal trial](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/cardinal%20trial/sepalinfo.md)

You will test: Your ability to refactor code so that it is easier to read and faster to execute.


// (a, b, c = d, d, d)

// (a, b, c = d, e, f)



















