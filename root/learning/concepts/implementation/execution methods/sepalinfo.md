# Execution Methods

## What are execution methods?

An execution method is about how a program is run. Generally, programs come in two main forms: Interpreted or compiled.

## Interpreted Programs

Interpreted programs are run by an interpreter.
The interpreter is a program that reads the code and then follows the instructions.
It's like an enzyme reading DNA.
The enzyme trails up the strand of DNA and follows the instructions given by it.
The actual thing doing the work is the enzyme, not the DNA, just as the interpreter, not the code, is doing the work.
Interpreted code is generally more flexible but further from the hardware, making it slower as a consequence.

## Compiled Programs
A compiler is a program that translates your human-readable code into another language - usually machine-readable code (although not always).
A compiler is just a translator; that's it.
You can think of it in the same way as a program that translates German into French.
Programs that are translated into machine-readable code are called executables.
Executables are programs that can be run by your computer directly, without the need to be interpreted.

### Ahead of Time Compilation

There are actually two kinds of compilation: Just-in-Time and Ahead-of-Time.
Ahead-of-time compilation is the most common type. A program is turned into an executable file, then the file sits around in your computer to be executed.
Ahead-of-time compilation is the fastest possible way to run your code.
If it's the fastest way, why isn't it used everywhere?
Because translating takes time.
If I give you a book in Italian and tell you to translate it into English, it will take you some time to translate it.
The compiler is no different.
Compilers are slow, and what they do is translate your code into a language that your computer can understand so that the program can run faster later, but translating that code is a slow process.
So essentially, when you compile code, you're spending some time now to make your code run faster later.

### Just in Time Compilation

The other way to compile your code is much more similar to interpretation.
Instead of having an interpreter, you have a just-in-time compiler (JIT compiler).
The JIT compiler is a program that reads your code, copies it, compiles it piece by piece, and runs those pieces.
So instead of translating that book from Italian to English, you're writing each verse into English and then reading them out sentence by sentence.
The biggest difference between JIT compilation and interpretation is that an interpreter isn't actually translating your code; it's just a large program designed to follow the code's instructions.
A JIT compiler translates your code into machine-readable code on the fly, and the computer runs the instructions.
The JIT compiler is still only a translator, and doesn't participate in the execution of your code.

## Is Trillia Compiled or Interpreted?
Compiled, technically, but that's a massive oversimplification.
Trillia is compiled ahead-of-time by default, but Trillia's compiler has an interpreter inside of it.
The interpreter is actually designed to read the code and follow *some* of the instructions to simplify them, then it puts the results back into the compiled code.
Because Trillia has an interpreter built into its compiler, it has both a compiler and an interpreter, and as such, it's built to be compiled and interpreted readily.
Trillia can be AOT compiled, JIT compiled, or interpreted.
Each method is better for certain tasks and worse for others.

In all, there are seven methods to run a Trillia program.
1. Run an AOT compiled Trillia file (machine executable)
2. Run a Trillia file by interpreting the source code
3. Run a Trillia file by JITing the source code
4. Run a half-compiled intermediate representation Trillia file using JIT
5. Run a half-compiled intermediate representation Trillia file using interpretation
6. Run a losslessly compressed source code Trillia file using JIT
7. Run a losslessly compressed source code Trillia file using Interpretation




















