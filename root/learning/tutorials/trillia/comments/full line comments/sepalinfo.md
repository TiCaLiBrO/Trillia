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

In this lesson, you will learn about the `##` full-line comment operator.

We'll take a look at the same example, with the `##` operator instead:

    printn("I like sharks")
    printn("Me too") ##

If you use one `#` symbol, you comment out everything to the right.
With two `##`, you comment everything to the left.
With three `###` or more, both the left and right sides are commented out.

> [!NOTE]
> Technically, there is no `###` symbol in Trillia. It's just `comment ##` plus `# comment` to make `comment ### comment`, to make a full-line comment.

*One advantage* that this provides you is the ability to comment out the code, but also gives you the ability to write an actual comment.

    printn("I like sharks")
    printn("Me too") ### This code was commented out

You can get rid of two `#` characters to return the code on the left back to working condition.
This doesn't come with the cost of shifting your code to the right.

If you look at the alternative, once you get rid of the `#` character, if you had a comment on the same line, it becomes broken code! 

    #printn("Me too") This code was commented out

becomes this:

    printn("Me too") This code was commented out

Which, by the way, will make your code suddenly not work.

## The Task

With your newfound powers, you can turn code into comments without misaligning it.

    printn("Her: What are you doing tonight?")
    printn("Him: Not much")
    printn("Him: You?")

Take the code above and turn the middle line into a comment *without misaligning it*.

On the same line as the nullified code, add the comment `Message unsent` on its right side.


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

