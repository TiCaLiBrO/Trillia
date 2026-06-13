# Full Line Comments

## Prelude

In the previous lesson, you learned the *bad* way to turn code into comments.

Why is it bad? Take the following code as an example:

    print("I like sharks")
    print("Me too")

When you commented it in the previous way, you ended up with this:

    print("I like sharks")
    #print("Me too")

Notice how the print statements don't align?
That's bad for readability, and it's also harder to tell if it's actually supposed to be code or just a comment.

In this lesson, you will learn about the `###` full-line comment operator.

We'll take a look at the same example, with the `###` operator instead:

    print("I like sharks")
    print("Me too") ###

*One advantage* that this provides you is the ability to comment out the code, but also gives you the ability to write an actual comment.

    print("I like sharks")
    print("Me too") ### This code was commented out

You can get rid of two `#` characters to return the code back to working condition.
This doesn't come with the cost of shifting your code to the right.

If you look at the alternative, once you get rid of the `#` character, if you had a comment on the same line, it becomes broken code! 

    #print("Me too") This code was commented out

becomes

    print("Me too") This code was commented out

> [!NOTE]
> You *can* technically use just two comment symbols `##` to turn a full line of code into a comment, but it's *bad practice*, as you'll see in [\trillia/conditions].


## The Task




> [!IMPORTANT]
> Invisible within Sepal.
>
>     code
>
> [next lesson]

