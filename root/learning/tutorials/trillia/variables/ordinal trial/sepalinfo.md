# Ordinal Trial

## Prelude

Using the techniques you learned in the previous lesson, it's now your turn to figure out how to perform an Ordinal swap on three values.

## The Trial

In the previous lesson, you had two variables that you wanted to swap.
In this trial, you will swap the values of three variables and use one auxiliary variable.

In this trial, you are given four variables: `x`, `y`, `z`, and `a`.
You must use only those four variables.
Your task is to give `y` `x`'s value, `z`, `y`'s value, and `x` `z`'s value.

Just like the previous assignment, the values of `x`, `y`, and `z` are unknown.

Just write the program as if you had already set the values of x, y, and z.
Also, this trial will print for you, so you don't need to worry about print statements either.
You should only be concerned with how you're going to swap x and y, not with setting them up.
Your only statements should be swaps: `"a = x"`, `"a = y"`, `"a = z"`, `"x = a"`, `"x = y"`, `"x = z"`, `"x = a"`, `"y = x"`, `"y = z"`, `"z = a"`, `"z = x"`, or `"z = y"`.

The rest is up to you.

Good luck.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     include random
> 
>     swaps_only =
>         default False
>         if    all line in lines_of_code
>         where line in ["a = x", "a = y", "a = z", "x = a", "x = y", "x = z", "x = a", "y = x", "y = z", "z = a", "z = x", "z = y"]
>         then  return True
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
>             sepal_execution
>             if  x = tests[test]/value2
>             and y = tests[test]/value1
>             then
>                 print("Test passed.")
>                 test_passed_count + 1
>             else
>                 print("Test failed.")
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


<!-- // a more advanced three-variable or four-variable swap. -->
<!-- The previous lesson is a warm-up before the trial. Have the Trial be an extended version with 4 variables? -->



