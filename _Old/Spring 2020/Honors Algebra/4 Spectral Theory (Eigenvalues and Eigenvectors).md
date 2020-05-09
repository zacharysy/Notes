# Motivation
* Matrices are difficult to multiply
* Diagonal matrices are easy to multiply
* Therefore best to reduce matrices to diagonal ones or as close as possible

## Example: Fibonacci Numbers
* $\mathbf{v}_n= [F_n, F_{n-1}]^T$
* then let $A = \begin{pmatrix} 1 & 1 \\ 1 & 0\end{pmatrix}$
* $\mathbf{v}_{n+1}=A\mathbf{v}_n$
	* This is called Dynamical System
* so $\mathbf{v}_n=A^n\mathbf{v}_1$
* let $\mathbf{v}_n\rightarrow C\mathbf{y}_n$
	* therefore $$\mathbf{y}_{n+1} = (C^{-1}AC)\mathbf{y}_n$$
* Want $A$ to be $\Lambda$ such that $\Lambda = \begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2\end{pmatrix}$
*
* Therefore $\mathbf{v}_n=C\Lambda^nC^{-1}[1,0]^T$
* 
* Want to find solution to
	* $$A\mathbf{v}=\lambda\mathbf{v}$$
* which is equivalent to
	* $$(A-\lambda\mathbb{I})\mathbf{v}=0$$
	

# Main Definitions
## Eigenvalues, Eigenvertors
* $A$ is $n\times n$
* we say that $\lambda$ is an **eigienvalue** of $A$
*  and $\mathbf{v}$ is the corresponding **eigenvector** 
	*  Is not unique, since for all $c\in\mathbb{R}$, $c\mathbf{v}$ is also an eigenvector
*  if $\mathbf{v\neq 0}$ and $$A\mathbf{v}=\lambda\mathbf{v}$$

## Finding Eigenvalues
* If $\lambda$ is an eigenvalue, then $$(A-\lambda\mathbb{I})\mathbf{v}=0$$ has a nontrivial solution
	* when $A-\lambda\mathbb{I}$ is not invertible
	* and so when $\det(A-\lambda\mathbb{I})=0$
		* and also $\det(\lambda\mathbb{I}-A )=0$

## Characteristic Polynomial of $A$
* $\det(A-\lambda\mathbb{I})$ is a polynomial of degree $n$ of $\lambda$
* $P_A(\lambda)=\lambda^n-\lambda^{n-1}\text{Tr }{A}+\cdots + (-1)^n \det{A}$
* Finding the eigenvalues of $A$ is the same as finding the roots of $P_A(\lambda)$
	* But even if $A$ is real, it may not have real eigenvalues
* $\lambda$ is an eigenvalue of $A$ iff $P_A(\lambda)=0$

## Complex Numbers ($\Bbb C$)
* $i^2 = -1$
* If $z=a+bi$ then we denote $\bar{z}=a-bi$, is called the complex conjugate
* $|z|=\sqrt{z\bar{z}}$

### Geometric representation of $\Bbb{C}$
* a vector in $\Bbb R^2$
* real axis and imaginary axis
* $z=|z|(\cos\alpha+i\sin\alpha) = |z|e^{i\alpha}$
	* $\bar{z}=|z|(\cos\alpha-i\sin\alpha) = |z|e^{-i\alpha}$ 

#### Euler Identity
* $e^{i\pi}+1=0$

### Matrix Form
* $\begin{pmatrix}a&b\\-b&a\end{pmatrix}$
* any 2 such matrices commute
* $\begin{pmatrix}a&b\\-b&a\end{pmatrix}=a\Bbb I_2 + b\Bbb J$
	* such that $\Bbb J^2 = -\Bbb I$
* So the set $\{a\Bbb I_2 + b\Bbb J\}$ can be viewed as a matrix model or representation of complex numbers

## Spectrum
* The set of all eigenvalues of of $A$ is called the spectrum of $A$ and denoted by $\sigma(A)$

## Fundamental Theorem of Algebra
* Every polynomial with complex coefficients has a zero in $\Bbb C$

### Corollary
* $P(\lambda)$ can be factored as $$P(\lambda)=(\lambda-\lambda_1)(\lambda-\lambda_2)\cdots(\lambda-\lambda_n)$$
	* where $\lambda_k$ are the complex roots, counting multiplicities (so they can coincide)

## Linear Transformation
* $T:V\rightarrow V$
* Linear transformation of a vector space $V$
* $\lambda$ is an eigenvalue of $T$ if there exists nonzero $\mathbf{v}\in V$ such that $T(\mathbf{v}) = \lambda\mathbf{v}$

### Characteristic Polynomial for $T$
* Pick a basis in $V$, $\mathcal{B}$. Then
* $$P_{T_{\mathcal{B},\mathcal{B}}}(\lambda) = \det(\lambda\mathbb{I}_n-T_{\mathcal{B},\mathcal{B}})$$
	* and this characteristic polynomial is independent of basis
		* $P_{T_{\mathcal{B},\mathcal{B}}}(\lambda)=P_{T_{\mathcal{A},\mathcal{A}}}(\lambda)$

### Relating to Matrices
* If $A$ is $n\times n$
* and $\tilde{A} = CAC^{-1}$
	* then $P_A(\lambda)=P_{\tilde{A}}(\lambda)$
* Characteristic polynomial does not change under similarity transformation

## Multiplicity
### Algebraic Multiplicity
* $P_A(\lambda)=(\lambda-\lambda_1)^{m_1}\cdots(\lambda-\lambda_r)^{m_r}$
* $r\leq n$ and $\sum_1^r m_i = n$
* $m_i$ is called an algebraic multiplicity of $\lambda_i$

### Geometric Multiplicity
* Let $\lambda\in\sigma(A)$
* geometric multiplicity of $\lambda$ is $\dim\{\mathbf{v}: A\mathbf{v}=\lambda\mathbf{v}\}$

### Proposition 1.1
* Geometric multiplicity of an eigenvalue cannot exceed its algebraic multiplicity

## Trace and Determinant
* $\text{tr} A = \lambda_1+\cdots+\lambda_n$
* $\det A = \lambda_1\cdots\lambda_n$
## Companion Matrix/Frobenius Matrix
* Every polynomial $p(\lambda)=\lambda^n+\cdots$ is a characteristic polynomial of at least one matrix
* The last column of $A$ is the negative of the coefficients of $p$ with $p_0$ in first row and $p_n$ in last row. Diagonal is all zero except for $p_n$ and there are $1$'s below diagonal

## Eigenvalues of triangular matrix Triangular
* If $A$ is triangular then $\sigma(A)=\{a_{11},\cdots,a_{nn}\}$

# Diagonalization
## Diagonalizable
* $A$ is diagonizable if there exists an invertible $C$ and a diagonal matrix $D$ such that $A=CDC^{-1}$
* If $A$ is diagonalizable, then $P_A(\lambda)=P_D(\lambda)$
* 
* $A\mathbf{v_i}=\lambda_i\mathbf{v_i}$ iff the set of eigenvectors of $A$ is given by the column of $C$, which are linearly independent because $C$ is invertible
* 
* $f(CDC^{-1})=Cf(D)C^{-1}$
	* for any function


## Theorem 2.1
* $A$ is diagonalizable iff there exists a basis formed by eigenvectors of $A$

## Application: Functions of Matrices
* $A=CDC^{-1}$
* $A^m = CD^mC^{-1}$
	* Where $D$ has $\lambda^k$ in the diagonal
	* Easier to compute powers of matrices
* If $P(t)$ is any polynomial then $P(A)= CDC^{-1}$
	* Where $D$ has $P(\lambda_k)$ in the diagonal
* Similarly if $f(t)$ has a taylor series, then can do the same thing
	* Where $D$ has $f(\lambda_k)$ in the diagonal

## Application: Systems of Linear Differential Equations
* A system of linear differentials with constant coefficients is $$\frac{d}{dt}\mathbf{x}(t)=A\cdot\mathbf{x}(t)$$
* Consider function $\Phi(t)=e^{tA}$, then $\frac{d}{dt}\Phi(t)=A\Phi(t)$
* Consider $\mathbf{x}(t)=e^{tA}\mathbf{x}(0)$, then $\frac{d}{dt}\mathbf{x}(t)=A\mathbf{x}(t)$
* If $A$ is diagonalizable, then easy to compute $\mathbf{x}(t)$

## If $A$ not diagonalizable
### Example 1 (Jordan Block)
* $$A = \begin{pmatrix}
\lambda & 1 & 0 & 0 \\
0 & \lambda & 1 & 0 \\
0 & 0 & \lambda & 1 \\
0 & 0 & 0 & \lambda
\end{pmatrix}$$ 
* $\sigma(A)=\{\lambda\}$
* if $f(\lambda) = \lambda^n$
*  $$A^n = \begin{pmatrix}
f(\lambda) & f'(\lambda) & \frac{f''(\lambda)}{2!} & \frac{f'''(\lambda)}{3!} \\
0 & f(\lambda) & f'(\lambda) & \frac{f''(\lambda)}{2!} \\
0 & 0 & f(\lambda) & f'(\lambda) \\
0 & 0 & 0 & f(\lambda)
\end{pmatrix}$$ 

## Theorem 2.2
* $A$ be a linear transformation $A:V\rightarrow V$
* $\lambda_1\cdots\lambda_r$ are distinct eigenvalues of $A$ and
* $\mathbf{v_1\cdots v_r}$ are corresponding eigenvectors
	* Then $\mathbf{v_1\cdots v_r}$ are linearly independent

### Corollary
* If $A$ has all distinct eigenvalues, then $A$ is diagonalizable

## How to determine eigenvalues of $A$ are distinct without calculating them
* Take a vector $\mathbf{v}_0\in V$
* consider $\mathbf{v}_0,A\mathbf{v}_0,A^2\mathbf{v}_0,\cdots , A^{n-1}\mathbf{v}_0$
* If this collection of vectors are linearly independent, $\mathbf{v}_0$ is called a cyclic/vacuum vector
* 
* __Theorem:__ If $A$ is diagonalizable, then there exists a cyclic vector
	* So for all $\mathbf{v}_0$, calculate determinant of resulting vector and if it is zero then $A$ is not diagonalizable

## Direct Sum of Subspaces
* $V$ is a vector spaces with subspaces $V_1,\cdots,V_r$
* $V$ is a direct sum of $V_1,\cdots,V_r$
	* notation: $V=V_1+\cdots + V_r$
* if every vector $\mathbf{v}\in V$ has a unique representation as $\mathbf{v}_1+\cdots+\mathbf{v}_r$, such that $v_k\in V_k$
	* Generalizes the notion of a basis

## Theorem 2.6
* Let $V=V_1+\cdots+V_r$ and let $\mathcal{B}_1,\cdots,\mathcal{B}_r$ be bases of $V_1,\cdots,V_r$
	* Then $$\mathcal{B}=\bigcup_{i=1}^r\mathcal{B}_i$$ is a basis in $V$

## Criterion of Diagonalizability (Theorem 2.8)
* Let $A:V\rightarrow V$ be a linear transformation, $\dim V = n$
* $A$ is diagonalizable iff
	* for any $\lambda\in\sigma(A)$
	* the algebraic multiplicity of $\lambda$ is equal to its geometric multiplicity
		* which is $\dim\text{Ker}(A-\lambda\mathbb{I}$)
