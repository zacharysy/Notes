# Advanced Spectral Theory

## Conjugation/Similarity Transformation
* $A:V\rightarrow V$
* Find a matrix $C$ 
* $$A=CDC^{-1}$$
* Best case is $D$ is diagonal

### Conjugation Equivalence
* Any $A$ is equivalent to $CAC^{-1}$

### Block Diagonalization
* if cannot be diagonalize, try to block diagonalize
* $$A \rightarrow \begin{bmatrix} A_1 & 0 & 0 \\ 0 & A_2 & 0 \\ 0 & 0 & A_3\end{bmatrix}$$
	* Where $A_i$ is $u_i\times u_i$ and has a single eigenvalue

# Preliminary Tools
# Cayley-Hamilton Theorem
* $A:V\rightarrow V$
* can compute characteristic polynomial
	* $$P_A(\lambda) = \det(A-\lambda\mathbb{I}_n)=(-1)^n\sum_{k=0}^n p_{k}\lambda^k$$
	* And so $$P_A(A)=(-1)^n\sum_{k=0}^n p_{k}A^k$$
* it ends up that $$P_A(A)=0$$

# Spectral Mapping Theorem
* $A:V\rightarrow V$
* let $P(t)$ be a polynomial
* then
	* $\sigma(P(A)) = p(\sigma(A))$

# Generalized Eigenspaces. Geometric meaning of algebraic multiplicity
## Invariant Subspaces
* $E\subset V$ is an invariant subspace for $A$ if
	* $AE\subset E$
* So this is equivalent to
	* $A^kE \subset E$
	* $p(A)E \subset E$
		* for any polynomial $p$

### Restriction to $E$
* Define a restriction to $E$, $A|_E:E\rightarrow E$
* $$(A|_E)\mathbf{v} = A\mathbf{v}~\mathbf{v}\in E$$

### Lemma 3.1
* $$P(A)|_E = p(A|_E)$$

## Block Diagonalization
* Suppose $V = E_1 \oplus \cdots \oplus E_r$
* and each $E_i$ is invariant
* Pick bases in $E_1,\cdots,E_r$ to give a basis for $V$
* then
	* $$A=\begin{bmatrix}A_1 & & \Huge{0} \\ & \ddots & \\ \Huge{0} & & A_r\end{bmatrix}$$
	* where $A_k = A|_{E_k}$
* so want to find the "smallest" invariant $E_1,\cdots,E_r$

## Generalized Eigenspaces
* $$E_\lambda=\{\mathbf{v}\in V: \exists k\in\mathbb{N}: (A-\lambda\mathbb{I})^k\mathbf{v}=0\}$$

### Properties
1. $$E_\lambda = \bigcup_{k=1}^{\infty}\text{ker}(A-\lambda\mathbb{I})^k$$
	* let $E_\lambda^{(k)}=\text{ker}(A-\lambda\mathbb{I})^k$
2. $$E_\lambda^{(k)}\subset E_\lambda^{(k+1)}$$
3. there exists a $k$ such that $$E_\lambda^{(k)}=E_\lambda^{(k+1)}$$
	* denote the smallest such $k$ by $d(\lambda)$ (depth)
	* and so $E_\lambda = E_\lambda^{(d(\lambda))}$
4. $AE_\lambda \subset E_\lambda$
	* $E_\lambda$ is an invariant subspace of $A$
5. $$(A|_{E_\lambda}-\lambda\mathbb{I}_{E_\lambda})^{d_\lambda}=0$$
6. $$\sigma(A|_{E_\lambda})=\{\lambda\}$$
7. if $E_\lambda \neq \{0\}$, then $\lambda\in\sigma(A)$


##  Theorem 3.4
* Let $\sigma(A) = \{\lambda_1,\cdots,\lambda_r\}$
* Then $$V=E_{\lambda_1}\oplus\cdots\oplus E_{\lambda_r}$$ 

### Remark
* Define $$p_i(\lambda) = \frac{1}{(\lambda-\lambda_i)^{n_i}}p_A(\lambda)$$
* Let $$q(\lambda)=p_1(\lambda)+\cdots +p_r(\lambda)$$
* If all $n_1,\cdots,n_r=1$, then $r=n$ and $$q(\lambda) = p_A'(\lambda)$$

### Lemma
* Let $B = q(A)$

#### Properties
1. $B$ is invertible
2. $BE_{\lambda_i}\subset E_{\lambda_i}$ 
3. $p_i(A)|_{E_{\lambda_i}}=0$
4. $B|_{E_{\lambda_i}}=p_i(A)|_{E_{\lambda_i}}$

## Lemma 3.7
* Let $$\mathcal{P}_i=B^{-1}p_i(A)$$

### Properties
1. $$\mathcal{P}_1+\cdots+\mathcal{P}_r=\mathbb{I}$$
2. $$\mathcal{P}_i|_{E_{\lambda_{j\neq i}}}=0$$
3. $$\text{Ran}(\mathcal{P}_i)=E_{\lambda_i}$$
4. $$\mathcal{P}_k\mathbf{v}=\mathbf{v}$$

### Decomposition
* Therefore for any $\mathbf{v}$, there is a unique decomposition $$\mathbf{v}=\mathcal{P}_1\mathbf{v}+\cdots + \mathcal{P}_r\mathbf{v}$$

## Geometric meaning of algebraic multiplicity
* For $\lambda\in\sigma(A)$ 
* we have algebraic multiplicity $a_\lambda$
* and geometric multiplicity $g_{\lambda}$
* depth of $\lambda$ is $d_{(\lambda)}$
	* the smallest integer such that $(A-\lambda\mathbb{I})^{d_{(\lambda)}}|_{E_\lambda}=0)$
* $$g_\lambda \leq d_\lambda \leq a_\lambda = \dim{E_\lambda}$$

### Jordan-Chevalley Decomposition (Corollary 3.9)
* For all $A:V\rightarrow V$
* there exists $D,N:V\rightarrow V$
	* $D$ is diagonalizable
	* $N$ is nilpotent
	* $D$ and $N$ commute
* such that $$A=D+N$$

### Application: Function of Linear Transformations
* Let $f:\mathbb{R}\rightarrow\mathbb{R}$ be a function with convergent taylor series

# Structure of nilpotent operators
## Cyclic Subspace
* For all $\mathbf{v}$, a cyclic subspace generated by $\mathbf{v}$ and $A$ is defined by $$C_A(\mathbf{v})\coloneqq\text{span}\{\mathbf{v},A\mathbf{v},\cdots,A^{d-1}\mathbf{v}\}$$

### Properties
* $AC_A(\mathbf{v})\subset C_A(\mathbf{v})$
* $\mathbf{v},A\mathbf{v},\cdots,A^{d-1}\mathbf{v}$ forms a basis in $C_A$
	* $A|_{C_A(\mathbf{v})}$ in this basis is a Jordan block

## Jordan Blocks 
* A matrix with all zeroes and 1's above the diagonal
* $J_d(\lambda)$

## Theorem 4.1
* Any nilpotent $A:V\rightarrow V$ is similar to a block diagonal with Jordan blocks

## Tools to Create Jordan Normal Form
### Elementary Transformations
#### Add rows
* $$A\rightarrow (\mathbb{I}+aE_{ij})A(\mathbb{I}-aE_{ij})$$
* add a multiple of jth row to the ith row and subtract the same multiple of the ith column from the jth column

#### Muliplication by scalar
* multiply ith row by $d$ and ith column by $d^{-1}$

#### Switch rows
* Switch rows $i$ and $j$ and columns $i$ and $j$

## Algorithm for producing Jordan Normal Form
1. Let $A$ be a nilpotent upper triangular matrix
2. Begin with the last column of $A$

3. If the last column is all $0$
	* then reduce the problem to the one for $(n-1)\times(n-1)$ matrices
4. Else, there is at least one nonzero entry in the last column
	* Pick $j$, which is the largest number such that $a_{jn}\neq 0$
	* can make $a_{jn}=1$ by conjugating $A$ with a matrix $D=\text{diag}\{1,1,\cdots, a_{j,n}^{-1}, 1,\cdots, 1\}$ 
	* Kill every entry in the last column above $j$ th row 
5. If $j=n-1$, proceed to column $(n-1)$
6. Else, consider the rest of the $j$ th row not including the last column
	* If it is $0$
		* move $j$ th row down to $n-1$ th row and move all the rows below above by change in basis from rows $e_1,\cdots,e_j,\cdots,e_{n-1},e_n$ to $e_1,\cdots,e_{j+1},\cdots,e_{n},e_j$ 
	* Else, pick the largest $i$ such that $a_{j,i}$
		* Can make $a=_{j,i}=1$ by dividing $i$ th column by $a_{j,i}$ and multiplying the $i$ th row by $a_{j,i}$
	* subtract $i$ th column from the last column and add the last row to the $i$ th row
7. If there is a nonzero value below the $j$ th row
	* If the nonzero value is on the $i$ th column
		* Repeat the previous steps
	* If the nonzero value just on the triangular, then can add a column to the $i$ th column 
8. Else the rows below the $j$ th row is just $0$
	* Can use elementary transformation to make all entries in the $j$ th row (except the last column) equal to $0$
	* Then can use permutation to make the last column look like $[0,\cdots,1,0]^T$
9. then repeat the previous steps with the next column

## Do we need to perform all these steps to figure out Jordan Normal Form
### Dot Diagram

/jordanNormalForm.png

* Short Form way of representing Jordan normal form
* Let $A$ be a matrix is jordan normal form
* The size of blocks is the number of dots in a column
* The number of columns is the number of Jordan blocks
* the size of $A$ is the number of dots
* the rank of $A$ is the number of dots below the 1st row
* the rank of $A^2$ is the number of dots below the 2nd row
* the rank of $A^k$ is the number of dots below the kth row
* the size of the largest Jordan Block is the number of rows

#### $A^2$
* Since $A$ is in block diagonal, the square is the same as the Jordan blocks squared
* In each Jordan block, all the $1$'s are pushed one row above

### Theorem
* If $A:V\rightarrow V$ is an arbitrary linear transformation, then there exists a basis in $V$ such that $A$ has a form 
* $$\text{diag}\{J_{n_{1},1}(\lambda_1),J_{n_{1},2}(\lambda_1), \cdots , J_{n_1,r_1}(\lambda_1), \cdots, J_{n_k,1}(\lambda_k),\cdots J_{n_k,l_k}(\lambda_k)\}$$
	* where $\{\lambda_1,\cdots,\lambda_k\}=\sigma(A)$
	* Algebraic multiplicity of $\lambda_j$ is equal to the number of jordan blocks
	* $n_{j,1}\leq n_{j,2}\leq\cdots\leq n_{j,j}$
* Each $A_j$ is such that $(A_j-\lambda_j\mathbb{I})$ is nilpotent