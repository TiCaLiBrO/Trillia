# Assembly

## What Is Assembly?

On physical machines, computation is just a physical process.
Electricity flows through transistors, and information is printed onto a disc.
Computers require hardware to function.
That hardware is usually very predictable, with 1s and 0s as the language of information, and register sizes at powers of 2.
This doesn't have to be the case, and traditionally, register sizes were very nonstandardized.
Throughout history, other radixes were tested for computation, and even today, certain machines use other radixes for specialized tasks.

Most modern computers use one of these three assembly brands: x86, RISC, or ARM.

An assembly language is a language that translates 1:1 with the hardware.
Meaning that each instruction is a process that the computer can perform.
For example, if your computer can add two numbers, it's likely because it has an adder chip.
The computer might recognize 1100 as an add operation, with the next few 1s and 0s as the inputs, but the assembly language turns 1100 into ADD(_, _).
The 1100 and ADD are the same thing; it's just that ADD is more readable to humans.

## Limitations of Assembly

Assembly is only capable of making 1:1 translations; it can only do exactly what the hardware can do.
Because of this, it's a very rigid kind of language.
Assembly languages are known for being untyped, meaning that you can use any data as any data type.
For example, all numbers are just bits.
If you have a 32-bit integer and a 32-bit unsigned integer, there is nothing different about them.
You can use unsigned operations on a signed integer, and it will work just fine, but it may affect the sign bit in unintended ways.

Another limitation of assembly languages is that they tend to be limited to jump instructions.
Jump instructions allow a computer to jump back and forth through your code to execute it several times (think a loop or a function call).
They have one critical weakness, though: they're really difficult to analyze.
This makes them extremely unsafe, difficult to reason about, and horrible for safety-critical code.

## Tria

Tria is a nativary assembly language, meaning that it's a language native to all machines.
If different machines have different hardware, then how is this possible?
Tria ---------













