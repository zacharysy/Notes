## Zachary Sy<br>Preview Assignment 20

#### 1. Given a circular linked list, implement an algorithm which returns node at the beginning of the loop

##### Identify Objectives
* Starting from the head, traverse each node of the linked list and keep track of visited node
* If a node is reached that has been visited, return that node

##### Risks and Alternatives
* Risk: How to store visited nodes???
	* Alternative: Use a hash table (`std::unordered_map`) so it has $O(1)$ retrieve 
* Risk: How to identify nodes????
	* Alternative: Use the node's memory address

##### Development and Testing
* Given a linked list, get the head node
* Place memory address of head node into hash table
* go to next node from head node and see if it is in the hash table
* If it is not in the hash table, put it in
* If it is in the hash table return the next node

**Testing**

![](https://sites.google.com/a/nd.edu/morrison/courses/cse20312/lecture-notes/preview-20/Updated%20Linked%20List.png?attredirects=0)

* Visited: 1
* Visited: 1,2
* Visited: 1,2,3
* Visited: 1,2,3,4
* Visited: 1,2,3,4,5
* Visited: 1,2,3,4,5,2
* Visited: 1,2,3,4,5,6,2
	* Already visited 2, so return node 2


#### 2. Given a circular linked list, implement an algorithm which returns node at the beginning of the loop, where you may not use an additional Advanced Data Structure, such as a Hash Table. (You may use simplified structures, like node pointers)

##### Identify Objectives
* Starting from the head, traverse each node of the linked list and keep track of visited node
* store the next node as the current node, and remove the next node from the head node
* check if the current node is pointing to null, if it isn't, store the next node as the current node and remove the pointer of the previous node
* keep going until a node with null is reached, which is the end of the node 

##### Risks and Alternatives
* Risk: This breaks the linked list
	* Alternative: I was just told to find the node at the beginning of the loop, so don't care about breaking the linked list
* Risk: How to store the next node while deleting the pointer to it from current node
	* Alternative: store next node in a temp variable, then delete its pointer in current, and then overwrite current

##### Development and Testing
**Testing**

![](https://sites.google.com/a/nd.edu/morrison/courses/cse20312/lecture-notes/preview-20/Updated%20Linked%20List.png?attredirects=0)

* **1** -> 2 -> 3 -> 4 -> 5 -> 6 -> 2 -> 3...
* 1  **2** -> 3 -> 4 -> 5 -> 6 -> 2 -> 3...
* 1  2  **3** -> 4 -> 5 -> 6 -> 2   3...
* 1  2  3  **4** -> 5 -> 6 -> 2  3...
* 1  2  3  4  **5** -> 6 -> 2  3...
* 1  2  3  4  5  **6** -> 2  3...
* 1  2  3  4  5  6  **2**  3... 
	* **2** Isn't pointing to anything


