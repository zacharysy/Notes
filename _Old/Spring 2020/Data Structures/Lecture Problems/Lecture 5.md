## Zachary Sy<br>Lecture 5

### Problem 1
#### Part 1
`void * floatArr = malloc(floatArrSize*sizeof(float))`

#### Part 2
`long unsigned int` Allocates the entire memory address

### Problem 2
```
long unsigned int doubleSize = 10;
void* voidPtr = malloc(doubleSize*sizeof(double))
double* doublePtr = (double*)malloc(doubleSize*sizeof(double))
double* doubleNew = new double[doubleSize]

```

### Problem 3
```
std::cout << (void *)&dblArray;
std::cout << dblArray;
std::cout << (dblArray+1);
std::cout << dblArray[5];
```