## Zachary Sy<br>Lecture 3

### Problem 1
```
# Author: Zachary Sy
# E-mail: zsy@nd.edu
#
# This is the Makefile for the CSE 20312 course Lecture 04

# G++ is for the GCC compiler for C++
PP := g++

# CFLAGS are the compiler flages for when we compile C code in this course 
FLAGS := -02 -g -Wall -Wextra -Wconversion -Wshadow -pedantic -Werror -lm
CXXFLAGS := -m64 -std=c++11 -Weffc++ $(FLAGS) 

# Variables for Folders
04 := ~/DSInClass/04-CPPIntro

# Compilation for the "ascii" program
# Command: make ascii
asciiObj :=  $(04)/ascii.o

ascii: $(04)/ascii.o 
	$(PP) $(CXXFLAGS) -o $(04)/ascii $(asciiObj)

ascii.o: $(04)/ascii.cpp 
	$(PP) $(CXXFLAGS) -c $(04)/ascii.cpp

# Compilation for the "squareFunc" program
# Command: make squareFunc
squareFuncObj :=  $(04)/squareFunc.o

squareFunc: $(04)/squareFunc.o 
	$(PP) $(CXXFLAGS) -o $(04)/squareFunc $(squareFuncObj)

squareFunc.o: $(04)/squareFunc.cpp 
	$(PP) $(CXXFLAGS) -c $(04)/squareFunc.cpp
	
# Make all
all: ascii squareFunc

# Make clean
clean :
	rm -rf *.o ascii squareFunc

```

### Problem 2
`Notre Dame\n`

### Problem 3
Typecasting integers greater than 126 would print out gibberish

### Problem 4
Allocating space for the `total` variable in the global stack. `main x,y` is put in the stack and pointed to, and one register each is allocated to `x` and `y`. The `x` register is then set to `3` and the `y` register is set to `4`. Then, `SumOfSquare x,y,z` isn added in the stack and registers are allocated to each of these `x,y,z` parameters, where `x-SOS` contains `3` and `y-SOS` contains `4`. Then `Square x` is added to the stack and `x-Square` is given a register and set to `49`, which when `return x` is called sets `z` to `49`. The stack is then popped along with any registers it used, and the pointer points to `SumOfSquares`. When `return z` is called, the global `total` is set to `49` and the stack is again popped and registers `SumOfSquares` used is cleared. Then the output is printed out, and when `return 0;` is called, the stack is emptied and any registers of `main` are cleared.
