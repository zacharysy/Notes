# Exam 1

## 4 Problems
### Problem 1
* 6 Quiz-like questions

### Problem 2
* One of the theorems

### Problem 3 & 4
* Homework Problems


## Review
### Topics
* Implicit Function Theorem
	* Know how to use
* Submanifolds
* Change in Coordinates


### Implicit Function Theorem
* $F^1(x^1,x^2,\cdots,x^5)=0$
* $F^2(x^1,x^2,\cdots,x^5)=0$

#### Need
* $Z=\{\mathbf{x}: F(\mathbf{x})=0\}$
	* Set of solutions of the system
	* A submanifold of dimension 3 (dimension of kernel)
* $F(x)=0\in\mathbb{R}^2$
* $J_F(x)\in Z$
* rank of $J_F$ is $2$
* A vector is tangent if it is equal to the velocity of a C^1 path through that point
	* Tangent space is the kernel of the jacobian

### Fermat Principle of Submanifolds
* If $\mathbf{x}$ is an extremum point, then the gradient of $\mathbf{x}$ at that point is orthogonal to the tangent plane

### Lagrange Multipliers
* Maximize $f(x^1,\cdots,x^5)$ subject to the above constraints
* Used IFT to show that submanifold exists with jacobian rank $2$
* there exists $\lambda_1,\lambda_2$, such that $\nabla f = \lambda_1 F^1 + \lambda_2 F^2$
	* Saying that the gradients of $F^1$ and $F^2$ are orthogonal to the surface

### Integration
* $B\subset\mathbb{R}^n$
* $f:B\rightarrow\mathbb{R}$
* $f$ is riemann integrable iff
	* $f$ is bounded
	* $$\inf_P S^*(f,P)=\sup_Q S_*(f,Q)$$
		* $$S^*(f,P)=\sum_{C\in\mathcal{C}(P)}\sup_{x\in C} f(x)\text{vol}_n(C)$$
		* $$S_*(f,P)=\sum_{C\in\mathcal{C}(P)}\inf_{x\in C} f(x)\text{vol}_n(C)$$
* $\int_B f(x)~dx = I$
	* let $I=\inf_P S^*(f,P)$, if for all $\varepsilon > 0$, there exists a partition $P_\varepsilon$ such that $$S^*(f,P_\varepsilon)< I+\varepsilon$$ and there exists a $Q_\varepsilon$ such that $$I-\varepsilon< S_*(f,Q_\varepsilon)$$

### Determining Function integrable
#### Darboux Theorem
* $f:B\rightarrow\mathbb{R}$ is bounded
* $f$ is integrable if for all $\varepsilon > 0$, there exists a partition $P$ such that $\omega(f,P)<\varepsilon$
	* where $$\omega(f,P)=\sum_C\text{osc}(f,C)\text{vol}_n(C)$$

#### Lesbegue
* A function is integrable on a box if the set of discontinuities is negligible

#### Negligible
* Can be covered in a countable family of boxes such that sum of volumes less than epsilon

### Integrable over $\mathbb{R}^n$
* $f:\mathbb{R}^n\rightarrow\mathbb{R}$
* $f$ is integrable if there exists a box such that $f|_B$ is integrable 
* $f(x)=0$ for all $\mathbb{x}\in\mathbb{R}^n\setminus B$
* $$\int_\mathbb{R}^n f~dx=\int_B f~dx$$

### Integrable over $S$
* $f:S\rightarrow\mathbb{R}$ is integrable if $f^0$ is integrable over $\mathbb{R}^n$
	* Where $f^0$ is the extension by $0$
* $\int_S f~dx = \int_{\mathbb{R}^n}f^0~dx~\text{vol}_nC$

### Jordan measurable
* $S$ is jordan measurable iff $I_S$ is integrable
* If $S$ is between a graph of continuous functions then it is integrable
* The union of domains of simple type are jordan measurable