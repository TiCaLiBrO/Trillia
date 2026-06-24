# Basic Arithmetic Trial

## Prelude

//

## The Trial

This trial will have you make three print statements.
Use `printn` for all of them.

### The first print statement:

You are given the statement `600 - 100 + 80`.
By adding brackets, change the order of operations such that both 100 and 80 are subtracted from 600.

### The second print statement
You are given `10 + 20 + 30 + 40 + 50 + 60 + 1 + 2 + 3 + 4 + 5 + 6`.
By only adding `-` signs in front of numbers to make them negative, make their sum result in `69`.

### The third print statement
You are given four values. `5310000`, `10620000`, `8016`, `8`, in that order.

Take the absolute difference of the first two values, the sum of the middle two values, and the difference of the final two values.

Chain each operation.

Run the code when ready.

> [!IMPORTANT]
> Invisible within Sepal
>
>     try   sepal_execute
>     when  standard_output has "420"
>     and   standard_output has "69"
>     and   standard_output has "5318008"
>     and   source_code has "600 - (100 + 80)" # we need to be lenient for whitespace
>     and   source_code has "10 + -20 + 30 + 40 + 50 + -60 + -1 + 2 + 3 + 4 + 5 + 6" # there may be several ways. I have to prove otherwise
>     and   (source_code has "5310000 delta 10620000 + 8016 - 8" or source_code has "+(5310000 - 10620000) + 8016 - 8") # also need to add lenience
>     catch lesson_passed = True
>
> [\trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)
