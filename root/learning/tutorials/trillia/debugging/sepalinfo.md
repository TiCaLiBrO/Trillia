# Debugging

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/debugging

In this chapter, you'll learn about debugging.
Debugging is the process of figuring out what's happening inside of a codebase.

## Lesson 1

[/debug operator](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/debugging/debug%20operator/sepalinfo.md)

You will learn: How to use the debug operator

/////////////////////////////////////////
Old
/////////////////////////////////////////




Using the `?` operator at the end of a line, with a space between it and the last object, prints out every evaluation and change that occurs on that line.

    x = 3
    while x != 1
        if x /@ 2
        then x / 2 ?
        else x * 3 + 1
>>> then x / 2 where x = 10 relatively assigns x = 5
>>> then x / 2 where x = 16 relatively assigns x = 8
>>> then x / 2 where x = 8 relatively assigns x = 4
>>> then x / 2 where x = 4 relatively assigns x = 2
>>> then x / 2 where x = 2 relatively assigns x = 1

If you want to monitor every line of code from a starting point to an end point, you can use the `?* *?` debug brackets.
They behave the same as the end of line `?`.

Using `try`, `when`, and `catch`, you can make your program behave differently to avoid a crash.

    when zero_division_error
    try
        x / y
    catch
        print("invalid input")

If your program has a compiler error, you can use `catch` and `ignore` to let your program run anyway.

    catch proven_pointer_cycle_error
        ignore

Because many errors usually result in or are caused by `Undefined` values, and because `Undefined` returns `Undefined` when augmented, this can result in accumulation of `Undefined` variables.
