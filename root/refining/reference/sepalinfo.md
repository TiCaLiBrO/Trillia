This is the Reference page. Here, you are able to look up how specific functions and keywords work. This part of the manual is more like a dictionary than a guide. It's best that you already familiarize yourself with the basics of Trillia before coming here, and if you get stuck remembering something specific, you may come here to find the exact object or symbol that is causing confusion.

From here, there are two pages accessible:
[/base trillia] and [/libraries].

If what you're looking for is inside of Trillia with no imports, then enter Base Trillia. If it's inside of any official library, then enter Libraries.

If you're not sure which, then look at the top of your program and see if there are any included libraries at the top.
If there is no library included at the top, then the symbol or keyword is in base Trillia or one of the Implicit Libraries.
If what you're looking for is a function, and there are no imports and no definition of the function inside of the code, then it's in one of the implicit libraries.
If there is a library included, then the next step is to think: Does the function I'm looking for behave deterministically?
If it's a purely mathematical function that behaves identically every time, doesn't access hardware, doesn't require randomness or input, and doesn't loop forever, then it's likely part of base Trillia.
If it isn't deterministic, then it's definitely from a library.






