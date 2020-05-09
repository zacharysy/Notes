# Different Faces of Linear Systems
## One Form
$$\left\{\begin{matrix}
a_{11}x_1+\cdots+a_{1n}x_n = b_1 \\
\vdots \\
a_{m1}x_1+\cdots+a_{mn}x_n = b_m \\
\end{matrix}\right .$$

## Same thing with Matrices
* $A=(a_{ij})^{m~~~~n}_{i=1~j=1}$
* $\mathbf{x}$ is a vector in $\mathbb{R}^n$
* $\mathbf{b}$ is a vector in $\mathbb{R}^m$
* Solve $A\mathbf{x=b}$

# Solution of a linear system. Echelon and reduced echelon forms

## Gauss-Jordan Elimination, Row Reduction
### Idea
* Design a few "elementary transformations" and use them to simplify your system

## Elementary Transformations
### Row Exchange
* Permute two equations

### Scaling
* Multiply equation by nonzero constant

### Row Replacement
* Add a multiple of an equation to another equation

## Row Operations
* Define an "extended matrix" $$\tilde{A}=[A|\mathbf{b}]$$
	* Permute rows of $A$
	* multiply a row by a nonzero scalar
	* add a multiple of an equation to another row


## Operations as Matrices
* Multiply $\tilde{A}$ on the left by

### Row Exchange
* Just an identity matrix with $0$ s in the diagonal of the two rows that are to be permuted
/rowExchange.png

### Scaling
* Identity matrix where in the diagonal at the row to scale it's a constant $a$ instead of a $1$
/scaling.png

### Row Replacement
* Identity matrix $$\mathbb{I}n+aE_{j,k}$$ where $E_{j,k}$ is the zero matrix with a $1$ at row $j$ and column $k$
* Also equivalent to that bottom thing, which is identity matrix with an extra $a$ at $k,j$
/rowReplacement.png

### Invertibility of Elementary Transformations
* Any invertible matrix can be made from composition of elementary transformations

## Row Reduction
### Steps/Algorithm
1. Find the leftmost column of $\tilde{A}$ such that it is not all zero
2. In that column, find the first nonzero entry ($i\text{th}$ row)
3. permute the first row and the $i\text{th}$ row so that the first row is a nonzero entry called the **pivot**
4. Murder all nonzero entries below the pivot by adding and subtracting appropriate multiples of the pivot
5. Apply same steps to the rows below pivot

### Row Echelon Form
* Result of applying the row reduction algorithm
* Has same size as the original $\tilde{A}$
* $$\begin{pmatrix}
0 & \cdots & 0 & * & x & x & x & x & \cdots \\
0 & \cdots & 0 & 0 & 0 & * & x & x & \cdots \\
0 & \cdots & 0 & 0 & 0 & 0 & * & x &\cdots \\
\end{pmatrix}$$
* If echelon form has any pivots on the last column, then there is no solution
	* Since then a nonzero number equals zero

### Reduced Echelon Form
* Make all pivots equal to $1$, and everything above pivots $0$
* From the bottom, kill all entries above pivots

## Analyzing the Echelon Form
* If there is a row of the form $(0,\cdots,0|*)$, then there is **no solution**
* If there is a pivot is every column, then the solution is **unique**
* If there is a column without a pivot, then there are **infinitely many solutions**

### Inverses
* Since with row reduction $$(E_n\cdots E_2 E_1)A\mathbf{x}=(E_n\cdots E_2 E_1)\mathbf{b}$$ is equivalent to $$\mathbb{I}\mathbf{x}=(E_n\cdots E_2 E_1)\mathbf{b}$$
* Then row reduction finds an inverse

## Corollaries about linear independence and bases. Dimension.
### Implications
* If there is a pivot of every row, then a solution exists for every $\mathbf{b}$
* If there is a pivot in every column then the solution is unique
*  Solution exists for any $\mathbf{b}$ an is unique iff there exists a pivot in every row in column implies $m=n$ and $A$ is invertible

### Another Perspective
* $\mathbf{v_1,\cdots,v_n}\in\mathbb{R}^m$
* Can we find a linear combination $x_1\mathbf{v_1},\cdots,x_n\mathbf{v_n}$ such that it is equal to a fixed constant $\mathbf{b}\in\mathbb{R}^m$
	* $A = [\mathbf{v_1},\cdots,\mathbf{v_n}] \iff A\mathbf{x+b}$ 

#### Implications
* If for every constant $\mathbf{b}$ there exists a solution, then complete
* Solution for every column gives linearly independence
* Pivot on every row and column implies that the set of vectors is a basis

### Proposition 3.2
* Any basis in $\mathbb{R}^m$ must contain $m$ vectors

### Dimension (Proposition 3.3)
* Any basis in $V$ has the same number of vectors in it
* This number is called the **dimension** in $V$

## Corollaries about invertible matrices.
* $A - m\times n$  can be invertible only if square 
* An $n \times n$ $A$ is invertible iff its reduced echelon form is $\mathbb{I}_n$

# Finding $A^{-1}$ by Row Reduction
* $$A^{-1}=[\mathbf{x_1},\cdots,\mathbf{x_n}]$$
* $$A\mathbf{x}_i=\mathbf{e}_i$$
* So $$\tilde{A}=[A | \mathbf{I}_n]$$
* by elementary matrix, transform to
* $$[\mathbf{I}_n |A^{-1}]$$

## Corollary 
* Any invertible matrix is a product of elementary matrices

# Dimension. Finite-dimensional spaces.
## Subspaces
* $V$ is a finite dimensional vector space
* $W\subset V$ implies $\dim{W}\leq\dim{V}$ 
	* and in the case $\dim{W}=\dim{V}$, then $W=V$
* Suppose $\mathbf{v_1,\cdots,v_r}$ is a linearly independent system of vectors, then it can be extended to a basis in $V$
	* If the system is not generating, adding more elements while still being linearly independent will eventually make it a basis

# General Solutions of a Linear System
## General Solution of $A\mathbf{x}=\mathbf{b}$
* $A\mathbf{x}=\mathbf{0}$ is called a homogeneous linear equation
	* Has at least one solution
* Denote by $W=\{\text{ all solutions of } A\mathbf{x}=\mathbf{0}\}$
	* $W$ is a subspace in $\mathbb{R}^n$
* Let $\mathbf{b}$ be any vector in $\mathbb{R}^m$
* Let $\mathbf{x_1,x_2}$ be two solutions of $A\mathbf{x}=\mathbf{b}$
	* Then $A(\mathbf{x_1-x_2}) = \mathbf{0}$
* A general solution of $A\mathbf{x}=\mathbf{b}$ is of the form $$\mathbf{x=x_{\text{part}}+x_{h}}$$
	* $x_{\text{part}}$ is an arbitrary solution of $A\mathbf{x}=\mathbf{b}$
	* $x_{h}$ is the general solution of $A\mathbf{x}=\mathbf{0}$

# Fundamental Subspaces of a Matrix. Rank
* Let $A:V\rightarrow W$ be a linear transformation between two finite dimension vector spaces.

## Kernel
* $$\text{Ker } A = \{\mathbf{v}\in V: A\mathbf{v}=0\}$$
* Dimension of kernel is given by number of free variables in echelon form of $A$
* Subspace of $V$


## Range/Image
* $$\text{Ran } A = \text{Col } A =\{\mathbf{w}\in W: \exists \mathbf{x}\in V \text{ such that } A\mathbf{x}=\mathbf{w}\}$$
* Subspace of $W$ spanned by the columns of $A$
* Any column of $A_e$ can be written as a linear combination of the pivot columns
* Pivot columns are linearly independent

## Row Space
$$\text{Row } A = \text{Col } A^T$$
* The rows of $A$

## Transposition
* If $A$ is represented by a matrix, then $A^T$ is also a matrix. We can define in a similar way $\text{Ker } A^T$ and $\text{Ran } A^T$
	* The basis of the range is the nonzero rows of the echelon form of $A$
* Instead of using $A^T$, can consider $$\mathbf{x}A=\mathbf{b}$$

## Rank
* $$\text{rank } A := \dim{\text{Ran }A}$$
* Can be found through row reduction because **the number of pivots in echelon form is equal to the rank** of $A$

## Observations
* $\dim{\text{Ker } A} + \dim{\text{Ran } A} = \dim{V}$
* $\dim{\text{Ker } A^T} + \dim{\text{Ran } A^T} = \dim{W}$

## Finding Basis in Range of $A$
* In a Reduced Echelon Form, the columns that contain pivots are a basis in $\text{Ran } A_{\text{red}}$
* where $A_{\text{red}}$ is $A$ in Reduced Echelon Form

### To get reduced echelon form
* $$A\mathbf{x} = \mathbf{b}$$
* $$EA\mathbf{x} = E\mathbf{b}$$ 
* $EA$ is the reduced echelon form

### Getting the basis of $A$
* $E^{-1}(\text{basis of } \text{Ran } A_{\text{red}})$ gives a basis in $A$

### Basis of Kernel of $A$
* the basis is the columns of the echelon form without pivots

### Basis of Column Space
* The basis is the columns of $A$ where the echelon form has a pivot

### Conclusion
* A basis in $\text{Ran } A$ is given by columns of $A$ in which the pivot elements of $A_{\text{red}}$ are contained
	* Just get reduced echelon form and columns of that are the basis of $A$

## Rank Theorems
### The Rank Theorem (Theorem 1)
* $$\text{rank }A = \text{rank }A^T$$
* The column rank of a matrix coincides with its row rank

### Theorem 2
* A $m\times n$ gives linear transformation $A:\mathbb{R}^n\rightarrow\mathbb{R}^m$
* $$\dim{\text{ker }}A + \text{rank }A = n$$
* $$\dim{\text{ker }}A^T + \text{rank }A = m$$

### Theorem 3
* The equation $A\mathbf{x}=\mathbf{b}$ has a solution $\mathbf{x}$ for all $\mathbf{b}\in\mathbb{R}^m$ iff $$\text{ker }A^T=\{\mathbf{0}\}$$ 
	* So $A^T$ is injective


## Completion of a linearly independent system to a basis
* Any linearly independent system can be made complete by adding in more linearly independent vectors

### Method
1. Form a matrix with the transpose of the linearly independent vectors
	* the vectors are rows to the matrix
2. Reduce to echelon form
3. Then add vectors as rows with a $1$ at a column with free variable (basically slotting in standard vectors with columns missing pivots)
4. These additional rows (transposed) and the original vectors are also a basis in $\mathbb{R}^n$

# Representation of a linear Transformation in arbitrary bases. Change of coordinates formula

## Coordinate Vector
* Let $V$ be a vector space with basis $B=\{\mathbf{b}_1,\cdots,\mathbf{b}_n\}$
* Coordinates are relative to $B$
* all $\mathbf{v}\in V$ has a unique representation as a linear combination of the bases
* $$\mathbf{v}\rightarrow [b_1,b_2,\cdots,b_n]^T$$
* implies that the coordinate vector
* $$\mathbf{[v]}_{\mathcal{B}}=[b_1,b_2,\cdots,b_n]^T$$

### In another basis
* Since bases are not unique, then let $A$ be another basis then
* $$\mathbf{[v]}_{\mathcal{A}}=[a_1,a_2,\cdots,a_n]^T$$

## Matrix of a Linear Transformation
* Let $T:V\rightarrow W$ such that $V$ is relative to basis $\mathcal{A}$ and $W$ relative to basis $\mathcal{B}$
* This matrix which sends a coordinate vector to another coordinate basis is called $T_{\mathcal{BA}}$
* $$[T(\mathbf{v})]_{\mathcal{B}}=[T]_{\mathcal{BA}}[\mathbf{v}]_{\mathcal{A}}$$

## Change of Coordinate Matrix
* Consider the identity transformation $\mathbb{I}$ and the matrix $\mathbb{[I]}_{\mathcal{BA}}$ so
* $$[\mathbf{v}]_{\mathcal{B}}=\mathbb{[I]}_{\mathcal{BA}}[\mathbf{v}]_{\mathcal{A}}$$

### Example
* If $$[\mathbf{a}_j]_{\mathcal{B}}=[\mathbb{I}]_{\mathcal{BA}}[\mathbf{a}_j]_{\mathcal{A}}$$
* Then since the resulting vector is just the $j$ th column of the identity function, then $[\mathbf{a}_j]_{\mathcal{B}}$ is the $j$ th column of the identity matrix

### To compute $[\mathbb{I}]_{\mathcal{BA}}$
* Find coordinate vectors of the vectors in $\mathcal{A}$ relative to $\mathcal{B}$ and arrange them as columns of $[\mathbb{I}]_{\mathcal{BA}}$

### Inverse
* If $$[\mathbf{v}]_{\mathcal{A}}=[\mathbb{I}]_{\mathcal{AB}}[\mathbf{v}]_{\mathcal{B}}$$
* then $[\mathbb{I}]_{\mathcal{AB}}=([\mathbb{I}]_{\mathcal{BA}})^{-1}$

### Using Standard Basis
* let $S$ be the standard basis and $B$ be another basis
* $$\mathbb{I}_{\mathcal{SB}}=[\mathbf{b_1|b_2|\cdots|b_n}]$$

## Matrix of a transformation and change of coordinates
* Let $T:V\rightarrow W$ with $A,\tilde{A}$ being two bases in $V$ and $B,\tilde{B}$ two bases in $W$ 
* $$[T]_{\mathcal{\tilde{B}\tilde{A}}}=[\mathbb{I}]_{\mathcal{\tilde{B}B}}[T]_\mathcal{BA}[\mathbb{I}]_\mathcal{A\tilde{A}}$$

## Why Change Coordinates
* Changing bases in target/source spaces can simplify how the matrix of a linear transformation looks like
	* by taking original $m\times n$ $T$ and multiply on the left by an invertible $m\times m$ matrix and on the right by an invertible $n\times n$ matrix


### How Simple can the result be
* $T \rightarrow Q T R$
	* Can use $Q$ to transform to reduced echelon form with row reduction
	* Can use $R$ to perform elementary operations on the columns
		* can use pivots to make all nonzero entries to the right of the pivot equal to $0$

### Theorem
* Any $m\times n$ matrix can be reduced via a change of basis in the source and target spaces form
	* $$\begin{pmatrix}\mathbb{I}_r & 0 \\ 0 & 0\end{pmatrix}$$
	* where $r$ is the rank

## Similarity Transformation
* $T:V\rightarrow V$, we want to replace $T_{\mathcal{A,A}}$ with $T_{\mathcal{B,B}}$
	* $$T_{\mathcal{B,B}}=T_{\mathcal{B,A}}T_{\mathcal{A,A}}T_{\mathcal{A,B}}$$
* which is 
	* $$T_{\mathcal{B,B}}=Q^{-1}T_{\mathcal{A,A}}Q$$
* $T\rightarrow Q^{-1}TQ$ is called a similarity transformation

### Properties
* $\text{Trace } Q^{-1}TQ = \text{Trace } Q^{-1}QT = \text{Trace } T$
* $\text{Trace } (Q^{-1}TQ)^k = \text{Trace } T^k$

### Conclusion
* For $T$ and $T_1$ to be similar, $$\text{Trace } T^k = \text{Trace } T_1^k$$