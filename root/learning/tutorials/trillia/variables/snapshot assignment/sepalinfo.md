# Snapshot Assignment

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[variables](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/sepalinfo.md)/snapshot assignment

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
*By default*, variables are never changed unless deliberately reassigned.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execution
>     when  A                     = 20
>     and   B                     = 10
>     and   length(lines_of_code) =  5
>     and   standard_output       = "20\n10"
>     catch lesson_passed         = True
> 
> next lesson [\variables/chain assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/chain%20assignment/sepalinfo.md)



