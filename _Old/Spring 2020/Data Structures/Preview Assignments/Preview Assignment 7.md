## Zachary Sy<br>Preview Assignment 7

#### 1. Given the following code example
```
#include <iostream>

float recurFunc(float f1, int y){

    if(y == 0){
        return 1;
    }

    return f1 * recurFunc( f1 / (float)2, y - 1);
}

int main(void){

    std::cout << recurFunc( (float)5, 2 );

}
```

##### a) Write a Recursive Trace as shown in the Lecture video (Compare to factorial recursion)
|Iteration| `f1` | `y` |
|:----- |:-----|:---|
| 0      |     5   |  2  |
| 1|2.5|1|
|2|1.25|0|


##### b) Correlate the code and results with the formal definition of Recursion (Similar to Slide 9)
* **Base Case**
	* `if(y == 0){ return 1; }`
* **Recursive Case**
	* `return f1 * recurFunc( f1 / (float)2, y - 1);`
* **Overall Definition**
	* $X=\{5, 2.5, 1.25\}, y=0$

#### 2. Combining Concepts: Given the following code example
```
#include <iostream>

int recurFunc2(int* intArr, int a, int b){

    if(a == b){
        return intArr[a];
    }
        
    else if(b - a == 1){
        if( intArr[a] > intArr[b] ){
            return intArr[a];
        }
        return intArr[b];
    }

    int c = (a + b) / 2;

    int d = recurFunc2( intArr, a, c );
    int e = recurFunc2( intArr, c+1, b );

    if( d > e )
        return d;

    return e;
}

int main(void){

    int* intArr = new int[5];
    *(intArr + 0) = 13;
    intArr[1] = 22;
    intArr[2] = 9;
    *(intArr + 3) = -7;
    intArr[4] = 10;

    std::cout << recurFunc2( intArr, 0, 4 ) << std::endl;

    return 0;
}
```

##### a) write the Binary Recursive Trace as shown in the Lecture video. 

* `recurFunc2(intArr, 0, 4)`
	* `d = recurFunc2(intArr, 0, 2)`
		* `d = recurFunc2(intArr, 0, 1)`
			* `return 22`
		* `e = recurFunc2(intArr, 2, 2)`
			* `return 9`
		* `return 22`
	* `e = recurFunc2(intArr, 3, 4)`
		* `return 10`
	* `return 22`

##### b) Correlate the code and results with the formal definition of Recursion (Similar to Slide 9)
* **Base Case**

	 ```
	 if(a == b){
        return intArr[a];
    }
        
    else if(b - a == 1){
        if( intArr[a] > intArr[b] ){
            return intArr[a];
        }
        return intArr[b];
    }
    ```
    
    and 
    
    ```
    if( d > e )
        return d;
    
    return e;
    ```

* **Recursive Case**

```
    int c = (a + b) / 2;

    int d = recurFunc2( intArr, a, c );
    int e = recurFunc2( intArr, c+1, b );
```


* **Overall Definition**
	* $X=\{22, 9,10\}$, `a==b` or `b-a==1` 