# Midterm 2
## Test Format
1. 6 Quizlike question
2. Problem Similar to one of the proofs of the theorems 
3. Homework Exercise
4. Homework-Like Exercise

## Key Concepts
### Compactness
* $K\subset\mathbb{R}^n$ is compact iff
	* HB: Every open cover of $K$ has a finite subcover
	* BW: Every sequence in $K$ has a convergent subsequence
	* $K$ Closed & Bounded
* Closure of a bounded set is bounded and so is compact

### Bolzano Weierstrauss
* $K\subset\mathbb{R}^n$ compact and nonemtpy
* $f:K\rightarrow\mathbb{R}$ is continuous
	* then $\exists x^\alpha\in K$ such that $$f(x)\leq f(x^\alpha)$$ for all $x\in K$

#### Proof
* Let $M=\sup_{x\in K} f(x)$
	* then there exists a sequence of points in $K$ such that $f(x_{\nu})\nearrow M$ (Important, called a maximizing sequence)
* $(x_{\nu})$ has a convergent subsequence $x_{\nu_k}\rightarrow x^*\in K$
* So $$\lim_{\nu\rightarrow\infty}f(x_\nu)=\lim_{\nu\rightarrow\infty}f(x_{\nu_k})=f(x^*)$$

#### Proof Part 2
* $f:\mathbb{R}^n\rightarrow\mathbb{R}$
* $S\subset\mathbb{R}^n$ is bounded
* prove that $$\sup_{x\in S} f(x) < \infty$$
	* Since $S$ is bounded, then the sup is contained in a closed ball
* Therefore since $K$ is bounded, sup is finite and can be reached by a sequence

### Differential Calculus
* Key concept is the Differential
* Differential is dependent on a function that is defined in an open set
* $F:U\subset_{\text{open}} \mathbb{R}^m\rightarrow\mathbb{R}^n$
* $x_0\in U$
* the differential of $F$ at $x_0$ is a linear operator $L:\mathbb{R}^n\rightarrow\mathbb{R}^m$ such that
* $$\lim_{h\rightarrow 0}\frac{1}{\lVert h \rVert}(F(x_0-h)-F(x_0)-Lh)=0$$
* $J_F(x_0)$ is the matrix representation of the differential, an $m\times n$ matrix.
* Determine the matrix by the partials
	* $$J_F(x_0)=[\partial_{x^1}F,\cdots, \partial_{x^n}F ]^T$$
	* $$\frac{\partial F}{\partial x^n} = \lim_{t\rightarrow 0}\frac{1}{t}(F(x_0+te^n)-F(x_0))$$
* Differential exists implies that partials exists
	* Converse not true
* Theorem: If partials exists in $U$ and are continuous at $x_0$ then $F$ is differentiable at $x_0$
	* $F\in C^1(U)$ means that $F$ and its partials are continuous on $U$
* Chain Rule
	* $d(G\circ F)=dG\circ dF$
	* (useful trick) $r:\mathbb{R}^n\setminus\{0\}\rightarrow\mathbb{R}$ 
		* $r(x)=\lVert x \rVert$
		* $$\frac{\partial r}{\partial x^1}=\frac{x^1}{r}$$
* $U\subset\mathbb{R}^n$ open
* $F:U\rightarrow\mathbb{R}$
* $\gamma(t):I\rightarrow U$ is a path
	* $$\frac{df}{dt}(\gamma(t))=\frac{df}{dt}(x^1(t),\cdots,x^n(t))$$
	* $$=\frac{\partial f}{\partial x^1}\dot{x}^1+\cdots+\frac{\partial f}{\partial x^n}\dot{x}^n$$
	* this is equal to $$\lang \nabla f, \dot{\gamma} \rang$$
* Lagrange MVT
	* $U\subset\mathbb{R}^n$ open and convex
	* $F:U\rightarrow\mathbb{R}$ continuous
	* There exists $p\in[p_0,p_1]$
	* $$F(p_0)-F(p_1)=\lang \nabla f(p), p_1-p_2 \rang$$
* Consequences of Lagrange MVT (Important)
	* If $F$ is $C^1$ and $\nabla f$ is $0$, then the function is constant
	* If $F$ is $C^1$ and $\nabla f$ is bounded, so $\lVert \nabla f \rVert < L$ for all $x\in U$, then the function is Lipschitz
		* $$|f(p_1)-f(p_0)|\leq L\lVert p_1-p_0 \rVert$$
		* Have control of the growth of $F$

