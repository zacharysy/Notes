## Zachary Sy<br>Preview Assignment 5

#### 1. Define and Differentiate between explicit and implict type casting

Explicit Type Casting is performed by the programmer explicitly stating the type the expression should be. Implicit Type Casting is done automatically by the compiler without programmer input. Explicit typecasting is much safer than implicit typecasting since there is no confusion about what type a certain variable is

#### 2. Given the following code segment and compiler error message, describe why each of the five errors occurs in Production Quality Compilation, and how you would resolve them

```
#include <iostream>
#include <cmath>

/********************************************
* Function Name  : main
* Pre-conditions : void
* Post-conditions: int
* 
* This is the main driver function for the program 
********************************************/
int main(void){
 
 /* Variable declarations */
 float slideFloat = 3.2;
 float smallFloat = -1.0125 * pow(2, -127);
 float largeFloat = pow(2, 127);

 return 0;
}
```

![](https://sites.google.com/a/nd.edu/morrison/courses/cse20312/lecture-notes/preview-5/floatBad.png?attredirects=0)

* **Error 1/2**
	* By default, C++ interprets decimals as doubles, and so there would be an implicit typecast when `slideFloat` and `smallFloat` are declared from `float` to `double`
	* These can be fixed by implicitly typecasting `3.2` and `-1.0125` as float
* **Error 3/4/5**
	* These errors are caused by the three variables not being used yet
	* These can be fixed by using the variables somewhere 

#### 3. Given the following code segment, state the output, and using your knowledge of how IEEE 754 data is structured, describe why the control structures evaluated the data the way that it did.

```
#include <iostream>
#include <iomanip>

/********************************************
* Function Name  : main
* Pre-conditions : void
* Post-conditions: int
* 
* This is the main driver function for the program 
********************************************/
int main(void){
 
 /* Variable Declarations */
 float x = (float)1.1, y = (float)1.2;
 double x2 = 1.3, y2 = 1.4;
 
 /* Evaluae if statements */
 if( x == y ){
 std::cout << "The statement x==y is true\n" << char(10);
 }
 else{
 std::cout << "The statement x==y is false\n" << std::endl;
 }
 
 /* This if/else will select the final else statement */
 if( x2 == y2 ){
 std::cout << "The statement x2==y2 is true" << (char)10;
 }
 else if( (y2 - x2) == 0.1 ){
 std::cout << "The statement (y2 - x2) == 0.1 is true\n";
 }
 else{
 std::cout << "Both are false!\n"; 
 
 std::cout << "If you print double with a precision of 6, it will look right, and you'll see "
 << std::setprecision(6) << y2-x2 << std::endl;
 std::cout << "But with a precision of 20, you'll see the true value of "
 << std::setprecision(20) << y2-x2 << std::endl;
 }
 
 return 0;
}
```

**Output:**

* `The statement x==y is false` (with a newline at the end)
	* Since there is no way, even in floating point decimals, that 1.1=1.2

```
Both are false!
If you print double with a precision of 6, it will look right, and you'll see 0.1
But with a precision of 20, you'll see the true value of 0.099999999999999866773
```

* `x2==y2` is obviously false
* Due to floating point errors, `y2-x2` is not exactly `0.1`, so `(y2 - x2) == 0.1` is false

#### 4. In your own words , briefly describe the three fundamental elements of a pointer, and how they are used in low-level languages like C++

   1. The address of the register is the memory location containing the pointer
   2. The register contains the address of the location in the heap where a larger piece of data starts
   3. The piece of information in that location is the value the pointer is pointing at

#### 5. In your own words and in detail, describe a void pointer. 

Since all data is just stored in bits, pointers don't need to be a specific data type since the "memory type" is ultimately void. Thus, a void pointer can point to any value of any data type since it is just storing a memory address. Though, accessing the value requires a typecast since the pointer itself does not know what type the value being stored in the address is.

#### 6. Type a code segment into your Word Document that performs the following using Production Quality Compilation. 

- Define a float variable floatVar equal to 2.7
- Allocate a register as a float pointer
- Set the float pointer equal to your variable.
- Print the address of the float pointer.
- Print the address contained by the float pointer.
- Print the value pointed to be the float pointer (simply writing std::cout << floatVar << std::endl; is not sufficient for credit)

```
#include <iostream>

int main(void){
	float floatVar = (float) 2.7;
	float *p;
	
	p = &floatVar; 
	
	std::cout << &p << std::endl;
	std::cout << p << std::endl;
	std::cout << *p << std::endl;	
}
```