## Zachary Sy<br>Preview Assignment 6

### 1. Review the description of the getLetter program. Describe, in your own words and in detail, what is going on in the program. Include a description of the stack, stack pointer, heap, and registers.

The `word` parameter is passed by reference, and takes in a pointer of a `char` array. `wordSize` and `findChar` are passed by value, Lastly in the function definition, `currLetter` is a pointer to an address of an integer. Inside the function is a `for` loop that tries to find a specific letter. The loop variable `i` is cast from a `long unsigned int` to an `int` and `currLetter` is set to the value of `i`.

In terms of data structures, a copy of the `getLetter` code is pushed to the stack. Then the stack pointer is updated to point to `getLetter`. When memory is allocated in the stack, a register for `word` points to the same memory location in the heap as the argument passed to it. Next, `long unsigned int wordSize` is given a register and set to a value. The same thing is done to `findChar`. For `curLetter`, this register points to the register of the argument that is passed to it. Next, the `for` loop is pushed to the stack and iterated. `word[i]` is compared to `findChar` until equality, at which the register pointed to by `curLetter` and that register is updated to the value at the register of `i`. `return` then pops `for` and `getLetter` from the stack, along with all the registers allocated to their local variables.

#### 2. Describe, in your own words, the difference between pass by reference and call by reference.

Pass by reference is legacy by C. Call by Reference abstracts away pointer complexity. In Call By Reference, `&` can be used for the variable for the function declaration. There is also no need to declare another pointer register. In Pass by Reference


#### 3. Given the following code segment, where the register address locations of the following are:

```
floatX is at 0x6b77c 
floatY is at 0x6b77e
ptrX   is at 0xab21d
ptrY   is at 0xab21f
```

State the output of the following code segment:

```
#include <iostream>

void func1(float* tempX, float* tempY){
 
 std::cout << &tempX << " " << &tempY << std::endl;
 std::cout << tempX << " " << tempY << std::endl;
 std::cout << *tempX << " " << *tempY << std::endl;

}

void func2(float& tempX, float& tempY){

 std::cout << &tempX << " " << &tempY << std::endl;
 std::cout << tempX << " " << tempY << std::endl;

}

int main(){

 float floatX = (float)3.2;
 float floatY = (float)-2.7;
 float *ptrX, *ptrY;
 
 ptrX = &floatX;
 ptrY = &floatY;
 
  func1(ptrX, ptrY);
 
 func2(tempX, tempY);
 
 return 0;
}
```

##### **Output:**

```
0xab21d 0xab21f
0x6b77c 0x6b77e
3.2 -2.7
0x6b77c 0x6b77e
3.2 -2.7
```