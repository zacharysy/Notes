## Zachary Sy<br>Lecture 6

### Part 1: Objectives
* using new, create an integer pointer and allocate an int array with an even length
* print all the elements of the array
* iterate through the array. Pass i and i+1 to a function and swap them
* Print all the elements of the array to check for successful swaps

### Part 2: Identify Risks and Alternatives
* Risk: Need to pass more than one value to the function
* Alternatives: Pass by reference or Call by reference
* Risk: Cannot use a temporary variable in swap function
* Alternative: Use math

#### Part 3: Product Development and Testing
* For coding simplicity, we will use the new/delete to allocate and free the array
* For printing the array, we will pass by reference since we are passing an integer pointer
* For coding simplicity, we will call by reference to sway the variables in the array