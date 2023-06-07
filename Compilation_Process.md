# ELF (Executable and Linkable Format File)
It is a common standard file format used in UNIX system for executable files, object code, shared libraries and core dumps.
- `$ objdump -f <bin_file_name>` . Use this command critical info about the executable file.
- `$ objdump --disassemble <filename>`. Gives addresses of various functions in the executable file.

A complier converts a C program to an executable. There are four phases for a C program to be converted to an executable:-
1) Pre-processing - Removes comments, expands macros, includes header files like stdio.h .
2) Compilation - Generates a file `.s` file which is in assembly-level language.
3) Assembly - Assembler takes `.s` file as input and converts code to machine level language.
4) Linking - Links all the function calls with their definitions.

In each step, an intermediate file is generated and they are of different file formats.
- The pre-processing step generates a `.i` file and to view the file, execute `vi <filename>.i`.
- Compilation step generates a `.s` file and to view the file, execute `nano filename.s`.
- Assembly step generates a `.o` file and to view the file, execute `vi filename.o`.
- Linker adds some extra code to `.o` file and can be verified using size command.

### To generate all the intermediate files, execute the following command:- `gcc -Wall -save-temps filename.c –o filename`.
