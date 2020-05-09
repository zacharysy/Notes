# Dual Spaces
- $V$ is a vector space over $\mathbb{R}$
- The dual space to $V$, denoted by $V'$ is the space of linear functionals on $V$
	- The space of all linear maps $L:V\rightarrow\mathbb{R}$
	- $V'=\mathcal{L}(V,\mathbb{R})$
- If $\ell\in V'$ is an arbitrary lineal functional, then 
	- $\ell(\mathbf{v}) = \ell(x_1\mathbf{v_1}+\cdots+x_1\mathbf{v_1})$
	- and if let $\ell_i(\mathbf{v})=x_i$, then $$\ell(\mathbf{v})=\sum_{i=1}^n\ell_i(\mathbf{v})\ell(\mathbf{v}_i)$$

## Uniqueness Theorem (Lemma 1.3)
- Let $\mathbf{v}\in V$ 
- if $\ell(\mathbf{v})=0$ for all $\ell\in V'$
	- then $\mathbf{v}=0$
- If $\ell(\mathbf{v}_1)=\ell(\mathbf{v}_2)$ for all $\ell\in V'$
	- then $\mathbf{v}_1=\mathbf{v}_2$

## Second Dual
- The dual of $V'$ is $V''$
- Let $\varphi_{\mathbf{v}}(\ell)\in V''$, then $\varphi_{\mathbf{v}}(\ell)=\ell(\mathbf{v})$
- Let $T$ be the transformation $T:V\rightarrow V''$
- $T$ is an isomorphism, so $V''$ is isomorphic to $V$  (Reflexivity)
	- $$V\ni\mathbf{v}\rightarrow\varphi_\mathbf{v}\in V''$$
		- where $\varphi_\mathbf{v}(\ell)=\ell(\mathbf{v})$ for all $\ell\in V'$
- May not be satisfied in infinite dimensional vector spaces

## Biorthogonal Bases
- Fix a basis $\mathbf{v}_1,\cdots,\mathbf{v}_n$ in $V$
- Then $V\mathbf{v}\in V$
	- $\mathbf{v}=x_1\mathbf{v}_1+\cdots+x_n\mathbf{v}_n$ 
- Define $\ell_i\in V'$ by $\ell_i(\mathbf{v})=x_i$
- Then $$\ell_i(\mathbf{v}_j)=\delta_{i,j}$$
	- Which is the Kroneker Delta


### Definition 1.4
- $\mathbf{v}_1,\cdots,\mathbf{v}_n\in V$ a basis
- $\ell_1,\cdots,\ell_n\in V'$ are a biorthogonal basis if  they satisfy the above

#### Abstract Non-orthogonal Fourier Expansion
- $$\mathbf{v}=\sum_{i=1}^n\ell_i(\mathbf{v})\mathbf{v}_i$$
- The two bases depend on each other

# Dual of an Inner Product Space
## Riesz Representation Theorem
- If $V$ is an inner product space, 
- then for any unique vector $\mathbf{y}\in V$
- there exists a unique linear functional $\ell_y\in V'$
- such that $$\ell_y(\mathbf{x})=\langle\mathbf{x},\mathbf{y}\rangle$$
	- Converse is also true

## Isomophism between Inner Product and Dual
- The inner product space is isomorphic to its dual if the space is real
	- $V\ni\mathbf{y}\mapsto\ell_y\in V'$

# Dual Transformations and Transpose
- Define operation $(,)$ by $$\ell(\mathbf{v}) = (\ell,\mathbf{v})$$

## Dual Transformation
- Let $A:V\rightarrow W$ be a linear transformation between vector spaces
- A Dual Transformation $A':W'\rightarrow V'$ is defined by $$A'(\ell)(\mathbf{v})=\ell(A\mathbf{v})$$
- It's like the adjoint $$(\ell,A\mathbf{v})=(A'\ell,\mathbf{v})$$
- For a complex space, $A'=A^T$

## Annihilators
- Let $E$ be a subspace of the vector space $V$
- The Annihilator of $E$, denoted by $E^\perp$ is the $\ell\in V'$ such that 
- $$\ell(\mathbf{x})=0$$
	- for all $\mathbf{x}\in E$
- Basically $$E^\perp = \{\ell\in V' : \ell(\mathbf{x})=0, \forall\mathbf{x}\in E\}$$

### Proposition 3.6
- $$(E^\perp)^\perp = E$$

## Annihilators in Fundamental Subspaces (Theorem 3.7)
- For $A:V\rightarrow W$
	1. $\text{Ker }A' = (\text{Ran }A)^\perp$
	2. $\text{Ker }A = (\text{Ran }A')^\perp$
	3. $\text{Ran }A = (\text{Ker }A')^\perp$
	4. $\text{Ran }A' = (\text{Ker }A)^\perp$


# Multilinear Functions. Tensors
## Multilinear Map
- Consider vector spaces $V_1,\cdots,V_p$ and $V$
- A multilinear map, $F:V_1\times\cdots\times V_p\rightarrow V$ is a map linear in each variable
	- For all $i$ and any scalars $a,b$
		- $$F(\mathbf{v}_1,\cdots,\mathbf{v}_{i-1},a\mathbf{v}_i+b\mathbf{v}_i,\cdots,\mathbf{v}_p)=$$
		- $$aF(\mathbf{v}_1,\cdots,\mathbf{v}_{i-1},\mathbf{v}_i,\cdots,\mathbf{v}_p)+bF(\mathbf{v}_1,\cdots,\mathbf{v}_{i-1},\mathbf{v}_i,\cdots,\mathbf{v}_p)$$
- The space of Multilinear Maps is denoted by $\mathcal{L}(V_1,\cdots,V_p; V)$
	- Is a vector space

### Examples
- Linear transformations $A:V_1\rightarrow V$ are linear maps
- Bilinear Forms on $V$ is an element of $\mathcal{L}(V,V;\mathbb{R})$
- $\det([\mathbf{v}_1~\cdots~\mathbf{v}_n])$, where $\mathbf{v}_i\in\mathbb{R}^n$ is an n-nlinear map from $\mathbb{R}^n\times\cdots\times\mathbb{R}^n\rightarrow\mathbb{R}$

### Dimension of $\mathcal{L}(V_1,\cdots,V_p; V)$
- $$\dim{\mathcal{L}(V_1,\cdots,V_p; V)} = (\dim V_1)\cdots(\dim V_p)(\dim V)$$

### Multilinear Functionals
- a multilinear map defined as $\mathcal{L}(V_1,\cdots,V_p,\mathbb{R})$
	- Could also be in $\mathbb{C}$
- So $$\dim \mathcal{L}(V_1,\cdots,V_p,\mathbb{R}) = (\dim V_1)\cdots(\dim V_p)$$

### Tensor Product of Functionals
- Let $f_1\in V_1',\cdots,f_p\in V_p'$
- Define $(f_1 \otimes\cdots \otimes f_p)\in \mathcal{L}(V_1,\cdots,V_p,\mathbb{R})$ by $$(f_1 \otimes\cdots \otimes f_p)(\mathbf{v}_1,\cdots,\mathbf{v}_p) = f_1(\mathbf{v}_1)\cdots f_p(\mathbf{v}_p)$$

### Proposition 5.2
- Let $\{b_i\}_{i=1}^{\dim V_k}$ be a basis of $V_k$
- and $\{\ell_i^k\}_{i=1}^{\dim V_k}$ be a dual basis of $V_k'$
- Consider all possible $\ell_{i_1}^1 \otimes \cdots \otimes \ell_{i_p}^p$
	- these multilinear functionals form a basis of $\dim \mathcal{L}(V_1,\cdots,V_p,\mathbb{R})$


## Tensor Products of Vector Spaces
* Let $V_1,\cdots,V_p$ be vector spaces
* the tensor product $$V_1\otimes \cdots \otimes V_p$$ is defined as $\mathcal{L}(V_1,\cdots,V_p,\mathbb{R})$

### Basis
* A basis of $V_1\otimes \cdots \otimes V_p$ is formed by the system $$b_{j_1}^1\otimes\cdots\otimes b_{j_p}^p$$ for all possible $j_1,\cdots,j_p$

### Example
* Let $F\in\mathcal(V_1,\cdots,V_p;V)$ a multilinear map
* then there exists a unique linear transformation $T:V_1\otimes\cdots\otimes V_p\rightarrow V$ 
* such that $$F(\mathbf{v}_1,\cdots,\mathbf{v}p)=T(\mathbf{v}_1\otimes\cdots\otimes\mathbf{v}_p)$$
	* for all $\mathbf{v}_1\in V_1, \cdots \mathbf{v}_p \in V_p$