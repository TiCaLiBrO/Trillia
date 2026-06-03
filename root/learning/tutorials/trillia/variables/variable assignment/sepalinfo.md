# Variable Assignment

## What Is a Variable?

Variables are names that hold values.
For example, you can have a name `age` that holds a value of 25.

## The Task

Type the following into your terminal:

    number = 12
    print(number)

Then run it. You should see `12` printed on your screen.

## Explanation

In lesson 2 of Chapter 1 [\trillia/printing/multiple statements](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/printing/multiple%20statements/sepalinfo.md), you learned that using `"Hello World!"` required quotation marks for it to be recognized as text.
In this chapter, you see exactly why.
If you were to type `print(Hello World!)` without quotation marks instead, it would be mistaken for code.

When you run your program with `print(number)`, it's not the same as `print("number")`.
`"number"` is just text, while `number` is a variable that holds the value 12.
When `print` sees `number`, it can't actually see the variable's name.
Instead, `print` only sees what value `number` holds.

The `=` sign is used to give a value to something.

> [!CAUTION]
> If you write `number` without writing `= 12` and then `print(number)`, you will get an error called `DeclarationError`.
> The error happens because `number` is a name that has no definition.
> When you make a name, that's called a declaration; you're declaring that the name exists.
> Every time you make a name, you must also define it in some way.
> You cannot declare a name without also defining it.

> [!IMPORTANT]
> Invisible within SEPAL.
>
>     when number = 12
>     try sepal_execution
>     catch lesson_pass = True
>
> [next lesson]

