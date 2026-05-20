# Ordinal Trial

## Prelude

Assignment allows us to swap data.
Using the techniques you learned already, you can do what is called an Ordinal swap.
Ordinal here just means that it's a swap that happens step-by-step.

## The Trial

Using the methods that you are familiar with, you can have two variables, `x` and `y`.
You will need to create a third variable, `z` that can be used to copy the data from `x` and `y`.

In this trial, you are limited to three variables.

Your program already has these two lines of code written:

    x = value1
    y = value2

You don't know the values of `value1` and `value2`.
Just write the program as if you had already set the values of x and y.
Also, this trial will print for you, so you don't need to worry about print statements either.
You should only be concerned with how you're going to swap x and y, not with setting them up.
your only statements should be swaps: `"x = y"`, `x = z`, `y = x`, `y = z`, `z = x`, or `z = y`.

The rest is up to you.
Good luck.

> [!IMPORTANT]
> Invisible within Sepal.
> 
>     swaps_only =
>         default False
>         return True if all lines in lines_of_code where line in ["x = y", "x = z", "y = x", "y = z", "z = x", "z = y"]
>
>     if swaps_only
>     then
>         test1 = [
>             local value1 = 4
>             local value2 = 5
>         ]
> 
>         test2 = [
>             local value1 = 8
>             local value2 = 6
>         ]
> 
>         tests = [test1, test2]
>         test_passed_count = 0
> 
>         test for tests
>             print("Test " + as_string(test) + ": ")
>             x = tests[test]/value1
>             y = tests[test]/value2
>             sepal_execute
>             if  x = tests[test]/value2 ;;
>             and y = tests[test]/value1 ;;
>             then
>                 print("Passed.")
>                 test_passed_count + 1
>             else
>                 print("Failed.")
> 
>         passed_or_failed =
>             default "failed."
>             if test_passed_count = length(tests)
>             then return "passed."
> 
>         print("Trial " + passed_or_failed)
>
>     else
>         print("Attempt failed. Not all lines of code were assingments.")
> 
> [next lesson]


