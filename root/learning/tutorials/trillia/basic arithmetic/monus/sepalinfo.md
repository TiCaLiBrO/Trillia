# Monus

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[basic arithmetic](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/sepalinfo.md)/monus

## Prelude

It's time to learn the final operation in basic arithmetic, *monus*.

### What Is Monus?

Monus is a form of subtraction that is never negative - much like delta.
However, unlike delta, monus isn't about absolute difference.
Monus is subtraction where the minimum result is 0.

`A monus B` is the same as `maximum(A - B, 0)`.
Here, the maximum() function is just a function that compares two values, A - B, and 0, and whichever value is larger, it uses that one.
Make sure there is a space between `monus` and the values it is operating on.
Just like delta, you never have to consider negative numbers.

> [!NOTE]
> If you are using Trillia's *official ligatures*, `monus` may look like `∸` when you write it.
> That symbol is the most common symbol used for monus in mathematics, and it's often called 'dot minus'.
> Don't worry, it's just for readability, and it will not affect the result of the program.

## The Task

Take any two numbers and, using monus, get their absolute difference.

Print the result.

Run when ready.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execute
>     when  source_code has "print"
>     and   source_code has "monus"
>     and   source_code not has "maximum("
>     catch lesson_passed = True
>
> next lesson [\basic arithmetic/basic arithmetic trial](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/basic%20arithmetic/basic%20arithmetic%20trial/sepalinfo.md)





