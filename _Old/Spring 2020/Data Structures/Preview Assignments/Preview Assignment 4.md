## Zachary Sy<br>Preview Assignment 4

#### 1. In your own words, describe what the computing device and Harvard architecture are doing when you run the nothing.cpp code presented in the lecture.
The computing device sees that there is a procedure to be performed, and that there is nothing in the input device. The computing device then starts the procedure with a curly brace. The device then informs the OS that the procedure was successful by sending `0` to the output device. The device then ends the procedure with the closing curly brace.

#### 2. In your own words, describe what the computing device and Harvard architecture are doing when you run the hello.cpp code presented in the lecture.

The computing device sees that there is a procedure to be performed, and that there is nothing in the input device. The computing device then starts the procedure with a curly brace. The characters of “`Hello, World`” are then stored in data memory. Then the `std::cout` method is called, which calls `fwrite`, which sends the characters and a newline to output.  The device then informs the OS that the procedure was successful by sending `0` to the output device. The device then ends the procedure with the closing curly brace.

#### 3. Briefly describe the three main elements of the Instruction Memory / Stack

The **stack** contains function calls and local variables. The next element in the is the **static and global variables** to simplify computing execution. The third element is the actual **code** that is being run

<br> 

#### 4. Briefly describe the purpose of the Data Memory / Heap

The heap is used for dynamic memory allocation of variables, such as arrays or trees or graphs. Their memory is allocated at runtime. Elements can be randomly accessed anytime. Also, blocks can be allocated and freed at anytime.

#### 5. Write a Production Quality Compilation Makefile with two executables

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

# Compilation for the "testFloat" program
# Command: make testFleat
testFloatObj :=  $(04)/testFloat.o

testFloat: $(04)/testFloat.o 
	$(PP) $(CXXFLAGS) -o $(04)/testFloat $(testFloatObj)

testFloat.o: $(04)/testFloat.cpp 
	$(PP) $(CXXFLAGS) -c $(04)/testFloat.cpp

# Compilation for the "testDouble" program
# Command: make testFleat
testDoubleObj :=  $(04)/testDouble.o

testDouble: $(04)/testDouble.o 
	$(PP) $(CXXFLAGS) -o $(04)/testDouble $(testDoubleObj)

testDouble.o: $(04)/testDouble.cpp 
	$(PP) $(CXXFLAGS) -c $(04)/testDouble.cpp
	
# Make all
all: testFloat testDouble

# Make clean
clean :
	rm -rf *.o testFloat testDouble

```