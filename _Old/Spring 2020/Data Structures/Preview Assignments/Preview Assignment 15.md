## Zachary Sy<br>Preview Assignment 15

#### 1. [15 points] - Video 2:17-4:04 and Slides 5-7 - In your own words, describe the three different ways of relating object types.

There are three ways to describe object relationships. The first one is "Uses a", which is when an object uses another object by calling a public method of that object. The next way is "Has a", which is when an object has a property and method, and is implemented with composition. The last way is "Is a", which is done using inheritance, where one object is a more specialized version of another object.

#### 2. [15 points] - Video 4:05-7:52 and Slides 8-10 - In your own words, describe the differences between a base class and a derived class.

A base class is a more general class and contains all that is common among its derived classes. Derive classes are more specialized and use, expend, modify, or replace base class behaviors. Anywhere a base class is used, the derived class can be used but not vice versa.

#### 3. [40 points] - Video 7:53-23:15 and Slides 11-18 - State and describe the first 8 rules for Inheritance and Polymorphism

When designing a base and derived class, adhere to the following rules. 

1. the base class requires a destructor with the virtual keyword in the .h file. The virtual function is a member function which is declared within a base class and is redefined by a derived class. If the base class does not require a destructor, then a copy or assignment operator is not needed
2. Any private members or methods in the base that can be accessed by the derived class must have a protected keyword
3. In the derived class declaration, the format is `class derived: public base`
4. If the base class is templated, then the class definition of the derived class must be templated
5. For private members or methods in the derived class, you only need to add members that are unique to the derived class
6. For the constructor, you should use the constructor for the base class as one of the arguments for the member initialization list
7. The derived class must have a destructor, even if the derived class does not have a pointer as a member. If the derived class destructor does not have a pointer, a copy and assignment is not necessary. No virtual keyword is needed in the derived class unless it is a base class for another class
8. You must write new friend methods since the friend method depends on the specific class you are passing to it



#### 4. [20 points] - Video 23:16-25:50 and Slide 19 - In your texting editing document, write a Production Quality Compilation Makefile for one executable, but with seven theoretical classes. The base class is Animal (Animal.cpp and Animal.h). The two derived classes from Animal are Pet and Wild (Both have .cpp and .h files). The two classes that are derived from Pet are Cat and Dog (Both have .cpp and .h files). Finally, the two derived classes from Wild are Rhino and Walrus.

```
# Author: Zachary Sy
# E-mail: zsy@nd.edu
#
# This is the Makefile for the CSE 20312 course Lecture 15

# G++ is for the GCC compiler for C++
PP := g++

# CXXFLAGS are the compiler flages for when we compile C++ code in this course 
FLAGS := -O0 -g -Wall -Wextra -Wconversion -Wshadow -pedantic -Werror 
CXXFLAGS := -m64 -std=c++11 -Weffc++ $(FLAGS) 

# Variables for Folders
15 := ~/cse20312/15-Inheritance
CLASSES := $(15)/classes
PROG := $(15)/programs
OBJECTS := $(15)/objects
EXE := $(15)/executables


# Command: make Animal
AnimalObjs := $(OBJECTS)/Animal.o $(OBJECTS)/Pet.o $(OBJECTS)/Wild.o  $(OBJECTS)/Cat.o $(OBJECTS)/Dog.o $(OBJECTS)/Rhino.o $(OBJECTS)/Walrus.o

Animal: $(AnimalObjs)
	$(PP) $(CXXFLAGS) -o $(EXE)/Animal $(AnimalObjs)
	$(EXE)/./Animal


# Base class
$(OBJECTS)/Animal.o: $(PROG)/Animal.cpp $(CLASSES)/Animal.h
	$(PP) $(CXXFLAGS) -c $(PROG)/Animal.cpp -o $@

# Derived Classes 1
# Wild inherits Animal
$(OBJECTS)/Wild.o: $(CLASSES)/Wild.cpp $(CLASSES)/Wild.h $(CLASSES)/Animal.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Wild.cpp -o $@

# Pet inherits Animal
$(OBJECTS)/Pet.o: $(CLASSES)/Pet.cpp $(CLASSES)/Pet.h $(CLASSES)/Animal.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Pet.cpp -o $@

# Derived Classes Pet 
# Cat inherits Pet
$(OBJECTS)/Cat.o: $(CLASSES)/Cat.cpp $(CLASSES)/Cat.h $(CLASSES)/Pet.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Cat.cpp -o $@

# Dog inherits Pet
$(OBJECTS)/Dog.o: $(CLASSES)/Dog.cpp $(CLASSES)/Dog.h $(CLASSES)/Pet.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Pet.cpp -o $@	
	
# Derived Classes Wild
# Rhino inherits Wild
$(OBJECTS)/Rhino.o: $(CLASSES)/Rhino.cpp $(CLASSES)/Rhino.h $(CLASSES)/Wild.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Rhino.cpp -o $@

# Walrus inherits Wild
$(OBJECTS)/Walrus.o: $(CLASSES)/Walrus.cpp $(CLASSES)/Walrus.h $(CLASSES)/Wild.h
	$(PP) $(CXXFLAGS) -c $(CLASSES)/Walrus.cpp -o $@	


# Make all
all: Animal

# Make clean
clean :
	rm -rf *.o $(OBJECTS)/* $(EXE)/*
```