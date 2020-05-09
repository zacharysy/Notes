## Zachary Sy<br>Preview Assignment 11
#### 1. [15 points] - In your own words, describe the difference in advice often given from industry representatives regarding data structures (as personified by the difference between Stephen Maderak and Nick Aiello), and then why we teach the Data Structures course with both "building your own" and "using the standard template libraries".

Some industry representatives say to not reinvent the wheel and trust standard libraries, while others say that  knowledge of data structures from scratch is also important. The Data Structures course is meant to allow us to be comfortable with both using the standard library and creating our own data structures.

#### 2. [15 points] - In your own words, describe what is going on in the following part of the code segment:

```
std::vector< float > floatVec( 5, (float)3.14159 );

for(float& a : floatVec){
        std::cout << a << std::endl;
}
```

The code segment initializes an `std::vector<float>` called `floatVec` that has `5` elements all with a value of `3.14159`. These values are then printed on the command line.

####  3. [70 points] Note: This is the exact same problem as given in the slide set. The way you can get the most benefit from this problem is to attempt it first after watching the video, but then trying it independently. If you get part or all of the problem wrong, write the concept error as d) Planning the Next Phase, and then write a second spiral, writing only the parts of the Identify Objectives, Identify Risks and Alternatives, and Product Development and Testing that you need for the correct answer. If you do the second spiral, you will get full credit for your solution, while getting an opportunity to learn from a mistake. The phrasing below will be identical to how it would be presented on an Exam.

For this question, you will need to state

a) Identify Objectives: Describe, in your own words, what you are trying to solve, and the computing principles you learned to implement these results

b) Identify Risks and Alternatives: Describe tradeoffs for memory (spatial and temporal) and runtime complexity. If you know an STL library that may solve your problem, state that you will use it here. You must identify both the name of the data structure and the name in the C++ STL.

c) Product Development and Testing: Describe your proposed solution, and show a test case indicating how it works.

d) Planning the Next Phase : If you discover the answer can be improved after working through it, describe the issues with your initial answer and then state your proposed improved solution. (This is here specifically so you can address an issue, and do not feel the need to erase previously wrong information)


**Problem Statement:** You are writing a checkbook balancing program. The program will read in the following for all checks that were not cashed as of the last time you balanced your checkbook

* The Check Number
* Date
* The Payer – If you are writing the check, payer should be SELF
* The Payee – If you are depositing the check, payee should be SELF
* The Amount of each Check

Using your knowledge of Data Structures, describe how you could organize a program that takes in any number of checks, and update the result of the balance, and print all the results in order

#### Identify Objectives
* We need to develop a class that represents a check
	* must contain private members for Check Number, Date, Payer, Payee, and Amount
* We need to store the checks in order
* We need to be able to perform addition and subtraction
	* Amount from the total amount
* We need to be able to print the Check class info
* We must be able to store an unknown number of cheques 

#### Risks and Alternatives
* We must allow for Dynamic Memory Allocation for all checks, and not just a standard array
* We must put them in the order we receive them
	* Cannot use a Hash Map, since they're not sorted
* To maintain accuracy for money, can't use a double or float
	* Develop a class for Money
	* Would need a `-` and `+` operator
* Need to check for SELF for Payer or Payee
	* should not be writing and depositing checks if I am not involved

#### Product Development and Testing
* We propose the use of a Dynamic Array storing a Check class
* For simplicity, we can use the `std::vector` to store elements
* We will develop a Money class with dollars and cents
	* `long signed int` for dollar
	* `int` for cents
* To print everything out, make a `friend operator<<` for Check and Money
* Since they are stored in a `std::vector`, can use smart iterator.
