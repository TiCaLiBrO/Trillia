The second stage of the Trillian compiler is tagging.

Once the code has been translated into IR, it can be tagged by the properties it has.
Tags are extremely important because they tell the later stages of the compiler how to properly handle certain code.

Tags come in mostly two forms. The first form is optimization tags.
These tags include commutativity and associativity flags to help with parallelization.
Certain operations have certain mathematical properties, and knowing them can be useful for calculating results more efficiently.
To give a demonstration, 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 does not have to happen one step at a time.
Because for addition, the order that you add two numbers together does not matter; the compiler can tag this expression so that it can do each step in parallel.

The second, and much more important kind of tagging is blight tagging.
In Trillia, *blight* is the term for anything that is not deterministic, and potentially non-halting.
Anything that ruins determinism, such as user input, date and time, or randomness, will be tagged as blight.
Blighted code is not able to undergo some of the Trillia compiler's optimizations safely, so this tagging is very important.
Deterministic algorithmic code - non-blighted code - is able to be presolved before runtime.


