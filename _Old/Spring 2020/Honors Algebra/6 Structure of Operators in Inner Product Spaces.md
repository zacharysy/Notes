* Let $X$ be a complex inner product space
* $A$ is self-adjoint if $A=A^*$
* $A$ is skew-adjoint if $A=-A^*$

# Upper Triangular representation of an operator

## Schur Normal Form (Theorem 1.1)
* For any linear transformation $A:X\rightarrow X$
	* there exists a unitary transformation $U$
	* and an upper triangular transformation $T$
	* such that $$A=UTU^*$$
		* Equivalently, there exists an ONB in which $A$ is upper triangular

## Theorem 1.2
* If $A$ is an operator in a real inner product space
* and $\sigma(A)\subset\mathbb{R}$
* then 
	* there exists an orthogonal $O$ 
	* and real upper triangular $T$
	* such that $$A=OTO^T$$

# Spectral Theorem for Self-Adjoint and Normal Operators

## Self-Adjoint
* $A$ is called self-adjoint if $A^*=A$

### Theorem 2.1
*  $\sigma(A)\subset\mathbb{R}$
	*  All the eigenvalues of $A$ are real

### Proposition 2.3
*  Let $\lambda,\mu\in\sigma(A)$, $\lambda\neq\mu$
*  and $A\mathbf{v}_\lambda=\lambda\mathbf{v}_\lambda$
*  and $A\mathbf{v}_\mu=\mu\mathbf{v}_\mu$
*  then $$\mathbf{v}_\lambda \perp \mathbf{v}_\mu$$

### Theorem 2.2 (Finite Dimensional Spectral Theorem)
* Any self-adjoint operator $A$ can be unitarily diagonalizable
	* There exists unitary $U$ and a real diagonal $D$ such that $$A=UDU^*$$
	* $A$ is unitarily equivalent to a real diagonal matrix

## Normal 
* Suppose $A$ is unitarily diagonalizable
	* $$A=UDU^*$$
	* $$A^* = UD^*U^*$$
* Then
	* $$AA^*=UDD^*U^*=UD^*DU^*=A^*A$$
* So a unitarily diagonalizable matrix commutes with its adjoint
* A matrix $N$ is called normal if it commutes with its adjoint

### Examples of Normal Operators
* Self-adjoint
* Skew-adjoint
* Unitary

## Theorem 2.4
* If $N$ is normal, then $N$ is unitarily diagonalizable

# Polar and Singular Value Decompositions
* Want to establish a representation of a linear transformation in an inner product space similar to $z=re^{i\theta}$

## Positive Definite
* A self-adjoint operator $A:X\rightarrow X$ is positive definite if
	* $$\langle A\mathbf{x,x}\rangle > 0$$
	* for all $\mathbf{x}\neq 0$

### Positive Semi-definite
* $$\langle A\mathbf{x,x}\rangle \geq 0$$
* for all $\mathbf{x}\in X$

## Theorem 3.1
* Let $A=A^*$ then
	* $A$ is positive definite $\iff$ all eigenvalues of $A$ are positive
	* $A$ is positive semidefinite $\iff$ all eigenvalues of $A$ are nonnegative

## Corollary 3.2
* If $A$ is self-adjoint and positive semidefinite
	* then there exists a unique positive semidefinite $B$ such that $B^2=A$
* $B=\sqrt{A}$ or $B=A^{\frac{1}{2}}$

## Recall
* For all $z\in\mathbb{C}$
* there exists a polar coordinate representation $z=|z|e^{i\theta}$
	* composition of rotation and positive stretching
* Want to find a similar polar decomposition for operators

## Modulus of Operator
* Consider $A^*A:X\rightarrow X$
	* it is positive semidefinite
* Then there exists a unique positive semidefinite square root
* Define this as $$|A| := (A^*A)^{\frac{1}{2}}$$

### Properties
1. $\lVert |A|\mathbf{x}\rVert = \lVert A\mathbf{x}\rVert$ (Proposition 3.3)
2. $\ker |A| = \ker A = (\text{Ran }|A|)^\perp$ (Corollary 3.4)

## Polar Decomposition (Theorem 3.5)
* Let $A:X\rightarrow X$ be an arbitrary operator
* then there exists a unitary $U$ such that
* $$A=U|A|$$
* with uniqueness of $U$ if $A$ is invertible

### For $A:X\rightarrow Y$
* Same form as above but $U:X \rightarrow Y$ is an isometry, not necessarily unitary

## Singular Value Decomposition (SVD) (Schmidt Normal Form)
* Let $A:X\rightarrow Y$
* Let $A^*A$ have nonzero eigenvalues (not necessarily all of the eigenvalues)
	* and are also positive since $A^*A$ is positive definite
* Then
	* $$\sigma_1=\sqrt{\lambda_1},\cdots,\sigma_r=\sqrt{\lambda_r}$$
	* are called the singular values of $A$
		* which are the nonzero eigenvalues of $|A|$


### Proposition 3.6
* Let $\mathbf{v_1,\cdots,v_r}$ be ONS of eigenvalues corresponding to $\lambda_1,\cdots,\lambda_r$
* Then $\mathbf{w_1,\cdots,w_r}$ given by $$\mathbf{w_i}=\frac{1}{\sigma_i}A\mathbf{v_i}$$ is also an orthonormal system
* So another way to represent $A$
	* $$\forall x \in X \implies x=\sum_{i=1}^r\langle x,\mathbf{v}_i\rangle\mathbf{v}_i + \mathbf{x_0}$$
		* $\mathbf{x}_0\in\ker A$

### Schmidt Decomposition
* So $$A\mathbf{x} = \sum_{i=1}^r\sigma_i\langle\mathbf{x,v}_k\rangle\mathbf{w}_k$$
* and $$A = \sum_{i=1}^r\sigma_i\mathbf{w}_k\mathbf{v}_k^*$$
* Decomposition may not be unique

#### Matrix Representation (Compact SVD)
* Let $V=[\mathbf{v_1 | \cdots | v_r}]$
* $W=[\mathbf{w_1 | \cdots | w_r}]$, 
* and $\Sigma$ be a diagonal matrix with nonzero entries $\sigma_i$, 
* then $$A=W\Sigma V^*$$

### Full SVD
* Complete $\mathbf{v_1,\cdots,v_r}$ to a basis in $\mathbb{C}^n$ 
	* By forming on ONB in $\ker A$
* Complete $\mathbf{w_1,\cdots,w_r}$ to a basis in $\mathbb{C}^m$ 
	* by forming an ONB in $(\text{Ran }A)^\perp$
* Then $V'=[\mathbf{v_1 | \cdots | v_r | v_{r+1}|\cdots|v_n}]$
*  $W'=[\mathbf{w_1 | \cdots | w_r | w_{r+1}|\cdots|w_n}]$
*  and $\Sigma'$ is an $m\times n$ block matrix with $\Sigma$ in the top left corner and the rest is $0$
*  So $$A=W'\Sigma'V'^*$$
*  $W'$ is unitary in $\mathbb{C}^m$ and $V'$ is unitary in $\mathbb{C}^n$

# Applications of SVD
## Rank
* Number of singular values is the rank of the matrix

## Geometry (4.1)
### Unit Ball in $\mathbb{R}^n$
* For any linear transformation $A:\mathbb{R}^n\rightarrow\mathbb{R}^m$
* the image of a Unit Ball is an $r$ - dimensional ellipsoid whose shape is determined by singular values

## Analysis (4.2)
### Operator Norm of Linear Transformation
* A vector space can be equipped with a norm
* Also $\mathcal{L}(\mathbb{C}^n,\mathbb{C}^m)$ (set of linear operators) is a vector space
	* has a natural inner product $$\langle A,B \rangle = Tr(B^*A)$$
	* So also has a norm $$\lVert A \rVert_2 = Tr(A^*A)^{\frac{1}{2}}=\sqrt{\sigma_1^2+\cdots+\sigma_r^2}$$
		* Also called Hilbert-Schmidt, or Frobenius

#### Operator Norm
* $A:\mathbb{C}^n\rightarrow\mathbb{C}^m$
* Take $$\lVert A\rVert := \max\{\lVert A\mathbb{x}\rVert: \lVert\mathbb{x}\rVert\leq 1 \}$$
* So in terms of Singular Values $$\lVert A\rVert = \max\{\sigma_1,\cdots,\sigma_r\}$$
* $$\lVert A\rVert \leq \lVert A\rVert_2$$

#### Inverse
* If $A$ is an invertible square matrix then $$\lVert A^{-1}\rVert = (\min\{\sigma_1,\cdots,\sigma_n\})^{-1}$$

## Computational (4.3)
### Condition Number
* $A:\mathbb{C}^n\rightarrow\mathbb{C}^n$ is invertible
* $$A\mathbf{x}=\mathbf{b}\implies\mathbf{x}=A^{-1}\mathbf{b}$$
	* but $\mathbf{b}$ is measured only approximately
* Replace $\mathbf{b}$ with $\mathbf{b}+\Delta\mathbf{ b}$
	* where $\Delta\mathbf{b}$ is the error
	* Relative error is $\frac{\lVert\Delta\mathbf{b}\rVert}{\lVert\mathbf{b}\rVert}$

### Solution
* $$A(\mathbf{x}+\Delta\mathbf{x})=\mathbf{b}+\Delta\mathbf{b}$$
* and want to measure the relative error of $\mathbf{x}$
* ends up that $$\frac{\lVert\Delta\mathbf{x}\rVert}{\lVert\mathbf{x}\rVert}\leq\frac{\sigma_1}{\sigma_n}\frac{\lVert\Delta\mathbf{b}\rVert}{\lVert\mathbf{b}\rVert}$$
	* where $\sigma_1$ is largest singular value and $\sigma_n$ is smallest singular value

### Condition Number
* $$\lVert A\rVert\lVert A^{-1}\rVert=\frac{\sigma_1}{\sigma_n}$$

#### Well-Conditioned
* The condition number is very small
* Image of unit ball is close to round

#### Ill-conditioned
* The condition number is very large

## Least Square Approximation
### Least Square using not full SVD
* let $\mathbf{x}_0=V\Sigma^{-1}W^*\mathbf{b}$
* Ends up that
* $$A\mathbf{x}_0=W'W'^*\mathbf{b}=\text{Proj}_{\text{Ran }W}\mathbf{b}=\text{Proj}_{\text{Ran }A}\mathbf{b}$$
* Therefore $\mathbf{x}_0$ is the least square solution
	* $$\mathbf{x}_0=V\Sigma^{-1}W^*b$$

### Moore-Penrose Inverse/Pseudoinverse
* Let $$A^+=V\Sigma^{-1}W^*$$

#### Properties
* $A^+AA^+=A^+$
* $AA^+A=A$
* 
* $(A^+A)^*=A^+A$
* $(AA^+)^*=AA^+$
* 
* Is unique
* A weakened version of an inverse

# Structure of Orthogonal Matrices
* $X=\mathbb{R}^n$
* $U$ is orthogonal
	* so $\lVert U\mathbf{x}\rVert = \lVert\mathbf{x}\rVert$
	* and $\det U = \pm 1$

## Rotation
* Any orthogonal $U$ with $\det U = 1$ is a rotation
 
## Reflections
* Preserves length but not orientation
* $$R=\begin{bmatrix}1&0\\0&-1\end{bmatrix}$$
* 
* If $\det U = -1$ (so a reflection), then define $$\tilde{U}=\begin{bmatrix}1&0\\0&-1\end{bmatrix}U$$
* $$\det{\tilde{U}}=1$$
* 
* Therefore any orthogonal matrix in $\mathbb{R}^n$ is either a rotation or a campasition of a rotation with a single reflection

## Simplifying a Orthogonal Matrix
### Change of Basis
* Try to change the basis so that $U$ is as simple as possible

### Composition
* Try to break $U$ into a composition of elementary $2D$ rotations


### Example 1 ($\mathbb{R}^2$)
 Assume $U$ is a rotation, so in the form $$R=\begin{bmatrix}\cos\alpha&-\sin\alpha\\\sin\alpha&\cos\alpha\end{bmatrix}$$
 
1. so eigenvalues are $e^{\pm i\alpha}$
	* which are not real so can't diagonalize
2. It's already an elementary rotation

### Example 2 ($\mathbb{R}^3$)
1. Eigenvalues have $|\lambda|=1$
	* So $\sigma(U)=\{e^{i\alpha},e^{-i\alpha},1\}$
	* Ends up that there exists an ONB in $\mathbb{R}^3$ of the form 
	* $$R=\begin{bmatrix}R_\alpha
&0\\0&1\end{bmatrix}$$

2. $U$ is determined completely by what it does to a pair of non-collinear vectors, or equivalently two points in space that are not on the same line through the origin
	* So every rotation $U$ in $\mathbb{R}^3$ can be represented as a poduct of at most $3$ elementary rotations

## General Case ($\mathbb{R}^n$) 
### Change of Basis (Theorem 5.1)
* For every rotation $U$, there exists an orthonormal basis in $\mathbb{R}^n$ in which
$$U=\begin{bmatrix}
R_{\alpha_1} & & & & \Huge{0} \\
&   R_{\alpha_2} \\
& &  \ddots & \\
& &   & R_{\alpha_k} \\
\Huge{0} & & &  & \mathbb{I}_p
\end{bmatrix}$$
* Where $R$ are $2D$ rotations
* and $p=n-2k$

#### Corollary (Theorem 5.2)
* If $U$ is orthogonal
* and $\det U = -1$
* then
	* there exists an ONB such that
$$U=\begin{bmatrix}
R_{\alpha_1} & & & & &\Huge{0} \\
&   R_{\alpha_2} \\
& &  \ddots & \\
& &   & R_{\alpha_k} \\
& & & &  \mathbb{I} \\
\Huge{0} & & &  & & -1
\end{bmatrix}$$

#### Restatement
* Any rotation in $\mathbb{R}^n$ is a product of at most $\frac{n}{2}$ commuting 2D rotations

### Elementary Rotations (Theorem 5.3)
* Any rotation $U$ in $\mathbb{R}^n$ can be represented as a product of at most $\frac{n(n-1)}{2}$ elementary rotations.

#### Lemma 5.4
* Let $\mathbf{x}=(x_1,x_2)^T$ be a vector in $\mathbb{R}^2$. Then there exists a rotation $R_\alpha$ such that 
	* $$R_\alpha\mathbf{x} = (a,0)^T$$
	* where $$a = \lVert\mathbf{x}\rVert =\sqrt{x_1^2+x_2^2}$$

#### Lemma 5.5
* Let $\mathbf{x}=(x_1,x_2,\cdots,x_n)^T$ be a vector in $\mathbb{R}^n$. Then there exists elementary rotations $R_1,R_2,\cdots,R_{n-1}$ such that 
	* $$R_{n-1}\cdots R_2R_1\mathbf{x} = (a,0,0,\cdots,0)^T$$
	* where $$a = \lVert\mathbf{x}\rVert =\sqrt{x_1^2+x_2^2+\cdots+x_n^2}$$
