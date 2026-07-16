# Intermediate Arithmetic





<!--

If you wish to cast the type and/or size of a variable into another type, you can also do so by using a declarative line.

    x natural(2 ** 32)
This is only possible if the value can be perfectly preserved. Floating point, being often inexact, often error.
It is highly recommended that you use the `rational` type to be able to represent values perfectly.

# 3. Types
Different data types are best for different tasks.
Trillia has three numeric types: `natural`, `integer`, and `rational`. All of these are suffixed by the number of bits used to represent them.
For example, natural(X) is most often in the forms `natural`, `natural(2 ** 8)`, `natural(2 ** 16)`, `natural(2 ** 32)`, and `natural(2 ** 64)`.

## 3.1 Numerics

`natural` numbers are what most other languages call `unsigned integer`. The `natural` type is the most basic form of numeric data type.

`integer`s allow negative numbers to be represented.

One thing before we get into decimal point types. As far as Trillia is concerned, *irrational numbers don't exist*. They're formulas and limits, not values.
In the same way that infinity is a limit, not a value, irrational numbers are also limits, not values.

`rational` numbers are actually an array of two numbers, a divisor and a denominator, that exist as a reduced fraction in memory. The size represents the size of both elements in the array.
The rational type is preferred over floating-point or fixed-point, where exact precision is more valuable than speed.

After the `rational` type, `fixed point` is the next most common decimal type. It is the preferred type for handling decimal values quickly, where inexact values are acceptable.

Floating-point numbers are not available in the base language, as they are not deterministic across hardware due to optimizations. They have been moved into a floating-point library.


