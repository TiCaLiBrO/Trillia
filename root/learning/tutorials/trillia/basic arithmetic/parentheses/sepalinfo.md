# Parentheses

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[basic arithmetic](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/sepalinfo.md)/parentheses

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

    print(100 - 50 - 20 - 10)

Copy the code above and insert brackets to make the result become `80` instead of `20`.

Run the code when ready.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execute
>     when  source_code     = print(100 - ((50 - 20) - 10)) # Fix this later, such that it is more lenient on whitespace.
>     and   standard_output = 80
>     catch lesson_passed   = True
>
> next lesson [\basic arithmetic/negative numbers](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/negative%20numbers/sepalinfo.md)




<!--

## 4.2 Order of operations
In Trillia, the order of operations is always brackets first, left to right. There is no higher precedence given to multiplication over addition, or certain functions over others.

`2 + 5 * 10` returns 70. If you want it to be done in proper order, just move things around or use brackets.

`5 * 10 + 2`   returns 52

`2 + (5 * 10)` returns 52

If there are multiple disconnected brackets in a larger expression, if your version of Trillia is implemented with automatic parallel threading, it should understand that it can solve for both pairs of parentheses at the same time.

Think of an expression like this: `(1 + 2) + (3 + 4)`

In such a case, `(1 + 2) + (3 + 4)` resolves to `(3) + (7)` in a single step, because both sides were solved simultaneously.

If there are more brackets to solve in parallel than there are cores on your computer, the left-most brackets are resolved first to preserve left-to-right execution.


