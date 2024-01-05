# holbertonschool-monty
Monty ByteCode Interpreter

About

In this project, we have developed a simple interpreter for Monty ByteCodes. The interpreter reads a bytecode file and executes the bytecode commands.

The Monty Language

Monty 0.98 is a scripting language initially compiled into Monty byte codes, similar to Python. It relies on a unique stack with specific instructions for manipulation.

Monty Byte Code Files

Files containing Monty byte codes typically have the .m extension. Although most of the industry adheres to this standard, it is not required by the language specification. Each line contains no more than one instruction, and any number of spaces before or after the opcode and its argument is permitted.

Compilation & Output

These codes were compiled using the following command:

bash
Copy code
gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
Any output must be printed on stdout, while error messages must be printed on stderr.

Examples

bash
$ cat -e bytecodes/000.m

push 0$
push 1$
push 2$
push 3$
pall$
push 4$
push 5$
push 6$
pall$

Tasks

Mandatory
push, pall: Implement the push and pall opcodes.
pint: Implement the pint opcode.
pop: Implement the pop opcode.
swap: Implement the swap opcode.
add: Implement the add opcode.
nop: Implement the nop opcode.

Author

[Author Name] 

