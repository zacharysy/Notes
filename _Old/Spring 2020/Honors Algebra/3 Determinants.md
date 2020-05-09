# Introduction
## Examples of Determinants
### Determinants In $\mathbb{R}^2$ (Signed Area)
* Let $\mathbf{v_1,v_2}$ be two vectors in $\mathbb{R}^2$. The area of the parallelogram dependent on the two vectors $$\text{Area}(\mathbf{v_1,v_2})=\mathbf{|v_1||v_2|}\sin\theta$$
* let $x_i = |\mathbf{v_i}|\cos\alpha_i$ and $y_i = |\mathbf{v_i}|\sin\alpha_i$ so $$\text{Area}(\mathbf{v_1,v_2})=\mathbf{|v_1||v_2|}(\sin\alpha_2\cos\alpha_1-\sin\alpha_1\cos\alpha_2)$$
* and $$\text{Area}(\mathbf{v_1,v_2})=x_1y_2-x_2y_1$$
* can be negative, and so it is the signed area and has more information

#### Properties of Signed Area
1. Let $|\mathbf{v_1,v_2}|:=\text{Area}(\mathbf{v_1,v_2})$
2. (Skew-symmetry) $$|\mathbf{v_2,v_1}| = -|\mathbf{v_1,v_2}|$$
3. $$|\mathbf{v_1},c\mathbf{v_1}| = 0$$
4. (Linearity in every argument) $$|c\mathbf{v_1,v_2}| = c|\mathbf{v_1,v_2}|$$
 $$|\mathbf{v_1+v_2,v_3}| = |\mathbf{v_1,v_3}|+|\mathbf{v_2,v_3}|$$
5. (Normalization) $$|\mathbb{I}|=1$$


#### Determinant
* $$\begin{vmatrix}x_1 & x_2 \\ y_1 & y_2\end{vmatrix}=x_1y_2-x_2y_1$$
* is called the determinant

### Determinants in $\mathbb{R}^3$ (Volume of Parallelotope)
* $\text{Vol}(\mathbf{v_1,v_2,v_3})$ is the height multiplied by the area of the base
* $$\text{Vol}(\mathbf{v_1,v_2,v_3})=|\mathbf{v_3}|\cos(\mathbf{v_1\times v_2})|\mathbf{v_1\times v_2}|$$
* and so
* $$\text{Vol}(\mathbf{v_1,v_2,v_3}) = |\mathbf{v_1,v_2,v_3}| =(\mathbf{v_1\times v_2})\cdot\mathbf{v_3}$$
	* cross product then inner product
* this is a signed volume and called the mixed product

#### Properties of the Mixed Product
1. (Skew-symmetry) $|\mathbf{v_1,v_2,v_3}|=$ 
	* $-|\mathbf{v_2,v_1,v_3}|$
	* $-|\mathbf{v_3,v_2,v_1}|$
	* $-|\mathbf{v_1,v_3,v_2}|$
2. If the vectors are linearly dependent then
	* $|\mathbf{v_1,v_2,v_3}|=0$ 
3. If any $\mathbf{v}_i$ is replaced with $c\mathbf{v}_i$ then
	* $|\mathbf{v_1,v_2,v_3}|=c|\mathbf{v_1,v_2,v_3}|$ 
4. (Linearity) $$|\mathbf{v_1+w_1,v_2,v_3}|=|\mathbf{v_1,v_2,v_3}|+|\mathbf{w_1,v_2,v_3}|$$
5. (Normalization) $$|\mathbf{e_1,e_2,e_3}|=1$$

#### Determinant
* $$\begin{vmatrix}x_1 & x_2 & x_3\\ y_1 & y_2 & y_3 \\z_1 & z_2 & z_3 \\\end{vmatrix}=\begin{vmatrix}y_1 & y_2 \\ z_1 & z_2\end{vmatrix}x_3-\begin{vmatrix}x_1 & x_2 \\ z_1 & z_2\end{vmatrix}y_3+\begin{vmatrix}x_1 & x_2 \\ y_1 & y_2\end{vmatrix}z_3$$

# Generalization of Determinant
* Want notion of "signed n-dimensional volume" (Determinant)
	* If $\mathbb{R}^n\ni\mathbf{v_1,v_2,\cdots v_n}$ then the determinant is $$\mathbf{|v_1v_2\cdots v_n|}$$
	* Is unique

## Properties (Main Properties are 1,3,4)
1. (**Skew-Symmetry**) If any two vectors are interchanged, then  $\det$ gets multiplied by $-1$
2. If vectors are linearly dependent, then $\det = 0$
3. (**Linearity**) $\det$ is linear in every component
	* $\mathbf{|v_1v_2\cdots \alpha v_i +\beta w_i \cdots v_n|}= \alpha\mathbf{|v_1v_2\cdots v_i \cdots v_n|}+\beta\mathbf{|v_1v_2\cdots w_i \cdots v_n|}$
4. (**Normalization**) Determinant of the standard basis is equal to $1$
5. If some $\mathbf{v_i=v_j}$ for $i\neq j$ then $\det = 0$
6. If $\mathbf{v_i=cv_j}$ then $\det = 0$
7. If $\mathbf{v_i=0}$ then $\det = 0$
8. $\det$ is preserved under "column replacement" (row replacement with the transpose)

## Determinants of Diagonal and Triangular Matrices
### Diagonal
* Only nonzero values are on the diagonal
* $\det(\text{diag}\{a_1,a_2,\cdots,a_n\})=a_1 a_2 \cdots a_n$

### Elementary Matrices
* Multiplication by a constant, $a$, multiply determinant by a constant
* (Row Replacement) $\det(\mathbb{I}_n+aE_{ij})$ is preserved
* (Row Exchange) $\det(P_{ij})=-1$
 
### Triangular
* Diagonal matrix with nonzero values either above xor below diagonal
* $\det(\text{T}\{a_1,a_2,\cdots,a_n\})=a_1 a_2 \cdots a_n$



## Determinants of Transpose and Product
### Product
* $\det(AB)=\det(A)\det(B)$

### Transpose
* $\det(A^T)=\det(A)$ 

## Vandermonde Determinant
* Take a matrix where the columns are the powers of a number starting from $0$ up to $n-1$
* $$\det = \prod_{1\leq i < j \leq n}{(x_j-x_i)}$$

# Formula For Determinant of an $n\times n$ Matrix
* Let $A$ be an $n\times n$ matrix
* (It's long, just check 4.1: Formal Definition. Existence and uniqueness of the determinant)
* $$\det A =\sum_{\sigma\in\text{Perm}(n)}{a_{\sigma_1,1}a_{\sigma_2,2}\cdots a_{\sigma_n,n}}\text{ sign}(\sigma)$$
	* where $\text{Perm}(n)$ is the number of permutations of $\{1,2,\cdots,n\}$
	* and $\text{sign}(\sigma)$ is $1$ when the number of column swaps to turn permutation matrix is even, and $-1$ when it is odd
		* $(-1)^{\text{number of column swaps that reduce the permutation matrix to }\mathbb{I}^n}$

## Permutation Matrix
* Matrix with a single $1$ in each row/column and the rest are $0$


## Properties of the Formula
* Each term contains one entry from each column and from each row
	* So linear in every column and row
* In terms of matrix entries, $\det A$ is a polynomial function of degree $n$
	* So homogeneous, since every term is degree $n$

## Block Triangular
* Block matrix with zeros on one of the quadrants
* $$A = \begin{pmatrix} A_1 & B \\ 0 & A_2 \end{pmatrix}$$
	* $A_1$ is $k\times k$
	* $A_2$ is $(n-k)\times(n-k)$
	* $B$ is $k\times(n-k)$
* Since $$A= \begin{pmatrix} A_1 & 0 \\ 0 & \mathbb{I}_{n-k} \end{pmatrix}\begin{pmatrix} \mathbb{I}_k & 0 \\ 0 & A_2 \end{pmatrix} \begin{pmatrix} \mathbb{I}_k & A_1^{-1}B \\ 0 & \mathbb{I}_{n-k}\end{pmatrix}$$
* Then  $\det A = \det A_1A_2$

# Cofactor/Laplace Expansion
* Let $A_{i,j}$ be a $(n-1)\times(n-1)$ matrix obtained by removing the $i$ th row and $j$ th column

## Cofactor Expansion Across Row $i$
* $1\leq i \leq n$
* $$\det A = \sum_{j=1}^n{(-1)^{i+j}a_{i,j}}\det{A_{i,j}}$$

## Cofactor Expansion Across Col $j$
* $1\leq j \leq n$
* $$\det A = \sum_{i=1}^n{(-1)^{i+j}a_{i,j}}\det{A_{i,j}}$$

## Cofactors
* $$C_{i,j}=(-1)^{i+j} \det A_{i,j}$$
* So the cofactor expansion is really just
	*  $$\det A = \sum_{j=1}^n{a_{i,j}C_{i,j}}$$

## Cofactor Matrix
* Let $C$ be a cofactor matrix
* $C = \{C_{i,j}\}^n_{i,j=1}$

## Cofactor formula for the Inverse Matrix
### Theorem 5.2
* If $A$ invertible, the $$A^{-1}=\frac{1}{\det A}C^T$$
* Therefore $A$ is invertible iff its determinant is nonzero and iff its rank is equal to $n$

# Minors and Rank
## Minors
* Let $A$ be $n\times m$
* Consider any $k\times k$ submatrix of $A$, where $k\leq \min(m,n)$
* It is determined by a row set 
	* $$I=1\leq i_1 \leq \cdots \leq i_k \leq m$$ 
* and column set
	* $$J=1\leq j_1 \leq \cdots \leq j_k \leq m$$ 
* We call $\det A^J_I$ a minor formed by row set $I$ and column set $J$

### Example
* Any matrix entry of $A$ is a $1\times 1$ minor

### Total number of minors
* $$\sum_{k=0}^{\min(m,n)}{{m\choose k}\cdot {n \choose k}}$$
* empty has determinant $1$

## Thoerem 6.1
* If $A$ is an $m\times n$ matrix
* then $\text{rank } A = k$
* iff 
	* any $\ell\times\ell$ minor of $A$ with $\ell > k$ is $0$
	* and there exists a $k\times k$ minor of $A$ which is not $0$

## Every $A$ of Rank $1$ (Not in Book)
* Suppose $A$ is an $m \times n$ matrix with all nonzero entries and $\text{rank } A = 1$  then
	* $$A = (u_iv_j)^{m~~~n}_{i=1\,j=1}$$
	* $u_i,v_j\neq 0$

## Rank of Product
* $A$ is $m\times n$ and $B$ is $n\times\ell$
* $$\text{rank}(AB)\leq\min(\text{rank }A,\text{rank }B)$$
* 
## Binet-Cauchy formula
* $$\det (AB)^J_I=\sum_{\underbrace{1\leq\ell_1<\cdots<\ell_k\leq n}_L}\det{A}_I^L\cdot\det{B}_L^J$$

## Desnanot-Jacobi-Dodgson Formula
* $A$ is $n\times n$ then
* $\lvert A^{\hat{i}}_{\hat{i}}\rvert\lvert A^{\hat{n}}_{\hat{n}}\rvert - \lvert A^{\hat{n}}_{\hat{i}}\rvert\lvert A^{\hat{i}}_{\hat{n}}\rvert = \lvert A\rvert\lvert A^{\hat{i}\hat{n}}_{\hat{i}\hat{n}}\rvert$

## Cramer's Rule
* $A$ is $n\times n$ and invertible
* $A\mathbf{x}=\mathbf{b}$
* the $k$ th entry of the solution $x_k$ is given by $$x_k = \frac{\det B_k}{\det A}$$
* where $B_k$ is $A$ with the $k$ th column replaced with $\mathbf{b}$