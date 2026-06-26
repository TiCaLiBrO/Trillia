# Chapter 2: Basic Arithmetic

In this chapter, you'll learn how to execute basic arithmetic operations.
Numbers are everywhere in programming, and arithmetic is the primary way that you, as a programmer, will be able to work with numbers and values.

## Lesson 1

[/addition](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/addition/sepalinfo.md)

You will learn: How to add two numbers.

## Lesson 2

[/subtraction](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/subtraction/sepalinfo.md)

You will learn: How to subtract one value from another.

## Lesson 3

[/parentheses](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/parentheses/sepalinfo.md)

You will learn: How to change the order of operations via brackets.

## Lesson 4

[/negative numbers](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/negative%20numbers/sepalinfo.md)

You will learn: How negative numbers are represented and how to use them in expressions.

## Lesson 5

[/absolute value](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/absolute%20value/sepalinfo.md)

You will learn: How to get the absolute value of a number or expression.

## Lesson 6

[/delta](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/delta/sepalinfo.md)

You will learn: How to take the absolute difference between two numbers.

## Trial 1

[basic arithmetic trial](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/basic%20arithmetic%20trial/sepalinfo.md)

You will test: Your ability to use the basic arithmetic operators properly, and apply precedence to them.

<!--

INTERMEDIATE ARITHMETIC
15
// multiplication
// division --- example: 10 / 2 = 5. Don't jump into decimal numbers just yet
// decimal numbers --- 5 / 2 = 2.5
// repeating decimal numbers --- 1 / 3 = 0.(3)
// rounding division
// floor division
// ceiling division
// rounded numbers
// floored numbers
// ceiling numbers
// percents
// factorial
// ratios
// remainder division
// remainder numbers
//// how to do mean average manually ((a + b + c) / 3)
//// how to do copy_sign manually. A = 15 and B = -20... (A * (B / +(B)))

ADVANCED ARITHMETIC
11
// exponentiation
// radication
// rounded radication
// floored radication
// ceiling radication
// remainder radication
// logarithmitization
// rounded logarithmitization
// floored logarithmitization
// ceiling logarithmitization
// remainder logarithmitization
//// how to do geometric mean manually ((a * b * c) // 3)

above: 32 chapters

// Everything in this chapter uses the rational type. Other types will be used in other chapters.
// note: no incrementation operator - because + 1 is clearer. The math library has an increment function.
// note: no decrementation operator - because - 1 is clearer. The math library has a decrement function.

// also talk about ordinand and cardinand.




## 4.3 Arithmetic Operator Symbols
For Arithmetic, Trillia has seven binary operations. You do not have to import a math library to access `pow()`, `sqrt()`, or `log()`; these operations are built into the language as symbols.

`*` Multiplication

`/` Division


`**` Exponentiation (Powers)

`//` Radication (Roots)

`\\` Logarithmatization (Logarithms)

The symbols chosen for roots and powers are the same as the symbols for multiplication and division. The symbol for logarithms is just a mirroring of the symbol for roots.
With a system like this, you don't have to remember individual symbols; you just need to remember rules.
The logic is extendable. You could imagine tetration being written as ***, and its root and log equivalent to be written as /// and \\\ respectively.
Such operations aren't supported by Trillia due to memory restraints on most computers. Even something as simple as 5 *** 10 would blow the stack on most computers.

The notation of binary operators is:
`base` then `operation` then `modicand`. A `return_value` is the result.
So in the expression `1 + 2`, `1` is the `base`, `2` is the `modicand`, `+` is the `operation`, and `3` is the `return` value.
There is no need to remember dividend, subtrahend, augend, or other operation-specific words.

Addition is commutative.

    2 + 3 returns 5
    3 + 2 returns 5

Subtraction will return a positive value if the base is greater than the modicand, and a negative return value if the base is less than the modicand.

    8 - 7 returns  1
    7 - 8 returns -1

Multiplication is commutative.

    5 * 7 returns 35
    7 * 5 returns 35

Division always returns a `rational` type if the result is a non-integer value and the base is not strictly typed.

    integer a = 2
    integer b = 3
    a / b
This expression would error because `2 / 3` gives a non-integer return value.
To avoid this, there are different types of division that can always return integer values.

To round your division up, down, or nearest, use `/^`, `/_`, and `/~` respectively.

    integer a = 2
    integer b = 3
    a = a /  b     # This errors because a is an integer and a / b returns a rational.
    a = a /^ b     # a = 1
    a = a /_ b     # a = 0
    a = a /~ b     # a = 1. In the case of 0.5, it rounds up.

There are also two more forms of division, `/%` and `/@`.
The `/%` is modulo division. It divides and then returns the remainder instead of giving a fraction.

    a /% b     # This would return 1

The `/@` can be literally read as *"divides at"* or *"is divisible by"*. Instead of returning a number, it always returns `True` or `False`.

    my_variable = a /@ b
For this expression, `my_variable` would be `False`.
The `/@` operator makes the common `a % b == 0` or `a % b != 0` expressions - that are often seen in other languages - shorter, and more readable.

    if a /@ b then ...

Exponents are non-commutative. The modicand is always the "little number" that you see in "x squared" or "x cubed".

    2 ** 3 = 8
    3 ** 2 = 9
This can be read as *"two to the power of three is eight"*.

Roots are written in the same way, where the exponent is the modicand.
This can seem slightly confusing at first because common notation puts the exponent on the left for roots, but in Trillia, the modicand is always the exponent.

    100 // 2 = 10
    25  // 2 = 5
This can be read as *"twenty-five of the root of two is five"*
Also, notice that with this notation, there is much more freedom than `sqrt()` and `cbrt()` because you are not limited. You can choose any exponent that you want, not just 2 or 3.

Roots also come with variant operations: `//_`, `//^`, `//~`, `//%`, and `//@`.
The `//_`, `//^` and `//~` operators round the result down, up, and nearest, respectively.

The `//%` operator returns the remainder of a root.

    10 //% 2 = 1
because `9 // 2 = 3` exactly, and `10` is 1 more than that.
Some more examples to get the hang of it:

    27 //% 2 = 2
    16 //% 2 = 0
    99 //% 2 = 8

The `//@` operator is basically like an *`is_square()`* or *`is_cube()`* function that returns `True` if the base is a power of the modicand.

    100 //@ 2 = True
    70  //@ 9 = False

Logarithms are the same as roots, except the return value and the modicand are swapped.

    100 \\ 10 = 2
    25  \\ 5  = 2

To get natural logarithms, you can use the built-in `E` constant as the modicand

    10 \\ E = 2.30258509299

The same variant operators exist for logarithms as do exist for division and roots. `\\^`, `\\_`, `\\~`, `\\%`, `\\@`.
The `\\^`, `\\_`, `\\~` operators round as expected.

    17 \\@ 12 = False
    10 \\%  3 = 1

Positive and Negative:
As a prefix, `+` makes what it affects always positive. It is an absolute value unary operator.

    +12
    g = -50
    h = +g # variable h is now 50.

As a prefix, the `-` sign always flips the sign from positive to negative, or negative to positive.

    g = -50
    h = -g # variable h is now 50.

For literals, you can only have a single `+` or `-` sign as a prefix. `--4` is not allowed because it can be reduced to `4`, or `+4` for clarity.
For variables, no sign, `+`, `-`, and `+-` are all allowed.

  g  = -50

  g is -50

 -g is  50

 +g is  50
 
+(-g) is -50

  i  =  20
  
  i is  20
  
 -i is -20

 +i is  20

+(-i) is -20

For variables, no sign before them means that you're just taking the value of the variable.
A `+` sign means you're taking the absolute value of the variable. This ensures you will get positive value.
A `-` sign means you're flipping the sign of the value of the variable. This ensures you will always get the opposite signage of the variable.
The `+-` means you're doing `+`, which makes the value of the variable positive, and then `-`, which flips the sign. This ensures you will always get negative value.
Trillia always reads signs from left to right. Order of operations is notated through left-to-right order and parentheses.
Under the hood, `+-` is just a single bitwise operation to set the sign bit, even though it's read by humans as two separate operations.







## 4.6 Relative Assignment Lines
In Trillia, for any line of code that starts with a variable and does not assign or reassign that variable, the variable is relatively assigned.

    a + 7 * 2
This takes `a`, adds `7` to it, then doubles it. That's the new value of `a`. If there are multiple variables on a line, such as in `a * b`, then only the left-most variable is reassigned.














(30~ lessons thus far. We might break arithmetic into three chapters: Beginner Arithmetic (`+`,`-`). Intermediate Arithmetic(`*`,`/`), Advanced Arithmetic(`**`,`//`,`\\`))

