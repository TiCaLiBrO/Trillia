# Parentheses

## Prelude

### Precedence

In Trillia, every line of code is read from left to right.
The only exception to this is parentheses, which are still internally read from left to right, but happen *first* in the ordering of your line of code.

So in a line of code:

    3 + 7 - 6

We start with `3 + 7`, giving us `10`.
Then the expression becomes `10 - 6`, giving us `4` as the result.

If instead we have an expression:

    3 + (7 - 6)

We instead start with `7 - 6`, which gives a result of `1`.
This is still read from left to right, but the bracket acts as a way to *break apart* one statement into two, with the expression inside the brackets being resolved first.
Then, `3 + 1` returns a result of `4`.

### Why Left to Right Precedence?

Trillia has a very strict left-to-right precedence.
It may not be immediately obvious as to why, but there are many benefits to a system like this.

In Trillia, the left-sided value is always the one that gets changed, and the right-sided value is the one that does the change.
For example, in the expression `5 - 3`, it's the same as saying *start with 5, then take 3 away from it*.

This is a universal property of the language itself, and it means that you and the compiler can always easily understand what gets changed and what causes the change.
This is a property that very few languages have, and not having this property can be very dangerous.
Without this universal property, it can be difficult to tell what, if anything at all, gets altered, which can cause mysterious behavior that is difficult to fix.

## The Task

You are given this expression:

    13 - 11 + 9 - 7 + 5 - 3 + 1
    



> [!IMPORTANT]
> Invisible within Sepal.
>
>     code
>
> [next lesson]





