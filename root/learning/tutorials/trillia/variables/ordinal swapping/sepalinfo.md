# Ordinal Swapping

## What Is Ordinal Swapping?

Ordinal swapping is when you have two variables that need to be swapped, and you use a third variable (*often called an auxiliary variable*) to help them swap values.

It's called *Ordinal* because each step happens in order. First step, then second step, then third step.
This is the manual way to swap two values.
You will eventually learn a much faster way.

## The Task:

In this assignment, Alice and Bob each have a toy that they want to trade.

You learned in [\variables/snapshot assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/snapshot%20assignment/sepalinfo.md) that a variable only holds the value that it's given, and doesn't change value if other variables' values change later.

### What We Cannot Do

Your intuition might be this:

    bob_toy   = alice_toy
    alice_toy = bob_toy

However, there's a problem in this code.

If Bob's toy is a monkey, and Alice's toy is a giraffe, as soon as we assign Bob's toy the value of Alice's, Alice and Bob both have a Giraffe.
This is because `=` is a copy operation, not a trade operation.

### Something New

Instead of creating your own variables, for this lesson, some of the code is written for you.

`alice_toy` and `bob_toy` are the variables you will be using.
You aren't told what toys they have that they want to trade.

So for this lesson, you don't have to worry about assigning `bob_toy = "monkey"` or anything like that.
And you also don't even know if it is a monkey for this lesson - Alice and Bob want to keep their toy-exchange secret!

## The Task

Here's the special trick that you will need in order to swap two variables.
In this lesson, you can just follow the instructions, but in the next lesson, you won't be told how to swap them.

- Create a variable named `auxiliary`, and give it the value of `bob_toy` (remember, `bob_toy` already exists).
- Assign `bob_toy` the value of `alice_toy`.
- Assign `alice_toy` the value of `auxiliary`.

Run your code when ready.

## Why This Works

You assigned `auxiliary` the value of Bob's toy, and so when you later made Bob's toy equal to Alice's toy, `auxiliary` still kept the old value of Bob's toy.
Then you copied the value of Bob's old toy into `alice_toy`, so they were able to trade toys successfully.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     test1             = ["Monkey", "Giraffe"]
>     test2             = ["Chicken", "Shark"]
>     tests             = [test1, test2]
>     test_passed_count = 0
>
>     for test in tests
>         bob_toy        = test[1]
>         alice_toy      = test[2]
>         sepal_execute
>         if   bob_toy   = test[2]
>         and  alice_toy = test[1]
>         then test_passed_count + 1
>
>     if   test_passed_count = length(tests)
>     then lesson_passed     = True
>     else print("Lesson failed.")
>     
> [next lesson](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/ordinal%20trial/sepalinfo.md)

