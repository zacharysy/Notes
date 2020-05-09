# Vector Spaces
## Vectors
* Vectors in the plane $(\mathbb{R}^2)$ (2D Plane)
* Direction

## Vector Spaces
* A vector space $V$ is a set with elements that are equipped by operations of addition and multiplication by scalars, subject to the following axioms
## Vector Axioms
### Addition Axioms
#### Zero Vector (A1)
* $\exists \mathbf{0} \in V$ such that $\forall \mathbf{v} \in V$
	* $\mathbf{0} + \mathbf{v} = \mathbf{v}$

#### Commutativity (A2)
* $\mathbf{v} + \mathbf{w} = \mathbf{w} + \mathbf{v}$

#### Associativity (A3)
* $(\mathbf{v} + \mathbf{w}) + \mathbf{u} = (\mathbf{w} + \mathbf{v}) + \mathbf{u}$

#### Inverse (A4)
* $\forall \mathbf{v} \in V\,\exists\mathbf{w}$ such that
	* $\mathbf{v} + \mathbf{w} = \mathbf{0}$

### Scalar Multiplication Axioms
### Identity (M1)
* $1 \cdot \mathbf{v} = \mathbf{v}$

### Associativity (M2)
* $\alpha \cdot (\beta \cdot \mathbf{v}) = (\alpha\beta)\cdot \mathbf{v}$
	* $\forall \alpha,\beta \in \mathbb{F}$
	* $\mathbf{v} \in V$

### Distributivity (M3)
* $(\alpha + \beta)\mathbf{v} = \alpha\mathbf{v} + \beta\mathbf{v}$
	* $\forall \alpha,\beta \in \mathbb{F}$
	* $\mathbf{v} \in V$

### Distributivity (M4)
* $\alpha(\mathbf{v}+\mathbf{w}) = \alpha\mathbf{v}+\alpha\mathbf{w}$
	* $\forall \alpha \in \mathbb{F}$
	* $\mathbf{v},\mathbf{w} \in V$

## Examples of Vector Spaces
### Real Numbers
$$\mathbb{R}^n = \begin{bmatrix}x_1 \\ x_2 \\ \vdots \\ x_n\end{bmatrix}$$

### The Space of $m \times  n$ matrices $(M_{m\times n})$

$$M_{m\times n} = \begin{bmatrix}
a_{11} & a_{12}  & \cdots & a_{1n} \\
a_{21} & a_{22}  & \cdots & a_{2n} \\
\vdots & \vdots  & \vdots & \vdots \\
a_{m1} & a_{m2}  & \cdots & a_{mn} \\
\end{bmatrix}$$


#### Example
$A = (a_{ij}), B = (b_{ij})$
$$A+B = (a_{ij} + b_{ij})$$
$$\alpha A = (\alpha\, a_{ij})$$


### Continuous Functions on $[0,1]$
* $C[0,1]$


## Subspaces
Consider $M_{m\times n}$

### Symmetric Matrix (Sym)
$$\text{Sym} = \{(a_{ij})_{i,j=1}^n : a_{ij} = a_{ji} \}$$
$$\begin{bmatrix}
a_{11} & 0 \\
0 & a_{22} \\
\end{bmatrix}$$

### Skew Symmetric Matrix (SkewSym)
$$\text{SkewSym} = \{(a_{ij})_{i,j=1}^n\} : a_{ij} = -a_{ji}$$
$$\begin{bmatrix}
0 & a \\
-a & 0 \\
\end{bmatrix}$$

### Upper Triangular (B+)
$$\text{B+} = \{(a_{ij})_{i,j=1}^n\} : a_{ij} = 0 \text{ for } i>j$$
$$\begin{bmatrix}
x & x \\
0 & x \\
\end{bmatrix}$$

### Lower Triangular (B-)
$$\text{B-} = \{(a_{ij})_{i,j=1}^n\} : a_{ij} = 0 \text{ for } i< j$$
$$\begin{bmatrix}
x & 0 \\
x & x \\
\end{bmatrix}$$

# Linear Combinations, Bases
## Linear Combination
* Let $\mathbf{v_1},\cdots,\mathbf{v_p}$ be vectors in a vector space $V$, and $\alpha_1, \cdots, \alpha_p$ be real numbers
* Then $$\alpha_1\mathbf{v_1}+\cdots+\alpha_1\mathbf{v_p}$$ is called a linear combination of $\mathbf{v_1},\cdots,\mathbf{v_p}$
* $\text{Span}(\mathbf{v_1},\cdots,\mathbf{v_p})$ is set of all linear combinations of $\mathbf{v_1},\cdots,\mathbf{v_p}$

## Basis
* A collection of vectors $\{\mathbf{v_1},\cdots,\mathbf{v_p}\}$ in $V$ is a **basis** of $V$ if any $\mathbf{v}\in V$ can be **uniquely** represented as a linear combination of $\mathbf{v_1},\cdots,\mathbf{v_p}$
	* Example
		* $$\begin{bmatrix}x\\y\end{bmatrix} = \alpha\begin{bmatrix}1\\1\end{bmatrix}+\beta\begin{bmatrix}1\\-1\end{bmatrix}$$
		* $\alpha =\frac{x+y}{2},\beta =\frac{x-y}{2}$
		* So the right expression can represent any $xy$ pair
* A set of vectors is a basis iff this set is <u>**complete**</u> and <u>**linearly independent**</u>

### Examples
### $V=\text{Sym}_3$
* $$\begin{bmatrix}
		a_{1,1} & a_{1,2} & a_{1,3}\\
		a_{1,2} & a_{2,2} & a_{2,3}\\
		a_{1,3} & a_{2,3} & a_{3,3}\\
	\end{bmatrix}$$
* Using standard basis
	* $$a_{1,1}\begin{bmatrix}
		1 & 0 & 0\\
		0 & 0 & 0\\
		0 & 0 & 0\\
	\end{bmatrix}+\cdots$$
* Can be taken as $n$ diagonal matrices with just one $1$  ($n\choose 1$)
* and $\frac{n(n-1)}{2}$ matrices with two $1$ ($n\choose 2$)

## Trivial Linear Combination
* A linear combination is trivial if the coefficients all equal zero

## Linear Dependent Systems
* Vectors $\mathbf{v_1},\cdots,\mathbf{v_p}$ are **linearly dependent** if there exists $\alpha_1, \cdots, \alpha_p$ not all zero, such that the linear combination is not equal to zero
* There are a set of nonzero coefficients which lead to the linear combination to be equal to zero
	* not just the trivial combination
* A system is linearly dependent iff there exists a vector ($\mathbf{v}_k$) such that $$\mathbf{v}_k=\sum_{I=1,\cdots,p \neq k}{\alpha_i\mathbf{v}_i}$$
	* Basically there exists a vector which is a linear combination if other vectors

## Linear Independent System
* If the linear combination implies that the coefficients all equal to zero
* the only linear combination equal to zero is when the coefficients all equal zero

## Complete Systems
* A set of vectors is called a spanning or complete set of vectors if $\text{Span}(\mathbf{v_1},\cdots,\mathbf{v_p})=V$
	* All vectors in $V$ can be represented as linear combination
	* does not have no be unique
* A basis is a **complete linearly independent** set of vectors in $V$
* Any **_finite_** complete system contains a basis


# Linear Transformations. Matrix-vector multiplication
## Transformation
* If $X,Y$ are $2$ sets, then a **transformation/map/function** $$F:X\rightarrow Y$$ with unique $Y$

## Linear Transformation
* If $V,W$ are vector spaces, then a linear transformation $$T:V\rightarrow W$$ is a map from $V$ to $W$ such that $$T(\alpha_1\mathbf{v}_1+\alpha_2\mathbf{v}_2)=\alpha_1T(\mathbf{v}_1)+\alpha_2T(\mathbf{v}_2)$$ for all $\alpha_1,\alpha_2 \in \mathbb{R}$ and for all $\mathbf{v}_1,\mathbf{v}_2\in \mathbb{R}^n$

## Examples
### $T:V \rightarrow W$ 
* $$T(\mathbf{0})=\mathbf{w}$$
* $$T(\alpha\mathbf{0})=\alpha T(\mathbf{0})$$
* $$\mathbf{w}=\alpha\mathbf{w}$$

### $T:\mathbb{R}\rightarrow\mathbb{R}$
* Any linear transformation of type is of the form $$T(x)=cx$$

### $T=$ rotation by an $\alpha$
* It is a linear transformation, too bad idk polar

### $T=$ reflection with respect to $y$ -axis in $\mathbb{R}$
* $$T\left(\begin{bmatrix}x\\y\end{bmatrix}\right)=\begin{bmatrix}-x\\y\end{bmatrix}$$

### Differentiation with Polynomials
* it follows the two rules 

### From $\mathbb{R}^n$ to $\mathbb{R}^m$ (matrix vector multiplication)
* $$T\left(\begin{bmatrix}x_1\\\vdots\\x_n\end{bmatrix}\right)=T(x_1\mathbf{e}_1+\cdots+x_n\mathbf{e}_n)$$
* $$x_1T(\mathbf{e}_1)+\cdots+x_nT(\mathbf{e}_n)$$
* $$x_1\mathbf{a}_1+\cdots+x_n\mathbf{a}_n$$
	* where $a_n=[a_{1,n},\cdots,a_{n,n}]^T$
* Equivalent to multiplying a matrix by a vector 
* 
* If $A=(a_{ij})^{m\,n}_{i=1\,j=1}$ and
* $\mathbf{x}=(x_{k})^{n}_{k=1}$
* then $$A\mathbf{x}=\left(\sum^n_{j=1}{a_{ij}x_{ij}}\right)^m_{i=1}$$

### Generalization
* In general, let $V$ and $W$ be vector spaces with bases $\{\mathbf{v}_1,\cdots,\mathbf{v}_n\}$ and $\{\mathbf{w}_1,\cdots,\mathbf{w}_n\}$
* $T:V\rightarrow W$ is a linear transformation which for all $\mathbf{v}\in V$ we can write a unique representation as $\mathbf{v}=x_1\mathbf{v}_1+\cdots+x_n\mathbf{v}_n$
* then $$T(\mathbf{v})=T\left(\sum^n_{j=1}{x_j\mathbf{v}_j}\right)$$
* $$=\sum^n_{j=1}{x_jT(\mathbf{v}_j)}$$
* $$=\sum^n_{j=1}{x_j} \sum^m_{i=1}{a_{ij}\mathbf{w}_j}$$
* $$=\sum^m_{i=1}\left(\sum^n_{j=1} {a_{ij}x_j}\right){\mathbf{w}_j}$$

#### Conclusion
* If $\mathbf{x}=[x_1, \cdots, x_n]^T$ is a coordinate vector for $\mathbf{v}\in V$ with respect to a fixed basis, then a coordinate vector for $T(\mathbf{v})$ with respect to a fixed basis in $W$ is given by $A\cdot\mathbf{x}$ where $A$ is some $m\times n$ matrix
	* $n$ is equal to the number of items in $\mathbf{v}$ 
		* For example $V = \mathbb{P}_n$ would make a column number of $n+1$
	* $m$ is equal to the number of items in $T(\mathbf{v})$ 
		* For example $W = \mathbb{P}_{n+1}$ would make a row number of $n+2$
	* We can select a basis that will make $A$ more simple

# Linear Transformations as a Vector Space
* Let $$\mathcal{L}(V,W)=\left\{\text{all linear transformations } T:V\rightarrow W\right\}$$
* $\mathcal{L}(V,W)$ is itself a vector space
	* $$(\alpha_1T_1+\alpha_2T_2)(\mathbf{v})=\alpha_1T_1(\mathbf{v})+\alpha_2T_2(\mathbf{v})$$
		* $T_1$ and $T_2$ have to be w.r.t. the same basis

# Composition of Linear Transformations and Matrix Multiplication

## Composition of Linear Transformation
* $T_1:V\rightarrow W$ and $T_2:W\rightarrow Z$ 
	* $$(T_2\circ T_1)(\mathbf{v}) = T_2(T_1(\mathbf{v}))$$
* The composition is also a linear transformation

## Matrix Multiplication
* Let $V=\mathbb{R}^n, W=\mathbb{R}^m, Z=\mathbb{R}^{\ell}$
* $T_1:V\rightarrow W, T_2:W\rightarrow Z$
* $A=(a_{ij})$ is an $m\times n$ matrix
* $B=(b_{pq})$ is an $m\times \ell$ matrix
* Then $T_2 \circ T_1$ corresponds to a $\ell \times n$ matrix $$C=B\cdot A$$

* The matrix that corresponds to $T_2(T_1)$ is 
	* $$B\cdot A = \left(\sum_{q=1}^m {b_{pq}a_{qj}}\right)_{p=1\,j=1}^{\ell\,\,\,n}$$
	* $B,A$ are some matrices
* Not every two matrices can be multiplied. If $$A \text{ is } m\times n$$  and $$B \text{ is } k\times \ell$$ then $B\cdot A$ makes sense only if $\ell = m$ and  $A\cdot B$ only if $n = k$

## Properties of Matrix Multiplication
* Not commutative

### Multiplicative Identity
* If $A$ is $m \times n$
	* $$I_n: A \cdot I_n = A$$
	* $$I_m: I_m \cdot A = A$$
* Identity is $1$ in the diagonal and $0$ everywhere else

### Associativity
* $$(A \cdot B) \cdot C = A \cdot (B \cdot C)$$
* $A$ is $m\times n$, $B$ is $n \times k$, and $C$ is $k \times\ell$

### Distributivity
* $$A \cdot (B + C) = (A \cdot B) + (A \cdot C)$$
* $A,B$ is $m \times n$, and $C$ is $n \times\ell$
* $$(A + B) \cdot C = (A \cdot C) + (B \cdot C)$$
* $A,B$ is $m \times n$, and $C$ is $n \times\ell$ 

### Square Matrices
* If $\text{Mat}_{n\times n}$ is the set of all $n\times n$ matrices, 
* then matrix multiplication is associative, distributive, and has a multiplicative identity. 
* Not commutative and there is no multiplicative inverse (but other matrices can be invertible).

## Transposition
* $$A\mapsto A^T$$
* $A$ is an $m\times n$ matrix
* $A^T = (a_{ji})$ is an $n\times m$ matrix
* $$\text{Sym}_n=\left\{n\times n\,A: A^T=A \right\}$$
* $$\text{SkewSym}_n=\left\{n\times n\,A: A^T=-A \right\}$$
* $$(AB)^T=B^TA^T$$

## Trace
* The sum of the diagonal entries
* For an $n\times n$ matrix $A$,
* $\text{Trace}(A) = \text{Tr}(A)=\sum_{i=1}^n{a_{ii}}$

### Properties
* $$\text{Tr}(A^T)=\text{Tr}(A)$$
* $$\text{Tr}(AB)=\text{Tr}(BA)$$

# Invertible Transformations and Matrices. Isomorphisms

## Identity Transformation
* $I:V\rightarrow V$ is called an identity transformation if
* $$I(\mathbf{v})=\mathbf{v}$$
	* for all $\mathbf{v}\in V$

### Properties
* $$T:V\rightarrow W$$ then
	* $$TI_v=T$$
	* $$I_wT=T$$

## Invertible Transformation
* $A:V\rightarrow W$ is left-invertible if there exists $B:V\rightarrow W$ such that
	* $$BA = I$$
* $A:V\rightarrow W$ is right-invertible if there exists $C:V\rightarrow W$ such that
	* $$AC = I$$
* $A$ is called invertible if it is both left and right invertible

### Corollary
* For $A$ invertible, there exists some $A^{-1}$ such that
	* $$AA^{-1}=I_w$$ and
	* $$A^{-1}A=I_v$$

## Isomorphism
* A linear transformation that is invertible
* Two vector spaces $V$ and $W$ are called **isomorphic** if there exists a unique invertible linear transformation $$T:V\rightarrow W$$
* $T$ is called **isomorphism**

### Theorem 6.6
* If $T:V\rightarrow W$ is isomorphism 
* and $\{\mathbf{v_1},\cdots,\mathbf{v_p}\}$ is a basis
* then $\{T(\mathbf{v_1}),\cdots,T(\mathbf{v_p})\}$  is a basis in $W$

### Theorem 6.8
* $A:X\rightarrow Y$ is an isomorphism iff
	* For any $\mathbf{y}\in Y$ there exists a unique $\mathbf{x}\in X$ such that $$A\mathbf{x=y}$$ 

# Subspaces and Quotient Space (Not in LADW)
## Subspace
* If $V$ is a vector space, $W$ is called a subspace of $V$ 
	* is $W\subset V$ and $W$ is a vector space
* $W$ is a vector subspace iff 
	* For any $\mathbf{w_1,w_2}\in W$ and any $\alpha_1,\alpha_2\in\mathbb{R}$
	* $$\alpha_1\mathbf{w_1}+\alpha_2\mathbf{w_2}\in W$$

### Examples of Subspace
* Line in $\mathbb{R}^2$ is a subspace
* Integers in $\mathbb{R}^1$ is not a subspace since multiplication by scalar may not be an integer
* Even and odd palynomials are subspaces of polynomials
	* monic polynomials are not subspaces
* If $m\leq n$, $\mathbb{R}^m$ can be identified with a subspace of $\mathbb{R}^n$.
	* one way is to just add a bunch of zeroes to match the dimensions of $n$

### Properties
* If $m\leq n$ then $\mathbb{R}^m$ is isomorphic to a subspace of $\mathbb{R}^n$
* $V = C(\mathbb{R})$ (is a continuous function in $\mathbb{R}$

## Quotient Space
### Equivalence Relation
* Let $X$ be a set. We say that $\sim$ is at equivalence relation on $X$ if for some $x,y\in X$ we say $x\sim y$ and have $3$ properties satisfied
	* (Reflexivity) $x \sim x$
	* (Symmetry) $x \sim y \iff y \sim x$
	* (Transitivity) $x \sim y$ and $y \sim z \implies x \sim z$
* 
* $[x]=\{y\in X : y \sim x\}$ is called an equivalence class
* 
* $X$ is a disjoint union of equivalence classes
	* Any $x\in X$ belongs to some $\sim$ class and
	* two equivalence classes are either disjoint or coincide

### Example of Equivalence Relation
#### Congruence $\bmod{~n}$
* $X\in\mathbb{Z}$ and $n\in\mathbb{N}$
	* we say $x\sim y\pmod{n}$ if $n|(x-y)$

### Quotient Space
* $W\subset V$ (a vector space)
	* Define an equivalence relation on $V$ $$\mathbf{x\sim y}\iff \mathbf{x-y}\in W$$ 
	* $V$ is a disjoint union of equivalence classes $$[\mathbf{x}]=\{\mathbf{x+w;w}\in W\}$$
* A **quotient space** (factor space) of $V$ with respect to $W$ is denoted by $$V/W := \{[\mathbf{x}]; \mathbf{x}\in V\}$$
	* $V/W$ is a vector space

### Example of Quotient Spaces
#### $m< n$, $\mathbb{R}^n/\mathbb{R}^m$
* $[z]=\{\}$
* $$\mathbb{R}^n/\mathbb{R}^m\cong\mathbb{R}^{n-m}$$

#### Continuous function and continuous function through origin
* $V=C(\mathbb{R})$ (continuous functions on a real line)
* $W=C_0(\mathbb{R})=\{f\in C(\mathbb{R}):f(0)=0\}$
* $V/W \ni [f]=\{f(t)+g(t): g(0)=0\}$
* For all $f\in C(\mathbb{R})$ we have $\tilde{f}(t)=f(t)-f(0)\in W$
* $f(t)-\tilde{f}(t)=f(0)$
	* which is just a constant in $\mathbb{R}$
* $$C(\mathbb{R})/C_0(\mathbb{R}) \cong \mathbb{R}$$

#### Polynomial and even polynomial
* $\mathbb{P}_{n,\text{even}}\subset\mathbb{P}_n$
	* $\mathbb{P}_{n,\text{even}} = \{p(t)\in\mathbb{P}_n: p(-t)=p(t)\}$
* $$\mathbb{P}_{n}/\mathbb{P}_{n,\text{even}}=\mathbb{P}_{n,\text{odd}}$$

