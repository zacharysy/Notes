# Chapter 3: Algorithms
## Properties
* Input
* Output
* Correctness
* Finiteness
* Effectiveness
* Generality


## Searching
### Linear Search
* Search linearly

### Binary Search
* Better than linear search

## Sorting
### Bubble Sort
* Exactly what it sounds like
* sort pairs of elements

### Insertion Sort
* Exactly what it sounds 
* Start with array with first two elements then sort, and then sort the next element, etc


## Big-O
* Worst Case
* Upper Bound
* There exists $k,C\in\mathbb{R}$ such that
	* $$x>k \implies f(x) \leq Cg(x)$$

### Some properties
* If $f_1\in O(g_1)$ and $f_2 \in O(g_2)$
	* $(f_1 + f_2) \in O(\max{g_1,g_2})$
	* $(f_1f_2) \in O(g_1g_2)$

## Big Omega
* Best Case
* Lower Bound
* There exists $k,C\in\mathbb{R}$ such that
	* $$x>k \implies f(x) \geq Cg(x)$$

### More Properties
* $$f\in O(g) \iff g\in\Omega(f)$$

## Big-Theta
* Average Case
* Bounded
* There exists $k,c_1,c_2\in\mathbb{R}$ such that
	* $$x>k \implies c_1 g(x) \geq f(x) \geq c_2 g(x)$$

### Smore propertires
* $$f\in \Theta(g) \iff g\in\Theta(f)$$


## Algorithm Complexity
