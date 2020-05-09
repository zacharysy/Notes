# Final

* 8 quizlike questions
* 1 proof theorem
* Critical points problem
* Chapter 12 problem
* Implicit Function problem
* Derivating Problem


## Convergence
* Key concept in analysis 
* For something to converge to something else, their distance must get to $0$
	* concept of distance is norm
* $\mathbf{x}_\nu\in\mathbb{R}^n$
	* $$\mathbf{x}_\nu\rightarrow\mathbf{x} \iff \lVert\mathbf{x}_\nu-\mathbf{x}\rVert \rightarrow 0$$
	* For all $\varepsilon > 0$, there exists $N=N(\varepsilon)$ such that for all $\nu > N$, 
		* $$\lVert\mathbf{x}_\nu-\mathbf{x}\rVert < \varepsilon$$
* Convergence without knowing limit
	* Cauchy
	* $(\mathbf{x}_\nu)$ converges iff it is cauchy
	* $$\forall\varepsilon >0~\exists N = N(\varepsilon)~\forall \mu,\nu> N:$$
		* $$\lVert\mathbf{x}_\mu-\mathbf{x}_\nu\rVert<\varepsilon$$


### Openness
* $U$ is open if
	* For all $\mathbf{p}$ in $U$, there exists $r>0$, such that
		* $B_r(\mathbf{p})\subset U$
* $C$ is closed if
	* For all $\mathbf{p}$ not in $U$, there exists $r>0$, such that
		* $B_r(\mathbf{p})\cap C \neq \emptyset$
	* The limit of any convergence sequence of points in $C$ is a point in $C$


## Compactness
* Closed and Bounded
* Bolzano Weierstrauss
	* Any sequence of points in the set contains a convergent subset where the limit is in the set
* Heine Borel
	* Any collection of open sets that cover the set contains a finite collection of open sets that cover the set

## Continuity
* For any $\varepsilon > 0$, there exists a $\delta = \delta(\varepsilon)$, such that for all $\mathbf{x}\in X$
	* $$\lVert\mathbf{x}-\mathbf{x}_0\rVert < \delta \implies \lVert F(\mathbf{x})- F(\mathbf{x}_0)\rVert < \varepsilon$$
	* $$\mathbf{x}_\nu\rightarrow\mathbf{x}_0 \implies F(\mathbf{x}_\nu)\rightarrow F(\mathbf{x}_0)$$
	* $$\mathbf{x}\in B_\delta(\mathbf{x_0})\implies F(\mathbf{x})\in B_\varepsilon(F(\mathbf{x}_0))$$
* $F:\mathbb{R}^m\rightarrow\mathbb{R}^n$
	* $F$ is continuous
	* $F^{-1}(U)$ is open for all $U\subset\mathbb{R}^n$ open
	* $F^{-1}(C)$ is closed for all $C\subset\mathbb{R}^n$ closed
* If $F:\mathbb{R}^n\rightarrow\mathbb{R}$,
	* then it is easy to check if a set in $\mathbb{R}^n$ is closed or open if $F$ is defined by an inequality because $>,<$ are open, and $\leq, \geq$ are closed


## Tutorial
* Linear Functionals
	* Affine subspaces of $\mathbb{R}^n$
* Continuous functions $f:U\rightarrow\mathbb{R}^m$
* Open/Closed Subsets
* Compact Set
	* Open Cover
	* Closed and Bounded 
	* Sequences
* Differential of $F:U\rightarrow\mathbb{R}^m$ at $\mathbf{x}_0$
	* $F$ is differentiable at $\mathbf{x}_0$ if 
		* there exists a linear map $A:\mathbb{R}^n\rightarrow\mathbb{R}^m$ such that
			* $$\lim_{\lVert\mathbf{h}\rVert\rightarrow\mathbf{0}}\frac{\lVert F(\mathbf{x_0+h})-F(\mathbf{x}_0-A\mathbf{h})\rVert}{\lVert\mathbf{h}\rVert}=0$$
* Critical Point
	* $f:\mathbb{R}^n\rightarrow\mathbb{R}$ is $C^1$
	* $\mathbf{x}\in\mathbb{R}^n$ is a critical point if $\nabla f(\mathbf{x})=0$
* Local Extrema
	* $\mathbf{x}$ is a local maximum if there exists a $\delta > 0$ such that for any $\mathbf{y}\in B_\delta(\mathbf{x})$, $$f(\mathbf{y})\leq f(\mathbf{x})$$
* $C^1$ Diffeomorphisms
	* $C^1$ map that has an inverse that is also $C^1$