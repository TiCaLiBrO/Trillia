# Adding Comments

## Prelude

Comments allow programmers to communicate their reasoning, take notes, and describe complicated code in human language.

The `#` character is used for creating comments.

You can start a line with `#` to make it a comment like this:

    # This is a comment

You can also use `#` in a line that contains code.
Everything to the right of the `#` character is a comment.

    print("Hello World") # This line of code prints "Hello World"

Having a line of code end with a comment is called a half-line comment.
Half of the line is code, and half of it is a comment.

## The Task

Here is some code that prints vertically.

    printn("H")
    printn("O")
    printn("R")
    printn("S")
    printn("E")

You know what it says, but if there were, say, 100 lines of printing, it might be difficult to tell what it says.

Copy the code above, but add the comment `# We use printn to print vertically` anywhere in the code.
Just make sure you add the comment ***at the end*** of a line.

> [!IMPORTANT]
>
>     try   sepal_execute
>     when  source_code has 'printn("H")'
>     and   source_code has 'printn("O")'
>     and   source_code has 'printn("R")'
>     and   source_code has 'printn("S")'
>     and   source_code has 'printn("E")'
>     and   source_code has "# We use printn to print vertically"
>     and   standard_output = "H\nO\nR\nS\nE\n"
>     catch lesson_passed   = True
>
> [next lesson]



