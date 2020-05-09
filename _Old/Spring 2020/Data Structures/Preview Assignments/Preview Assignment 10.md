## Zachary Sy<br>Preview Assignment 10

#### 1. [20 points] - In your own words, describe how a templated class is constructed differently - be sure to describe how method declarations and method definitions are different - and describe why this difference is essential.

In writing templated classes, there should be a line
`template<class T, class U, ...> `
before the class, and `T, U, ...` are the types that are used for private variables and methods.

When making a class template, the compiler makes a copy of the class at runtime, and so the computing device does not know the actual value of the generic prior to runtime.  Because of this, the `.h` files must have function definitions to avoid errors.

#### 2. [15 points] - Describe, in your own words and in detail, the purpose of a destructor and when to call them.

A destructor is a member function which destructs or deletes an object. It is automatically called when the object goes of scope. Destructors have the same name as the class but with a tilde. The destructor should delete anything that is a pointer, otherwise leave it empty since the computing device automatically removes primitive types from the stack.

#### 3. [15 points] - Describe, in your own words, the Rule of Three, and its purpose in class construction.

The Rule of Three states that there are three member functions that must be defined if one of them is defined. Namely, the destructor, the copy constructor, and assignment operator. This ensures all possible ways of allocating and deallocating memory, and prevents segfaults

#### 4. [15 points] - Describe, in your own words, the purpose of the `this` pointer.

The `this` pointer allows a class to be referred to itself in its' methods, such as in the assignment operator. 

#### 5. [20 points] - Given a pointer to a class `A<float,int> object ptr*`, where the pointer's register is located at `0x17bb010`, whose contents point to the location in Data Memory of `0xdacc792`, and a correctly printed overloaded operator would print `"-6.23, 5"`, state the output of the following code segment:
```
A<float, int> *ptr = new A<float, int>(-6.23, 5);
std::cout << *ptr << std::endl;
std::cout << ptr << std::endl;
std::cout << &ptr << std::endl;
```

**Output:**

```
-6.23,5
0xdacc792
0x17bb010
```
#### 6) [15 points] - In your word document (not on the ND Machine), write a Production Quality Compilation Makefile which describe the compilation for one executable, a theoretical library declarations in a .h file, and theoretical program in a .cpp file.  (You may use the Makefile on the Lecture Code page as an example).

* Folder: ~/DSInClass/10-Templates
* Classes: $(10)/classes
* Programs: $(10)/programs
* Objects: $(10)/objects
* Executables: $(10)/executables
* Executable 1: irishTemp
* Main File: $(PROG)/irishTemp.cpp
Templated Class: $(CLASSES)/Q.h

```
# Author: Zachary Sy
# E-mail: zsy@nd.ehu
#
# This is the Makefile for the CSE 20312 course Lecture 10

# G++ is for the GCC compiler for C++
PP := g++

# CXXFLAGS are the compiler flages for when we compile C++ code in this course 
FLAGS := -O0 -g -Wall -Wextra -Wconversion -Wshadow -pedantic -Werror 
CXXFLAGS := -m64 -std=c++11 -Weffc++ $(FLAGS) 


10 := ~/DSInClass/10-Templates
CLASSES := $(10)/classes
PROG := $(10)/programs
OBJECTS := $(10)/objects
EXE := $(10)/executables


irishTempObjs := $(OBJECTS)/irishTemp.o

irishTemp: $(irishTempObjs)
	$(PP) $(CXXFLAGS) -o $(EXE)/irishTemp $(irishTempObjs)
	$(EXE)/./irishTemp


$(OBJECTS)/tempTest.o: $(PROG)/tempTest.cpp $(CLASSES)/Q.h
	$(PP) $(CXXFLAGS) -c $(PROG)/tempTest.cpp -o $@

# Make all
all: irishTemp

# Make clean
clean :
	rm -rf *.o $(OBJECTS)/* $(EXE)/*
```