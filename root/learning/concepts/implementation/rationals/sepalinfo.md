# Rationals

The implementation of rational objects is very simple and mathematically honest.

A rational consists of two parts: A divisor and a denominator.

They form a list if unbounded, or an array if bounded.
This is because if unbounded, the divisor and denominator are allowed to change size independently of one another, and will do so eagerly.
If given a fixed size, both values have a maximum bound, and both of them are identically sized in memory, making it ideal to put them in an array for faster access.

A rational is always in the form `[X, Y]` where `X` and `Y` are integers.

## Absolute Value

When you put a rational value through absolute value operations, the form `[X, Y]` gets converted into `[+X, Y]`.
`Y` is always positive, and so no sign flipping is needed beyond `X`.

## Negative

When a rational type has its sign flipped, `[X, Y]` has the sign of `X` flipped.
`[+X, Y]` becomes `[-X, Y]`, and if starting with `[-X, Y]`, it becomes `[+X, Y]`.

## Addition

If using the rational type, with addition, subtraction, flip sign, absolute, and delta only, on integer values, you will never produce a non-integer value.

`[X, Y]` + `[A, B]` happens like this:

Step 1: Multiply the left side by B and A by Y at the same time.
This is done via a cardinal multiplication: `X, Y, A * B, B, Y`.
You *could* do  `X, Y, A, B * B, B, Y, Y` instead, but B is not needed, so, as an optimization for higher-quality Trillia compilers, the tricardinal form is correct.
This step is T(n \\ 2), scaling with input size because integer multiplication has logarithmic time.
This step is T(1) pardoned complexity.

Step 2: Add `A` to `X`.
This step is T(n \\ 2) because integer addition is logarithmic time.
This step is T(1) pardoned complexity.

Step 3: Reduce the fraction of `[X, Y]` if possible.
A GCD operation is used, and both `X` and `Y` are divided by the resulting value.
This step is also logarithmic T(n \\ 2) because GCD and integer division are both logarithmic.
This step is T(1) pardoned complexity.

This means that the entire operation is T(n \\ 2) logarithmic time, scaling as input sizes grow.
It should be noted that in traditional notation, multiplication, addition, and division are often considered constant time, but in reality, that is a lie.
This has T(1) pardoned complexity with 3 pardons.





## Subtraction

## Delta


##





## Rational to Integer and Rational to Natural addition












