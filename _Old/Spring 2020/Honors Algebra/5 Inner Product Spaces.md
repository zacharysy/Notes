# Inner Product in $\mathbb{R}^n$ and $\mathbb{C}^n$
* In abstract Vector Space, there is no notion of angle or distance (only addition and subtraction), so define an inner product space
## Inner Product ($\mathbb{R}$)
* $V$ is a real vector space
* An inner product is a function $V\times V\rightarrow\mathbb{R}$, 
	* $(\mathbf{v,w})\rightarrow \langle \mathbf{v,w} \rangle$

### Properties
#### Symmetry
* $$\langle\mathbf{v,w}\rangle=\langle\mathbf{w,v}\rangle$$

#### Linear
* $$\langle\mathbf{\alpha v_1+\beta v_2,w}\rangle=\alpha\langle\mathbf{v_1,w}\rangle + \beta\langle\mathbf{v_2,w}\rangle$$

#### Nonnegative
* $$\langle\mathbf{v,v}\rangle \geq \mathbf{0}$$

#### Nondegenerate
* $$\langle\mathbf{v,v}\rangle = \mathbf{0} \implies \mathbf{v=0}$$

### Norm
* A function $V\rightarrow [0,\infty)$
* $\mathbf{v}\rightarrow\lVert\mathbf{v}\rVert$
* $$\lVert\mathbf{v}\rVert=\sqrt{\langle\mathbf{v,v}\rangle}$$
* generalization of length

### Standard Inner Product
* $\mathbb{R}^n$ are column vectors
* $$\langle\mathbf{x,y}\rangle = \mathbf{x}^T\mathbf{y}$$
* consequently
* $$\lVert\mathbf{v}\rVert = \sqrt{\mathbf{x}^T\mathbf{x}}=\sqrt{\sum_{k=1}^n{x_k^2}}$$

## Inner Product ($\mathbb{C}$)
* Basically the same as $\mathbb{R}$
* $W$ is a complex vector space 
* A (Hermitian) inner product is a function $W\times W\rightarrow\mathbb{C}$, 
	* $(\mathbf{w_1,w_2})\rightarrow \langle \mathbf{w_1,w_2} \rangle$
* $$\langle\mathbf{x,y}\rangle=\sum_{i=1}^n{x_i\overline{y_i}}$$

### Properties
* Mostly the same as reals
#### Symmetric (Hermitian)
* $$\langle\mathbf{u,v}\rangle=\overline{\langle\mathbf{v,u}\rangle}$$

#### Linear (Hermitian)
* $$\langle\mathbf{v,\alpha w}\rangle=\overline{\alpha}\langle\mathbf{v,w}\rangle$$

### Standard Hermitian Inner Product (Example 1.1)
* $\mathbb{C}^n$ are column vectors
* $$\langle\mathbf{v,w}\rangle = \mathbf{v}^T\overline{\mathbf{w}}=\overline{\mathbf{w}}^T\mathbf{v}=\mathbf{w}^*\mathbf{v}$$

### Hermitian Adjoint
* If $A$ is a complex matrix, then $$A^*=\overline{A}^T$$

### Norm
* $W\rightarrow [0,\infty)$
* $\mathbf{v}\rightarrow\lVert\mathbf{w}\rVert$
* $$\lVert\mathbf{w}\rVert=\sqrt{\langle\mathbf{w,w}\rangle}=\sqrt{\sum_{k=1}^n{|w_k|^2}}$$
* Is always real

### Inner Product of Complex Polynomials (Example 1.2)
* Let $W$ be complex polynomials of degree $\leq n$
	* complex vector space with dimension $n+1$
* $$\langle f,g\rangle = \int_{-1}^1f(t)\overline{g(t)}~dt$$

### Frobenius Inner Product (Example 1.3)
* $M_{m\times n}$ complex matrices
	* complex vector space if dimension $mn$
* $$\langle A, B \rangle =\text{tr}(B^* A)$$

## Properties of Inner Product
### Lemma 1.4
* For all $\mathbf{y}$
* $$\langle\mathbf{x,y}\rangle = 0 \iff \mathbf{x=0}$$

### Corollary 1.6
* $A,B:V\rightarrow W$ are linear maps
* $W$ is an inner product space
* if for all $\mathbf{x}\in V$ and $\mathbf{y}\in W$
	* $$\langle A\mathbf{x,y}\rangle = \langle B\mathbf{x,y}\rangle$$ 
* Then $A=B$

### Cauchy-Schwartz Inequality (Theorem 1.7)
* $$| \langle \mathbf{x},\mathbf{y} \rangle |\leq \lVert\mathbf{x}\rVert \lVert\mathbf{y}\rVert$$

### Triangle Inequality (Lemma 1.8)
* $$\lVert \mathbf{x+y}\rVert\leq\lVert \mathbf{x}\rVert+\lVert \mathbf{y}\rVert$$

### Parallelogram Identity (Lemma 1.10)
* $$\lVert\mathbf{x+y}\rVert^2+\lVert\mathbf{x-y}\rVert^2=2(\lVert\mathbf{x}\rVert^2+\lVert\mathbf{y}\rVert^2)$$

### Polarization Identities (Lemma 1.9)
* All the information about the inner product is contained in the norm

#### Real Case
* $$\langle\mathbf{x,y}\rangle=\frac{1}{4}(\lVert\mathbf{x+y}\rVert^2-\lVert\mathbf{x-y}\rVert^2)$$

#### Complex Case
$$\langle\mathbf{x,y}\rangle=\frac{1}{4}(\lVert\mathbf{x+y}\rVert^2-\lVert\mathbf{x-y}\rVert^2+i\lVert\mathbf{x}+i\mathbf{y}\rVert^2-i\lVert\mathbf{x}-i\mathbf{y}\rVert^2)$$

## Normed Spaces
* Inner product space always has a norm with the properties:
	1. Homogeneity
		* $$\lVert\alpha\mathbf{x}\rVert=|\alpha|\lVert\mathbf{x}\rVert$$
		* for all $\alpha\in\mathbb{R}\cup\mathbb{C}$
	2. Triangle Inequality
		* $$\lVert \mathbf{x+y}\rVert\leq\lVert \mathbf{x}\rVert+\lVert \mathbf{y}\rVert$$
	3. Non-Negativity
		* $$\lVert \mathbf{x}\rVert\geq 0$$
	4. Non-degeneracy
		* $$\lVert \mathbf{x}\rVert= 0 \iff \mathbf{x=0}$$
* Can be generalized into a norm vector space

### Definition
* A norm on a (real or complex) vector space is a function $\lVert\cdot\rVert:V\rightarrow\mathbb{R}$, $\mathbf{v}\mapsto\lVert\mathbf{v}\rVert$ satisfying the above properties
* This vector space is called a __normed__ vector space
	* Example: inner product spaces are normed vector spaces

### P-norms ($L_p$)
* On $\mathbb{R}^n$ or $\mathbb{C}^n$
* for $1\leq p < \infty$
* define $L^p$ norm
	* $$\lVert\mathbf{x}\rVert_p=\left(\sum_{k=1}^n|x_k|^p\right)^{\frac{1}{p}}$$
* If $p=\infty$
	* $$\lVert\mathbf{x}\rVert_\infty=\max_{k=1,\cdots,n}\{|x_k|\}$$
* Satisfies all the properties of normed spaces

#### Shapes when $\lVert\mathbf{x}\rVert_p=1$
* $p=1$
	* a square
* $p=2$
	* is the norm we know
	* is a circle
* $2 < p < \infty$
	* turns into a squircle, approaches the bigger square
* $p=\infty$
	* is a bigger square

### Theorem 1.11
* A norm in a normed space is obtained from some inner product iff it satisfies the parallelogram inequality
	* Which is only $\lVert\cdot\rVert_2$


# Orthogonality
* Inner product exists iff angles in a vector space

## Orthogonal (Definition 2.1)
* $\mathbf{u,v}\in V$ 
* in a vector space $V$ with an inner product
* $\mathbf{u}$ is orthogonal to $\mathbf{v}$ ($\mathbf{u\perp v}$) if
	* $\langle \mathbf{u,v} \rangle =0$

## Orthogonal to Subspace (Definition 2.2)
* If $E\subset V$ is a linear subspace
* then $\mathbf{v}\perp E$ if
	* $$\langle \mathbf{v,w} \rangle = 0$$
	* for all $\mathbf{w}\in E$

## Orthogonal Subspaces
* If $E,F\subset V$ are two linear subspaces
* then $E\perp F$ if
	* $$\langle \mathbf{v,w} \rangle = 0$$
	* for all $\mathbf{v}\in E,\mathbf{w}\in F$

## Orthogonal System (OS)
* $\mathbf{v_1,\cdots,v_k}\in V$ is an orthogonal system if
	* $$\langle \mathbf{v_i,v_j}\rangle = 0$$
	* $i\neq j$

### Orthogonal Basis
* $\mathbf{v_1,\cdots,v_k}\in V$ is an orthogonal basis if it is OS and a basis

### Orthonormal Basis (ONB)
* An orthogonal basis is called orthonormal if every vector has a norm

### Generalized Pythagorean Identity (Lemma 2.5)
* If $\mathbf{v_1,\cdots,v_n}$ is an orthogonal system then 
	* $$\left\lVert\sum_{k=1}^n a_k\mathbf{v}_k\right\rVert=\sum_{k=1}^n |a_k|^2\left\lVert\mathbf{v}_k\right\rVert^2$$
* If the system is orthonormal basis, $\lVert\mathbf{v_k}\rVert=1$ and so the sum is equal to $$\sum_{k=1}^n |a_k|^2$$

### Finite Dimensional Fourier Expansion
* If $\mathbf{v_1,\cdots,v_n}$ is an orthonormal basis then 
* $$\mathbf{v}=\sum_{i=1}^n\langle\mathbf{v,v_i}\rangle \mathbf{v}_i$$

# Orthogonal Projection and Gram-Schmidt Orthogonalization

## Orthogonal Projection (Definition 3.1)
* Let $\mathbf{v}\in V$
* $E\subset V$ is a subspace
* then an orthogonal projection of $\mathbf{v}$ to $E$ is a vector $\mathbf{v}_E$ such that
	1. $\mathbf{v}_E\in E$
	2. $(\mathbf{v-v}_E) \perp E$ 

### Existence and Uniqueness (Theorem 3.2)
1. If $\mathbf{x}\in E$ then
	* $$\lVert\mathbf{v-v}_E\rVert\leq\lVert\mathbf{v-x}\rVert$$
2. if $\lVert\mathbf{v-v}_E\rVert=\lVert\mathbf{v-x}\rVert$ then
	* $$\mathbf{x=v}_E$$

## How to Compute $\mathbf{v}_E$
* Pick an orthonormal basis $\mathbf{w_1,\cdots,w_k}\in E$.
* then $$\mathbf{v-v}_E \perp E \iff \langle\mathbf{v-v}_E,\mathbf{w}_i\rangle=0$$
* and so $$\langle\mathbf{v}_E,\mathbf{w}_i\rangle=\langle\mathbf{v},\mathbf{w}_i\rangle$$
* therefore $$\mathbf{v}_E = \sum_{i=1}^k\langle\mathbf{v,w}_i\rangle\mathbf{w}_i$$

### Generally
* $$P_E\mathbf{v} = \sum_{k=1}^r{\frac{\langle\mathbf{v,w_k}\rangle}{\lVert\mathbf{w}_k\rVert^2}\mathbf{w}_k}$$
* where $P_E$ can be seen as a linear operator, such that $$P_E = \sum_{k=1}^r{\frac{1}{\lVert\mathbf{w}_k\rVert^2}\mathbf{w}_k\mathbf{w}_k^*}$$

## Gram-Schmidt Orthogonalization
* $V$ is a vector space with inner product
* $\mathbf{v_1,\cdots,v_n}$ is a basis in $V$
* Building an ONB $\mathbf{e_1,\cdots,e_n}$ from $\mathbf{v_1,\cdots,v_n}$ in such a way that for any $i=1,\cdots,n$ $$\text{span}(\mathbf{v_1,\cdots,v_i})=\text{span}(\mathbf{e_1,\cdots,e_i})$$
* To build orthonormal basis:
	1. $\mathbf{e}_1=\frac{1}{\lVert\mathbf{v}_1\rVert}\mathbf{v}_1$
	2. Then find $c_{2,1}$ such that $$\mathbf{v}_2-c_{2,1}\mathbf{e}_1 \perp \mathbf{e}_1$$
		* and so $\langle\mathbf{v_2,e_1}\rangle=c_{2,1}$
		* therefore $$\mathbf{e}_2=\frac{\mathbf{v_2-\langle v_2,e_1 \rangle e_1}}{\lVert\mathbf{v_2-\langle v_2,e_1 \rangle e_1}\rVert}$$
	3. Then find $c_{3,1},c_{3,2}$ such that $$\mathbf{v}_3-c_{3,1}\mathbf{e}_1-c_{3,2}\mathbf{e}_2 \perp \mathbf{e}_1,\mathbf{e}_2$$
		* and so like part 2
		* $$\mathbf{e}_3=\frac{\mathbf{v_3-\langle v_3,e_1 \rangle e_1-\langle v_3,e_2 \rangle e_2}}{\lVert\mathbf{v_3-\langle v_3,e_1 \rangle e_1-\langle v_3,e_2 \rangle e_2}\rVert}$$

* So for any $i$
	* $$\mathbf{e}_i=\frac{\mathbf{v_i-\sum_{j=1}^{i-1}\langle v_i,e_j \rangle e_j}}{\lVert\mathbf{v_i-\sum_{j=1}^{i-1}\langle v_i,e_j \rangle e_j}\rVert}$$

### Example (Legendre Polynomials)
* $\mathcal{P}_n$ is a polynomial of degree at most n over $\mathbb{R}$
* $\langle p(t), q(t) \rangle = \int_{-1}^1p(t)q(t)~dt$
* if $\mathbf{v}$ is the standard basis, then using gram-schmidt
	* $\mathbf{e_1} = \frac{1}{\sqrt{2}}$
	* $\mathbf{e_2} = \sqrt{\frac{3}{2}}t$
	* $\mathbf{e_3} = c_{3,2}t^2+c_{3,0}$
	* $\vdots$
	* $\mathbf{e_{2k}} = c_{2k,2k-1}t^{2k-1}+c_{2k,2k-3}t^{2k-3}+\cdots$
	* $\mathbf{e_{2k+1}} = c_{2k+1,2k}t^{2k}+c_{2k+1,2k-2}t^{2k-2}+\cdots$
* let $\mathbf{e_k} = P_{k-1}(t)$, then $tP_{k}\perp P_i$  for $i=0,\cdots,k-2$

## Orthogonal Complement
* The orthogonal complement of $E$ in $V$ is $$E^{\perp}=\{\mathbf{v:v}\perp E\}$$
* $E^{\perp}$ is a subspace in $V$
	* any linear combination of $\mathbf{v}\in E^{\perp}$ is orthogonal to $E$
* $V=E\oplus E^{\perp}$
	* for all $\mathbf{v}\in V$
	* there exists unique $\mathbf{u}\in E$ and $\mathbf{w}\in E^\perp$ such that
		* $\mathbf{v=u+w}$

### Proposition 3.6
* $$(E^\perp)^\perp=E$$

## Adjoint Transformation
* Let $A:V\rightarrow V$ be a linear transformation
* Then an adjoint transformanion $A^*$ is defined by $$\langle A\mathbf{v,w}\rangle=\langle\mathbf{v},A^*\mathbf{w}\rangle$$
* For standard inner product over $\mathbb{R}$, $$A^* = A^T$$
* For standard inner product over $\mathbb{C}$, $$A^* = \overline{A}^T$$

### Computing $A^*$
* Pick an ONB $\mathbf{e_1,\cdots,e_n}$ in $V$
* $$\langle A\mathbf{e_i,e_j}\rangle=\langle\mathbf{e_i},A^*\mathbf{e_j}\rangle$$
* $$a_{ji}=\langle A\mathbf{e_i,e_j}\rangle=\langle\mathbf{e_i},A^*\mathbf{e_j}\rangle=\overline{a^*}$$
* $$A^* = (\overline{a_{ji}})^{n~~~~~n}_{i=1~j=1}$$

### Remark
* $V$ with inner product $\langle\cdot\rangle_v$
* and $W$ with inner product $\langle\cdot\rangle_w$
* $A:V\rightarrow W$
* $$\langle A\mathbf{v,w}\rangle_w=\langle\mathbf{v},A^*\mathbf{w}\rangle_v$$

# Least Square Approximation
* Finding solution when solution doesn't exist
* $$A\mathbf{x=b}$$
* $A$ is $m\times n$
* to find approximate solution $$\lVert A\mathbf{x-b}\rVert$$ should be minimized

## Calculus Approach
* minimize $$\lVert A\mathbf{x-b}\rVert^2=\sum_{i=1}^n\left|\sum_{j=1}^n{a_{ij}x_j=b}\right|^2$$ by taking partial derivatives

## Geometric Approach
* Since no solution, $\mathbf{b}\notin \text{Ran }A$
* So closest approximation in $\text{Ran }A$ would be the orthogonal projection of $\mathbf{b}$ onto $\text{Ran }A$
* Solve $$A\mathbf{x}=\text{Proj }_{\text{Ran }A}\mathbf{b}$$

## Better Geometric Approach
* Let $\mathbf{v=b-}A\mathbf{x}$
* By definition, $\mathbf{v}\perp \text{Ran }A$ 
	* and so is equal to the span of the columns of $A: \mathbf{a_1,\cdots,a_n}$ 
* Therefore $$\langle\mathbf{b-}A\mathbf{x,a_i}\rangle=0$$
* and so $$A^*(\mathbf{b-}A\mathbf{x})=0$$
* which is equivalent to 
	* $$(A^*A)\mathbf{x}=A^*\mathbf{b}$$
* which is guaranteed to have a solution
* 
* If $A^*A$ is invertible then there is a unique solution
* For $A^*A$ to be invertible, need
	* $m\geq n$
	* $\text{rank }A = n$
	* 
* And so $$\text{Proj }_{\text{Ran }A}\mathbf{b}=A(A^*A)^{-1}A^*\mathbf{b}$$


## Properties of Orthogonal Projection Matrix
* $P^2=P$
* $P^*=P$