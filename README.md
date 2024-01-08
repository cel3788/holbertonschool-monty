# Monty Interpreter

## Project Overview

This project involves the implementation of a Monty interpreter in C. Monty is a scripting language with its bytecode files, and the goal is to create an interpreter that executes Monty bytecode instructions.

## Data Structures

Please use the following data structures in your implementation. Include them in your header file (`monty.h`):

```c
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
    int n;
    struct stack_s *prev;
    struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
    char *opcode;
    void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;


ChatGPT
Bien sûr, voici un exemple de fichier README en Markdown pour votre projet Monty :

markdown
Copy code
# Monty Interpreter

## Project Overview

This project involves the implementation of a Monty interpreter in C. Monty is a scripting language with its bytecode files, and the goal is to create an interpreter that executes Monty bytecode instructions.

## Data Structures

Please use the following data structures in your implementation. Include them in your header file (`monty.h`):

```c
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
    int n;
    struct stack_s *prev;
    struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
    char *opcode;
    void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;
List of Files/Descriptions

S/N	Files	Description
1.	monty.h	Header file
2.	monty.c	Main file
3.	stack_operations.c	Stack operation functions
4.	opcode_functions.c	Opcode handling functions
5.	error_handling.c	Error handling functions

Compilation & Output

These codes were compiled using:
bash
Copy code
gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
Any output must be printed on stdout.
Any error message must be printed on stderr.
Examples

Example #1
bash
Copy code
~/monty$ cat -e bytecodes/00.m
push 1$
push 2$
push 3$
pall$
~/monty$ ./monty bytecodes/00.m
3
2
1
Example #2
bash
Copy code
~/monty$ cat bytecodes/07.m
push 1
push 2
push 3
pall
pop
pall
pop
pall
pop
pall
~/monty$ ./monty bytecodes/07.m
3
2
1
2
1
1
Example #3
bash
Copy code
~/monty$ cat bytecodes/09.m
push 1
push 2
push 3
pall
swap
pall
~/monty$ ./monty bytecodes/09.m
3
2
1
2
3
1
Running the Monty Program

To run the Monty program, use the following command:

bash
Copy code
./monty file
file is the path to the file containing Monty bytecode.
If the user provides no file or more than one argument, the program will print the error message USAGE: monty file and exit with EXIT_FAILURE.
If the file cannot be opened, the program will print the error message Error: Can't open file <file> and exit with EXIT_FAILURE.
If the file contains an invalid instruction, the program will print the error message L<line_number>: unknown instruction <opcode> and exit with EXIT_FAILURE.
Tests

We encourage collaboration on a set of tests to ensure the correct functionality of the Monty interpreter.

AUTHORS CELESTINE AND KAIS 

