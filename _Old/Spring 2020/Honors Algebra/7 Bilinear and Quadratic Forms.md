# Main Definitions
## Bilinear Form
* Let $V$ be a vector space
* $(\cdot,\cdot):V\times V \rightarrow\mathbb{C}$ is called a bilinear form if
	* for any $\mathbf{v_1,v_2,v_3}$ and $\alpha_1,\alpha_2$
	* $$(\alpha_1\mathbf{v}_1+\alpha_2\mathbf{v}_2,\mathbf{v_3})=\alpha_1(\mathbf{v_1,v_3})+\alpha_2(\mathbf{v_2,v_3})$$
	* and
	* $$(\mathbf{v_3},\alpha_1\mathbf{v}_1+\alpha_2\mathbf{v}_2)=\alpha_1(\mathbf{v_3,v_1})+\alpha_2(\mathbf{v_3,v_2})$$
	* Basically linear in both variables
* Different from inner product in that inner product is not bilinear, and Bilinear Forms don't have to be symmetric

### Possible Properties
* A bilinear form is symmetric if $$(\mathbf{v_1,v_2})=(\mathbf{v_2,v_1})$$ for all $\mathbf{v_1,v_2}$
* A bilinear form is skew-symmetric if $$(\mathbf{v_1,v_2})=-(\mathbf{v_2,v_1})$$  
* A bilinear form is nondegenerate if $$(\mathbf{v,w})=0,\forall\mathbf{w}\in V \implies \mathbf{v}=0$$ 

### Matrix of Bilinear Form
* Let $(,)$ be a bilinear form in $V$ and pick a basis $\mathbf{e_1,\cdots,e_n}\in V$
* For any $\mathbf{x,y}\in V$ can be written as $$\mathbf{x}=x_1\mathbf{e_1}\cdots x_n\mathbf{e_n}$$ and $$\mathbf{y}=y_1\mathbf{e_1}\cdots y_n\mathbf{e_n}$$
* So let $A=(a_{ij})^n_{i,j=1}$, then
$$(\mathbf{x,y})=\mathbf{x}^TA^*\mathbf{y}$$
* in other words
$$(\mathbf{x,y})=\langle A\mathbf{x},\mathbf{y}\rangle$$
* So a bilinear form is an $n\times n$ matrix
	* and bijective if basis is fixed
* The matrix $A$ is determined uniquely by the bilinear form

### Bilinear Form under a change of basis
* If $A$ is the matrix of bilinear form
* and $C$ is the invertible matrix such that $\mathbf{x}=C\mathbf{u}$
	* and $\langle A\mathbf{x,y}\rangle=\langle AC\mathbf{x},C\mathbf{y}\rangle$
* then under a change of basis, $$A\rightarrow C^*AC$$
	* Which is similar if $C$ is unitary

## Quadratic Form
* $$Q[\mathbf{x}] = (\mathbf{x,x})$$
* Equivalently, $$Q[\mathbf{x}]=\langle A\mathbf{x,x}\rangle$$

### Noninjectivity of Quadratic Form
* Correspondence between quadratic forms and matrices $A$ is not a bijection
	* A quadratic form can have an infinite number of matrix representations

### Bijection 
* If $A$ is self-adjoint, then the quadratic form is unique 

### Skew Symmetric Bilinear Form
* If the bilinear form is skew-symmetric, then the quadratic form is $0$

# Diagonalization of Quadratic Forms
* Want to reduce $Q[\mathbf{x}]$ to a form (in some other basis) $$\langle D\mathbf{y,y}\rangle=\sum_{i=1}^n d_iy_i^2$$ 

## Orthogonal Diagonalization
* If the change of basis is orthogonal, then it is self-adjoint and so can be diagonalized
* Let $U$ be an invertible matrix, and $D$ a diagonal matrix of eigenvalues
* Can pick a column of $U$ to be eigenvectors forming an ONB $$U^*AU=D$$

## Non-orthogonal Diagonalization
* Assume already have $$Q[\mathbf{y}]=\langle D\mathbf{y,y}\rangle$$ 
* Then find diagonal invertible $C$ such that $$D= C^*DC$$
	* Where the diagonal values of $C^*DC$ are equal to $\lambda_ic_i^2$
	* By picking appropriate $c_i$, can reduce all the diagonal entries of the matrix to $\pm 1$ or $0$

## Theorem
* Let $Q[\mathbf{x}]$ be a quadratic form
* Then
	* If Orthogonal
		* There exists an ONB in which $Q$ has an expression $$Q[\mathbf{y}]=\sum_{i=1}^n \lambda_iy_i^2$$
	* If not necessarily orthogonal
		* There exists a basis in which $Q$ has an expression $$Q[\mathbf{z}] = z_1^2 + \cdots + z_r^2 - z_{r+1}^2-\cdots-z_m^2$$
			* where $0\leq r\leq m \leq n$

### Practical Ways to Diagonalize $Q[\mathbf{x}]$
* Completing the square
* Row reduction

# Silvester's Law of Inertia
## Theorem
* $Q[\mathbf{x}]=\langle A\mathbf{x,x}\rangle$
* $A$ is self-adjoint
* Suppose $Q$ is diagonallized as $$Q[\mathbf{z}] = z_1^2 + \cdots + z_{r_+}^2 - z_{r_++1}^2-\cdots-z_{r_-+r_+}^2$$
* Then $r_+,r_-$ depends only on $A$ and not on the way $Q[\mathbf{x}]$ is diagonalized

### Claim
* $r_+$ is the dimension of the positive subspace for $Q[\mathbf{x}]$
* $r_-$ is the dimension of the negative subspace for $Q[\mathbf{x}]$

## Definition
* $E$ is called a **positive** subspace for $Q[\mathbf{x}]$ if 
	* $Q[\mathbf{x}]>0$
* $E$ is called a **negative** subspace for $Q[\mathbf{x}]$ if 
	* $Q[\mathbf{x}]<0$
* $E$ is called a **neutral** subspace for $Q[\mathbf{x}]$ if 
	* $Q[\mathbf{x}]=0$


# Positive Definite Forms. Minimax chacarterization of eigenvalues and the Silvester's criterion of positivity
## Definitions
### Positive (Semi)Definite
* If for all $\mathbf{x}\neq 0$,
	* $Q[\mathbf{x}]>0$
		* then it is positive definite
		* $A$ has all positive eigenvalues
	* $Q[\mathbf{x}]\geq 0$
		* then it is positive semidefinite
		* $A$ has all nonzero eigenvalues
### Negative (Semi)Definite
* If for all $\mathbf{x}\neq 0$,
	* $Q[\mathbf{x}]<0$
		* then it is negative definite
		* $A$ has all negative eigenvalues
	* $Q[\mathbf{x}]\leq 0$
		* then it is negative semidefinite
		* $A$ has all nonpositive eigenvalues
### Indefinite
* If either $Q[\mathbf{x}]\geq 0$ or $Q[\mathbf{x}]\leq 0$
	* then it is indefinite
	* Diagonalization has both nonnegative and negative eigenvalues

## Silvester's Criterion of Positivity (Theorem 4.2)
* Let $Q[\mathbf{x}]$ be a quadratic form in $\mathbb{R}^n$ and assume $Q$ is positive definite
* Let $A=A^*$ be the matrix associated with the quadratic form with entries $a_{i,j}$
	* Let $A_k$ be an upper left submatrix with diagonal size $k$
* Then $$Q_{A_k}[\mathbf{x}]=\langle A_k\mathbf{x},\mathbf{x}\rangle$$ is positive definite
* 
* In conclusion, a self-adjoint matrix $A$ is positive definite $\iff$ $$\det A_k > 0$$ for all $k=1,\cdots,n$

## Minmax Chacarterization of Eigenvalues (Theorem 4.3)
* Let $A=A^*$
* Suppose $\sigma(A)=\{\lambda_1,\cdots\lambda_n\}$
	* $\lambda_1\geq\cdots\geq\lambda_n$
* Then
	* $$\lambda_k=\max_{E: \dim E = k}\min_{\lVert\mathbf{x}\rVert=1;\mathbf{x}\in E}\langle A\mathbf{x,x}\rangle=\min_{F: \text{codim }F = k-1}\max_{\lVert\mathbf{x}\rVert=1;\mathbf{x}\in F}\langle A\mathbf{x,x}\rangle$$

## Interlacing Property of Eigenvalues (Corollary 4.4)
* Let $A=A^*$
* Let $\hat{A}$ be the $(n-1)\times(n-1)$ upper left block of $A$, then $\hat{A}=\hat{A}^*$
* Let $\lambda_k$ be eigenvalues of $A$ and $\mu_k$ be eigenvalues of $\hat{A}$
* then $$\lambda_1\geq\mu_1\geq\cdots\geq\lambda_{n-1}\geq\mu_{n-1}\geq\lambda_n$$