## Zachary Sy<br>Preview Assignment 9

#### 1. [15 points] - In your own words, describe what is being done by the following code segment:

```
typedef double REAL;
```

`typedef` allows the `double` type to be referred to as a `REAL` type.

#### 2. [30 points] - Given the following class name and members, write a PQC default constructor code segment for the .cpp file. You must include the member initialization list with the members defined in order. (Hint: Make the default GPA 4.0, the default ndID 9000000000. Hint: you can call the default constructor for the strings, such as lastName() in the member initialization list will correctly create a default string)

```
class Student{

private:
    double GPA;
    unsigned int ndID;
    std::string lastName;
    std::string firstName;

public:

    // Default constructor
    Student();

            -----
```

```
Student::Student() : GPA(4.0), ndID(9000000000), lastName(), firstName() {}

```

#### 3. [30 points] - Given the following class Person .h and .cpp file, identify which methods in the .h and .cpp file should be declared as const, and then write how they would be declared in both the .h and .cpp files. (You only need to do the required methods, you do not need to write the entire class)

![](https://sites.google.com/a/nd.edu/morrison/courses/cse20312/lecture-notes/preview-9/Class%20Const.png?attredirects=0)

1: `getLast()`

```
// Person.h
std::string getLast() const;

// Person.cpp
std::string Person::getLast() const{
	return lastName;
{
```

2: `getFirst()`

```
// Person.h
std::string getFirst() const;

// Person.cpp
std::string Person::getFirst() const{
	return firstName;
{
```

#### 4. [25 points] - In your word document, write a Production Quality Compilation Makefile for one executable, but with two theoretical classes, where one classes is aggregated on another (family.h has #include "person.h", and classTest.cpp has "family.h"). (You do not need to create any of these files).

* Folder: ~/DSInClass/09-Classes
* Executable 1: classTest
* Main File: classTest.cpp
* Library 1 Declarations: family.h
* Library 1 Definition: family.cpp
* Library 2 Declarations: person.h
* Library 2 Definitions: person.cpp

```
#G++ is for the GCC compiler for C++
PP := g++

# GCC is the compiler for C.
CC := gcc

# CFLAGS are the compiler flages for when we compile C code in this course 
FLAGS := -O0 -g -Wall -Wextra -Wconversion -Wshadow -pedantic -Werror -lm
CXXFLAGS := -m64 -std=c++11 -Weffc++ $(FLAGS) 
CFLAGS := -std=c11 $(FLAGS)

# Variables for Folders
09 := ~/DSInClass/09-Classes

# classTest
# Command: make classTest
classTestObjs :=  $(09)/classTest.o $(09)/family.o $(09)/person.o

classTest: $(classTestObjs) 
	$(PP) $(CXXFLAGS) -o $(09)/classTest $(classTestObjs)

classTest.o: $(06)/classTest.cpp
	$(PP) $(CXXFLAGS) -c $(09)/classTest.cpp	
	
family.o: $(09)/family.cpp $(09)/family.h
	$(PP) $(CXXFLAGS) -c $(09)/family.cpp
	
person.o: $(09)/person.cpp $(09)/person.h
	$(PP) $(CXXFLAGS) -c $(09)/person.cpp
	
# Make all
all: classTest

# Make clean
clean :
	rm -rf *.o classTest
```