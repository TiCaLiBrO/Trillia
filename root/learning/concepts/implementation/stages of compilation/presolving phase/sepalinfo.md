The fifth phase of the compiler is the Presolve phase.

It interprets all code that is tagged as deterministic, running it to simplify it, leaving only blighted code to remain at runtime.
Because the code has been automatically parallelized and reordered to be faster for interpreters, this code can be interpreted in parallel.
This is potentially the longest step during compilation because Trillia literally runs an interpreter for your code inside the compiler to make sure everything is maximally reduced.

If your entire codebase is deterministic and algorithmic, the executable file will just be a bunch of constants, not an executable file.
This is because your entire program has been reduced - solved entirely at compile time during the presolve phase.
