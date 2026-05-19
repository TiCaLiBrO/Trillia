# Snapshot Assignment

## Prelude

In mathematics, if you have a formula, let's say y = (x * x + x), we can give an input value to x and see what happens to y.

In Trillia, like most programming languages, changing `x` after assigning `y` does not *necessarily* change `y`.

Once we assign `y`, it's been given a value, and will not change value unless reassigned.

## The Task

Each of these instructions is one line of code. Follow them carefully:

- Create a variable `A` and assign it the value 10.
- Create a variable `B` and assign it the value `A`.
- Reassign `A` the value 20.
- Using `printn`, print `A`.
- Using `print`, print `B`.

## Explanation

When you reassigned `A`, you did not reassign `B`.
By default, variables are never changed unless deliberately reassigned.
There *is* one way to automatically reassign the dependent variable, but it's in a few chapters.
Feel free to take a look: (foreshadowing -> [\trillia/reactivity])

> [!IMPORTANT]
> Invisible within Sepal.
>
>     when  A = 20;;
>     and   B = 10;;
>     and   length(lines_of_code) = 5
>     try   sepal_execution
>     catch lesson_passed = True
>
