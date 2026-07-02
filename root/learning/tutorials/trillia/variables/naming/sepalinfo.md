# Naming

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[variables](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/sepalinfo.md)/naming

## Prelude

When naming a variable, it's always a good idea to give it a suitable name that clearly describes what it does or what it represents.

Naming variables well has no downside and improves your code's readability.
If you ever work in a team, or plan on working on a project for a long time, it can be very difficult to understand what your code is supposed to be doing if it isn't named properly.

Take a look at this example:

    e = 12
    v = 8
    f = 6

You might be able to tell what this is supposed to be if you think about it.
This is supposed to represent a cube.

Here's the same code, but cleaned up a bit:

    edge_count   = 12
    vertex_count = 8
    face_count   = 6

One potential problem with using many single-letter names is that if someone later decides to use `v` to represent volume, they'll accidentally be using the same variable `v` that's used for vertices!
This can ruin your code, and it's often very difficult to debug.

## Naming Conventions

### Use Long Names
Naming your variables properly is **always better than using single-character names** like `x` or `y` if the variables are meant to represent something.

It is only acceptable to name your variables with single letters in purely mathematical contexts or on your home-made projects, not for production code.

If your variable represents how much something costs, you can name the variable `cost`, `price`, or `value`; maybe even `dollar_cost` to specify that it's the cost in dollars, not in cents or some other currency.

> [!NOTE]
> Do not use names that are way too long just for the sake of it.
> If you end up with a name like `the_number_of_days_until_christmas`, you might want to try to reduce it to `days_till_christmas`, dropping some grammar.
> A name can be pretty dense in meaning, so `spiders_per_square_kilometer` is acceptable because each word adds valuable context.
> If even one of the words in `spiders_per_square_kilometer` is dropped, the variable no longer has a name that literally describes what it represents accurately.
> It could be refactored to `square_kilometer_spider_count`, but it is still of the same density.
> Generally, try to make your name as dense as possible without losing exact meaning.
> `square_kilometer_spiders` is potentially ambiguous, and could refer to the number of spiders that are a square kilometer in size.

### Snake Case
In Trillia, snake_case is the proper naming convention for variables.
Snake case uses all lowercase letters, and between words, you use `_` instead of spaces.

So, 'quote of the day' becomes `quote_of_the_day`, hyperbolic time chamber becomes `hyperbolic_time_chamber`, and so on.
We use `_` between words because it makes it easier to tell that it's a single object.
For example, `quote` and `day` are two nouns, but we're specifically talking about the `quote_of_the_day` (which can be refactored into `daily_quote` or `todays_quote`).

## Naming Rules

### What's in a Name?

A valid name:
- Must always start with a letter a-z or A-Z.
- May contain letters, numbers 0-9, and underscores `_`.
- Must end in a letter or number.
- Must not contain consecutive underscores.

The letters that appear must appear within the English alphabet without accent marks, so `cafe`, `resume`, and `cliche` are proper.

The following are examples of valid names:

- `happiness`
- `x`
- `burgers4god`
- `I_will_never_learn_how_2_read`
- `A77FFF7777777777`
- `diamond_count`

All but two of these are *pretty bad* names, but all are technically allowed.

## Reading Comprehension

This task is a bit different.
When you're ready, write `start` and run it to be transferred to a series of questions.
Answer all of them correctly to pass this lesson.

### Question 1
Shorter variable names speed up code execution:
Answer `True` or `False`.

### Question 2
Programmers should save development time by giving their variables single-letter names:
Answer `True` or `False`.

### Question 3
Variable names may contain numbers:
Answer `True` or `False`.

> [!IMPORTANT]
> Invisible within Sepal.
>
>     try   sepal_execution
>     when  source_code = "start"
>     catch
>         print("Shorter variable names speed up code execution: True or False?")
>         when  source_code = "False"
>         catch
>             print("Programmers should save development time by giving their variables single-letter names: True or False?")
>             when  source_code = "False"
>             catch
>                 print("Variable names may contain numbers: True or False?")
>                 when  source_code   = "False"
>                 catch lesson_passed = True
>     if   lesson_passed = True
>     then print("Lesson passed.")
>     else print("Lesson failed, try again.")
> 
> next lesson [\variables/string assignment](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/variables/string%20assignment/sepalinfo.md)














