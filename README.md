# MyLib C Library Project

This project demonstrates building a static C library (`mylib.a`) and linking it with a main program to create an executable.

## Prerequisites

- GCC compiler (gcc)
- Make build tool

## Project Structure

- `src/mylib.c`: Source code for the library functions
- `include/mylib.h`: Header file declaring library functions
- `src/main.c`: Main program that uses the library
- `Makefile`: Build configuration
- `lib/`: Directory where the static library is created
- `output/`: Directory where the executable is placed

## Building the Library and Executable

To build the static library and the executable:

```bash
make
```

This will:
1. Compile `src/mylib.c` into `src/mylib.o`
2. Create the static library `lib/libmylib.a` from `src/mylib.o`
3. Compile `src/main.c` into `src/main.o`
4. Link `src/main.o` with `lib/libmylib.a` to create `output/main`

## Running the Executable

To build and run the program:

```bash
make run
```

This will execute `./output/main`, which prints "Hello World!" and demonstrates the `add` function from the library.

## Cleaning Up

To remove all object files, dependency files, the library, and the executable:

```bash
make clean
```

## Library Usage

The library provides a simple `add` function:

```c
#include "mylib.h"

int result = add(5, 3);  // Returns 8
