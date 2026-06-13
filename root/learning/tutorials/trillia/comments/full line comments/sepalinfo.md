# Full Line Comments

## Prelude

In the previous lesson, you learned the *bad* way to turn code into comments.

Why is it bad? Take the following code as an example:

    printn("I like sharks")
    printn("Me too")

When you commented it in the previous way, you ended up with this:

    printn("I like sharks")
    #printn("Me too")

Notice how the print statements don't align?
That's bad for readability, and it's also harder to tell if it's actually supposed to be code or just a comment.

In this lesson, you will learn about the `###` full-line comment operator.

We'll take a look at the same example, with the `###` operator instead:

    printn("I like sharks")
    printn("Me too") ###

*One advantage* that this provides you is the ability to comment out the code, but also gives you the ability to write an actual comment.

    printn("I like sharks")
    printn("Me too") ### This code was commented out

You can get rid of two `#` characters to return the code back to working condition.
This doesn't come with the cost of shifting your code to the right.

If you look at the alternative, once you get rid of the `#` character, if you had a comment on the same line, it becomes broken code! 

    #printn("Me too") This code was commented out

becomes this:

    printn("Me too") This code was commented out

Which, by the way, will make your code suddenly not work.

> [!NOTE]
> You *can* technically use just two comment symbols `##` to turn a full line of code into a comment, but it's *bad practice*, as you'll see in [\trillia/conditions].

## The Task

With your newfound powers, you can turn code into comments without misaligning it.

    printn("Her: What are you doing tonight?")
    printn("Him: Not much") ### Message unsent
    printn("Him: You?")

Take the code above, and turn the middle line into a comment without misaligning it.

On the same line, add the comment `Message unsent` on the right side.


> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execute
>     when  lines_of_code has 'printn("Her: What are you doing tonight?")'
>     and   lines_of_code has 'printn("Him: Not much")'
>     and   lines_of_code has 'printn("Him: You?")'
>     and   lines_of_code has '###'
>     and   lines_of_code has 'Message unsent'
>     and   standard_output = "Her: What are you doing tonight?\nHim: You?"
>     catch lesson_passed   = True
>
> [next lesson]

