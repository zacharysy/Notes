## Zachary Sy<br>Preview Assignment 14

#### 1. [50 points] - Similar to the problems from Video 1:36-11:37 and Slides 5-13 - A retail company is designing a program that determines how many items are purchased. The corporate office will change the types and total number of items sold (for holidays or different times of year), but they need to figure out what items sell best on given days, and if those items drive customers to purchase other items in the store. Each item has a unique ID, but the IDs are dictated by the item vendor, so the ID ordering is out of the control of the retail company. Design a function that updates the total number of a given item whenever an item is purchased, can rapidly determine the number of items sold with a given ID, as well as which item is the best selling.
	
##### Identify Objectives
* Store product IDs and number of items sold
* Receive an ID as an input
* Determine the right number of items sold based on ID
* Modify the number sold based on input 
* Determine the product with the most sold

##### Risks and Alternatives
* Risk: The format of the IDs are not known (Is it just integers, are they alphanumeric, UUIDs, or any miscellaneous symbols)
	* Alternative: Store the ID as an `std::string` since any type of ID can be stored as a string
* Risk: A wrong ID might be given or misspelled
	* Alternative: Do checking to make sure the given ID has an associated product
* Risk: There is no mention of products possibly being returned
	* Alternative: Assume products can be returned so a negative number of items sold is theoretically possible, which means the data must be stored in a signed integer

##### Development and Testing
* Create three functions, `purchaseItem`, `amountSold`, and `bestSeller` to perform  the three operations described in the problem statement
* The arguments of `purchaseItem` and `amountSold` are a hash map of type `<std::string, int>` called `inventory` and `std::string` ID. `bestSeller` just takes in `inventory` as input
* `purchaseItem` finds the product in `inventory` with the given ID and increments the associated `int`
* `purchaseItem` finds the product in `inventory` with the given ID and returns the associated number of items sold
* `bestSeller` iterates through the key value pairs and keeps track of the ID and amount of the product with the greatest amount sold

	
####  2. [50 points] - Similar to the problems from Video 11:38-18:02 and Slides 14-22 - Given a Dynamic Array, design a function that removes all elements from that Array.

##### Identify Objectives
* Iterate through the elements in a dynamic array
* for each element, remove it from the array

##### Risks and Alternatives
* Risk: How to be sure all the elements are deleted
	* Argument: Keep deleting until the size of the array is $0$

##### Development and Testing
* Create a while loop with condition `arr.size() > 0`
* Inside the loop, use `arr.erase(arr.begin())` to remove the head of the array