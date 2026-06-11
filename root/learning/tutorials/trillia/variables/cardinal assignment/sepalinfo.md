# Cardinal Assignment

## Prelude

You already learned how to assign one variable the value of another in [\variables/variables assigning other variables](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/variables%20assigning%20other%20variables/sepalinfo.md), and if you passed the first trial, you've also learned how to swap values manually.
What you've learned so far is the *slow* way of swapping values.

## Ordinality in Brief

What you've learned already is called *Ordinal Assignment*.
To put it simply, Ordinal means that one assignment must happen *before* the other. c = a, *then* a = b, *then* b = c.

In math, ordinal numbers are numbers like 1st, 2nd, 3rd.
There is an order to them that must be followed.

## Cardinality in Brief

The name Cardinal stems from cardinal numbers such as 1, 2, and 3.
These numbers refer to *how many* of something there are, rather than which order they must happen in.
They are still given unique values, but they aren't necessarily bound to ordering.

You may think of it like a recipe.

1st step: gather the ingredients.
- sugar
- milk
- eggs

2nd step: throw them at people, telling them that you're the embodiment of chaos. Strike fear into the hearts of mere men.

You get the idea.

You need the ingredients before you can throw them at people, but the order in which you gather the ingredients does not actually matter.
If you had three people, you could send them to the far reaches of the earth to gather all three ingredients simultaneously.

Cardinal just means "can be done at the same time".
Modern computers can do multiple things at the same time, so usually doing lots of things simultaneously is faster than doing them one at a time.

When you write code that has steps done at the same time, that is called parallelization.
No other common programming language can do this automatically; it usually requires the programmer to write a lot of extra code to break a problem down into tasks that can be done at the same time.
Trillia can break problems down automatically, making it extremely fast without making it more complicated to reason about or write.

In Trillia, parallelization is more often referred to as *Cardinalization*.

## The Task

Before, you had to write the following:

    a = x
    x = y
    y = a

All of this, just to swap two values.

Now you will learn a much simpler way:

    x, y = y, x

This way uses one line instead of three, and does not require a third auxiliary variable.
This process is also faster because `x` and `y` are swapped cardinally rather than ordinally.

The `x` and `y` on the right side are copies of `x` and `y` before the swap ocurrs, and because of that, 

> [!CAUTION]
> You cannot make a cardinal swap that affects the same left-handed object multiple times:
> 
>     x, y, x = a, b, c
>
> This is not allowed because the statement assigns the value of x multiple times.

> [!CAUTION]
> Another mistake that can occur is not having the same number of arguments on the left and right side:
>
>     a, b, c = 1, 2
>
> This is not allowed because `c` doesn't have a partner on the right side.

## The Task

Now that you know how to write a Cardinal swap, it's time to put that to the test.

### Context

You are writing some code for a fantasy video game.
The hero can collect items that they find throughout their journey.
Whenever the hero wants, they can swap the item in their hand with one that is inside their inventory.

You are given two variables: `held_item` and `inventory_item`.
Use a Cardinal swap to swap them.

> [!IMPORTANT]
> Invisible within Sepal
>
>     try   sepal_execute
>     when  source_code   = "held_item, inventory_item = inventory_item, held_item"
>     or    source_code   = "inventory_item, held_item = held_item, inventory_item"
>     catch lesson_passed = True
> 
> [next lesson]

