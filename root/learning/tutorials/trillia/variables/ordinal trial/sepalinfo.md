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
>     include source_code
>
>     constant assignments = ["a = x", "a = y", "a = z", "x = a", "x = y", "x = z", "x = a", "y = x", "y = z", "z = a", "z = x", "z = y"]
> 
>     is_only_assignment =
>         default False
>         if    all line in lines_of_code
>         where line in assignments
>         then  return True
>
>     if is_only_assignment
>     then
>         test_count        = 100
>         test_passed_count =   0
>         tests             =  []
>         for x in 1-test_count
>             (tests)append([random_integer(1, 100), random_integer(1, 100), random_integer(1, 100)])
> 
>         for test in tests
>             print("Test " + as_string(test) + ": ")
>             x = tests[test][1]
>             y = tests[test][2]
>             z = tests[test][3]
>             sepal_execute
>             if  x = tests[test][3]
>             and y = tests[test][1]
>             and z = tests[test][2]
>             then
>                 print("Passed.")
>                 test_passed_count + 1
>             else
>                 print("Failed.")
> 
>         passed_or_failed =
>             default "Failed."
>             if test_passed_count = test_count
>             then return "Passed."
> 
>         print("Trial " + passed_or_failed)
>
>     else
>         print("Attempt failed. Not all lines of code were assingments.")
> 
> [next lesson]





