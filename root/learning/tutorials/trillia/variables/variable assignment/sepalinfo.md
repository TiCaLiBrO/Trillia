# Variable Assignment

## The Task

This program prints `Undefined`, but we want it to print a number.

    number
    print(number)

Rewrite the code so that the first line becomes `number = 10`.
Run the code after you've fixed it.

## Explanation

Now, when you run the code, it prints `10`.
This is because `number` is a variable that holds the value 10.
When `print` sees `number`, it can't actually see the variable's name.
Instead, `print` only sees what value `number` holds.
That's why earlier it printed `Undefined` because `number` didn't hold any value until you gave it one.

> [!IMPORTANT]
> Invisible within SEPAL.
>
>     when number = 10
>     try sepal_execution
>     catch lesson_pass = True
>
> [next lesson]
