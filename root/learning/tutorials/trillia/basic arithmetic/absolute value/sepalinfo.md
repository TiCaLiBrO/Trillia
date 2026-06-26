# Absolute Value

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[basic arithmetic](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/sepalinfo.md)/absolute value

## Prelude

Absolute value can be thought of as the "size" of a number, regardless of its sign.
For example, `-15` is less than `10`, but the absolute value of `-15` is greater than `10` because `15` is more than `10`.

You can get the absolute value of a number by using the `+` operator, prepended to a number.

If you aren't familiar with the term *absolute value*, you can think of it as making a number positive if it wasn't already.

Examples include:
- `+10`
- `+(-30)`
- `+0`

You get the idea.
For negative numbers, you need brackets around the number because the original number already has a sign.
In Trillia, you are not allowed to make monstrosities like `+-+++----+--+--++-5`... well, you can, but you need to use brackets to show the ordering.
The innermost brackets are always resolved first - as with all expressions.

When you use brackets, it solves the expression and then gets the absolute value of the result, like this:

    +(10 - 30)

This results in `+20`.

## The Task

You are given the following code:

    print(10 + 20 - 100)

Change the math so that we add the absolute value of `20 - 100` to `10`.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execute
>     when  source_code     = "print(10 + +(20 - 100))" # change later to be more whitespace-lenient
>     and   standard_output = "90"
>     catch lesson_passed   = True
>
> next lesson [\basic arithmetic/delta](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/delta/sepalinfo.md)


