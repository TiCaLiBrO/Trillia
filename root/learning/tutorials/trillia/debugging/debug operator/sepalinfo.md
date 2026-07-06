# Debug Operator

You are here@[root](https://github.com/TiCaLiBrO/Trillia/blob/main/root/sepalinfo.md)/[learning](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/sepalinfo.md)/[tutorials](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/sepalinfo.md)/[trillia](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/sepalinfo.md)/[debugging](https://github.com/TiCaLiBrO/Trillia/blob/main/root/learning/tutorials/trillia/debugging/sepalinfo.md)/debug operator

## Prelude
The `?` operator can be appended to a variable to track and print every change that happens to it from that point in the code onward.

    x? for 1-100          # The ? at the end of x is used to show that we are tracking x.
        if is_prime(x)
        then x / 2
        else x * 3 + 1


## The Task

> [!IMPORTANT]
> Invisible within Sepal.
>
> code
>
> next lesson []

# 6. Debugging
    x = 3
    x?        # this line is used to explicitly track x
    while x != 1
        if x /@ 2 then x / 2 else x * 3 + 1

This prints out:

>>> while x != 1 where x = 3 returns True to while
>>> 
>>> if x /@ 2 where x = 3 returns False to if
>>> 
>>> else x * 3 + 1 where x = 3 relatively assigns x = 10
>>>
>>> while x != 1 where x = 10 returns True to while
>>>
>>> if x /@ 2 where x = 10 returns True to if
>>>
>>> then x / 2 where x = 10 relatively assigns x = 5
>>>
>>> while x != 1 where x = 5 returns True to while
>>>
>>> if x /@ 2 where x = 5 returns False to if
>>>
>>> else x * 3 + 1 where x = 5 relatively assigns x = 16
>>>
>>> while x != 1 where x = 16 returns True to while
>>>
>>> if x /@ 2 where x = 16 returns True to if
>>>
>>> then x / 2 where x = 16 relatively assigns x = 8
>>>
>>> while x != 1 where x = 8 returns True to while
>>>
>>> if x /@ 2 where x = 8 returns True to if
>>>
>>> then x / 2 where x = 8 relatively assigns x = 4
>>>
>>> while x != 1 where x = 4 returns True to while
>>>
>>> if x /@ 2 where x = 4 returns True to if
>>>
>>> then x / 2 where x = 4 relatively assigns x = 2
>>>
>>> while x != 1 where x = 2 returns True to while
>>>
>>> if x /@ 2 where x = 2 returns True to if
>>>
>>> then x / 2 where x = 2 relatively assigns x = 1
>>>
>>> while x != 1 where x = 1 returns False to while
>>>
>>> It's very verbose and goes through every change for which x is either queried or changed.
