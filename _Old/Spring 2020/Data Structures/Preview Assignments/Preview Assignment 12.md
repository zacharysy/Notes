## Zachary Sy<br>Preview Assignment 12
#### 1. [10 points] - Video 4:27-5:28 and Slides 8 - In your own words, describe the purpose and implementation of the C++ Standard Template Library std::pair

`std::pair` is used to associate a `Key` to a `Value`. The key must be a const since the search algorithm depends on the  Key being constant. The value can be set to anything. To access the key value pair, the format is `<object>.first` for the Key and `<object>.second` for the value.

#### 2. [10 points] - Video 8:26-11:04 and Slides 11-12 - In your own words, describe the issues students often have with implementing the [] operator in the C++ Standard Template Library std::unordered_map.

A common issue students encounter is with the `operator[]` when accessing an item not in the hash because the the function inserts a new element with the corresponding key if the key doesn't exist. 

#### 3. [20 points] - Video 11:07-15:23 and Slides 13-15 - On Slide 13, the concept of collisions in a Hash Table is discussed. In your own words, describe the following
* **[4 points] From Slide 14 - Briefly describe the two main Collision Resolution strategies**
	* One Collision Resolution strategy is to divide by a number, such as using the number of buckets as the divisor, to determine the location of the next bucket
	* Another strategy is to set the number of buckets equal to a prime number. This will reduce clustering.
* **[8 points] From Slide 14 - Describe the issues of table size in the context of risks of implementing a Hash Table**
	* Too large a table will cause a wastage of memory. On the other side of things, too small a table will cause increased collisions and eventually force rehashing
* **[8 points] From Slide 15 - Describe the use of prime numbers as an alternative of implementing table sizes in a Hash Table**
	* The number of buckets can be set to be a prime number. This will reduce clustering, particularly in large hash tables, since the only divisor of a prime number is itself and 1

#### 4. [15 points] - - Given a Separately Chained Hash Map with seven buckets, and a hash function of value%7, show the result for the insertions for the following:
14, 8, 5, 6, 7, 1, 0

1. inserts 14 to 0
2. inserts 8 to 1
3. inserts 5 to 5
4. inserts 6 to 6
5. chains 7 to 14
6. chains 1 to 8
7. chains 0 to 7


|:-|:-|:-|
|0:|14|7|0|
|1:|8|1
|2:|
|3:|
|4:| 
|5:|5|
|6:|6|

#### 5. [15 points] - - Show the process for using a Hash Table to implement Counting Sort for the following (Show the full Hash Table and the final order of the emissions):
9, 6, 7, 8, 6, 7, 9, 1, 3, 1, 9, 7


|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | | | | |1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | |1| | |1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| || | | | 1 | 1| |1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | |1|1|1|1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | |2|1|1|1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | |2|2|1|1|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count| | | | | |2|2|1|2|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count|1| | | | |2|2|1|2|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count|1| |1|| |2|2|1|2|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count|2| |1|| |2|2|1|2|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count|2| |1| | |2|2|1|3|

|:-|
|Value|1|2|3|4|5|6|7|8|9|
|Count|2||1| | |2|3|1|3|

Output: 1,1,3,6,6,7,7,7,8,9,9,9

#### 6. [30 points] - Go to Sakai->Resources->In-Class Powerpoint Slides, and open Lecture 08 - In Class. Review Slides 7-9. Now consider a scenario where you are asked to sort a set of integers. The three potential approaches are
1. Using an array containing the initial unordered set to recursively sort the values using the MergeSort algorithm we developed in Lecture 07 In Class
2. Using a Dynamic Array and developing a class method push_sort that is similar to push_back shown on the In-Class 10 Lecture Slide except we find the location in the array where the integer goes in sorted order.
	* Example: 9, 3, 7, 6, 10, 5
	* Insert 1: 9
	* Insert 2: 3, 9
	* Insert 3: 3, 7, 9
	* Insert 4: 3, 6, 7, 9
	* Insert 5: 3, 6, 7, 9, 10
	* Insert 6: 3, 5, 6, 7, 9, 10
3. Using a Hash Table to perform Counting Sort, as we have done in this lecture.

In your own words, describe the Risks and Alternatives of all three approaches.

##### First Approach
* Risk: Recursion can be slow and also memory intensive, especially for large arrays
	* Alternative: Use a for loop instead
* Risk: Merge sort is generally $\Omega(n\log n)$ time complexity 
	* Alternative: Use a timsort which has same big O but is $\Omega(n)$
* Risk: Merge sort is $O(n)$ space complexity
	* Alternative: Use a quicksort, which has $O(\log n)$ space complexity

##### Second Approach
* Risk: Assuming a new dynamic array would have to be created to store the sorted elements, this takes up a lot of memory
	* Alternative: Instead of creating a new array, reinsert the element in the same array 
* Risk: Dynamic arrays are contiguous in memory, which would be inefficient for large arrays
	* Alternative: Use a linked list for the unsorted elements, since only the head is being accessed, then insert it into a new dynamic array

##### Third Approach
* Risk: Creating a new key value pair each time a new number is found can take up a lot of time
	* Alternative: Find the maximum number and instantiating all the key value pairs with default values before sorting
* Risk: if the range of numbers are large, instantiating a lot of key value pairs would take up an unreasonable amount of memory
	* Alternative: If the range is large, create a new key value pair each time a new number is found
	* 