# Conditions

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/conditions












//////////////////////////////////////////////////////////////////////////////////

- `if`
- `then`
- `else`
- `unless`
- `True`
- `False`
- `None`
- `Undefined`
- `and`
- `or`
- `not`
- `is`
- `=` for questions
- `!=`
- `>`
- `<`
- `>=`
- `<=`
- `__/@__`
- `__//@__`
- `__\\@__`
- Boolean logic
- Booleanite logic



# 5. Control Structures
The six comparative operators are: `=`, `!=`, `>`, `<`, `>=`, and `<=`.
These operators return `True` or `False`, and are used to interact most often with conditions.

## 5.1 Branch Control Structures
Trillia supports `if`, `else`, `unless`, and `then`.
The `if` and `unless` keywords are followed by a condition and subordinate code.

    if   x = 6
    then print(x)
This is an example of an *if block*. The subordinate code `print(x)` is only ever executed if the entire condition is `True`.
In Trillia, it is encouraged that you use the `unless` keyword for negative if statements.

    unless weather = rainy
    then   go_outside()
The `unless` keyword only activates subordinate code if the expression is `False`.
`unless` is desirable because it makes complicated negations of conditions easier to manage. If there is a mix of positive and negative conditions, the `if` keyword is encouraged for clarity.

The `then` keyword can be used to make subordinate code on the same line, or simply for clarity.

    if is_even(x) then x + 1
or

    if is_even(x)
    then
        x + 1

If you want to execute code only in the case that the condition fails, you can use the `else` keyword.

    if health <= 0
    then
        print("You Died")
    else
        print("You survived a critical hit")

The words can be shifted around and used in different ways as needed to make your code clearer.

    if health <= 0
    then
        print("You Died")
    else
        print("You survived a critical hit")

    if health <= 0 then print("You Died") else print("You survived a critical hit")

A note about optimization:
To provide simplicity and consistency, Trillia does not support `switch`, `case`, `default` keywords for control structures.
Instead, if-else chains are optimized such that if questions are asked using `=`, then the chained `if`s are compiled into a `switch` block for greater speed.

    if   x = 1
    then do some code
    if   x = 2
    then do some code
    if   x = 3
    then do some code
    ...

The Ternary Operator
Trillia has a very simple ternary operator.

    if a then b else c
That's it, and it's no different in syntax than regular if-else statements. You can use the `unless` keyword too.












Traditional Boolean logic versus Trillian Boolean logic
// Talk about proper safety using True as the only way to build a lemma, and False as the default.

