# New Line Print

In the previous lesson, you used the print function on two different lines of code.
You may have noticed that there was only one line of text printed to the terminal.

Sometimes you might want to make a new line in your text.

You already learned `print`, but now you will learn `printn`.
The "n" stands for newline.
If you have a `printn` function, it automatically ends the text with a new line.

> [!NOTE]
> In Trillia, abbreviations are *extremely rare*, but the print function allows an abbreviation in `printn`.
> For debugging your code and seeing what's going on, you'll likely be using this function a lot, so it's important that the name is short and fast to write, and isn't intrusive.

In this lesson, you will write a program that prints **three** lines total.
The output should be:

    We
    Eat
    Rocks!

> [!TIP]
> The third line should not end in a new line!
> Use the `printn` function for the first two lines, and `print` for the final line.

> [!IMPORTANT]
> Not visible in SEPAL.
> The source code is:
>
>     when standard_output = "We\nEat\nRocks!"
>     then
>         lesson_passed = True




