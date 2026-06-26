# Debugging



/////////////////////////////////////////
Old
/////////////////////////////////////////


# 6. Debugging
The `?` operator can be appended to a variable to track and print every change that happens to it from that point in the code onward.

    x = 3
    x?        # this line is used to explicitly track x
    while x != 1
        if x /@ 2 then x / 2 else x * 3 + 1

This prints out:
>>> while x != 1 where x = 3 returns True to while
>>> if x /@ 2 where x = 3 returns False to if
>>> else x * 3 + 1 where x = 3 relatively assigns x = 10
>>> while x != 1 where x = 10 returns True to while
>>> if x /@ 2 where x = 10 returns True to if
>>> then x / 2 where x = 10 relatively assigns x = 5
>>> while x != 1 where x = 5 returns True to while
>>> if x /@ 2 where x = 5 returns False to if
>>> else x * 3 + 1 where x = 5 relatively assigns x = 16
>>> while x != 1 where x = 16 returns True to while
>>> if x /@ 2 where x = 16 returns True to if
>>> then x / 2 where x = 16 relatively assigns x = 8
>>> while x != 1 where x = 8 returns True to while
>>> if x /@ 2 where x = 8 returns True to if
>>> then x / 2 where x = 8 relatively assigns x = 4
>>> while x != 1 where x = 4 returns True to while
>>> if x /@ 2 where x = 4 returns True to if
>>> then x / 2 where x = 4 relatively assigns x = 2
>>> while x != 1 where x = 2 returns True to while
>>> if x /@ 2 where x = 2 returns True to if
>>> then x / 2 where x = 2 relatively assigns x = 1
>>> while x != 1 where x = 1 returns False to while
It's very verbose and goes through every change for which x is either queried or changed.

Using the `?` operator at the end of a line, with a space between it and the last object, prints out every evaluation and change that occurs on that line.

    x = 3
    while x != 1
        if x /@ 2
        then x / 2 ?
        else x * 3 + 1
>>> then x / 2 where x = 10 relatively assigns x = 5
>>> then x / 2 where x = 16 relatively assigns x = 8
>>> then x / 2 where x = 8 relatively assigns x = 4
>>> then x / 2 where x = 4 relatively assigns x = 2
>>> then x / 2 where x = 2 relatively assigns x = 1

If you want to monitor every line of code from a starting point to an end point, you can use the `?* *?` debug brackets.
They behave the same as the end of line `?`.

Using `try` and `(catch??? , except???)`, you can make your program behave differently to avoid a crash.

    when zero_division_error
    try
        x / y
    catch
        print("invalid input")

If your program has a compiler error, you can use `catch` and `ignore` to let your program run anyway.

    catch proven_pointer_cycle_error
        ignore

Because many errors usually result in or are caused by `Undefined` values, and because `Undefined` returns `Undefined` when augmented, this can result in accumulation of `Undefined` variables.
