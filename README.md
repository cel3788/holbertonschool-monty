**About:** In this project, we created a simple interpreter for Monty ByteCodes. The interpreter reads a bytecode file and executes the bytecode commands.

### The Monty language

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it.


### Monty byte code files

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument


## Compilation & Output

* These codes were compiled using: ```gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty```

* Any output must be printed on ```stdout```

* Any error message must be printed on ```stderr```


## Examples

```

julien@ubuntu:~/monty$ cat -e bytecodes/000.m

push 0$

push 1$

push 2$

  push 3$
                   pall    $
push 4$

    push 5    $
      push    6        $
pall$

julien@ubuntu:~/monty$

```


## Tasks:

### Mandatory:-

0. push, pall

   Implement the push and pall opcodes.

1. pint

   Implement the pint opcode.

2. pop

   Implement the pop opcode.

3. swap

   Implement the swap opcode.

4. add

   Implement the add opcode.Implement the add opcode.

5. nop

   Implement the nop opcode.


Celestine 