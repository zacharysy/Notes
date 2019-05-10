# Chapter 12: Inverse Functions

## Injection
$f$ is **Injective** (one-to-one) if 
$$x\neq y \in Dom(f) \implies f(x)\neq f(y)$$

* All $x$ has one unique $y$ and vice versa 

## Surjection
$f$ is **surjective** (onto) if 
$$\forall y \in \text{codomain}(f), \exists x\in \text{Domain}(f), f(x)=y$$

* Each $y$ in $f$ is hit by an $x$ at least once
* Meaning, codomain is equal to range

## Bijection
$f$ is **bijective** if it is injective and surjective

* domain and codomain has a perfect one-to-one correspondence


## Inverse Function ($f^{-1}$)
When $f$ is injective, can form new function from $f$ because $f=\{(a,b):a\in Dom(f)\}$

### New Function:
$$f^{-1}=\{(b,a):a\in Dom(f)\}$$

* $f^{-1}$ is the *inverse* of $f$, $f$ is *invertible*
	* $f^{-1}$ is a function $\iff$ $f$ is injective

### Properties of Inverse Functions
* $f^{-1}$ has domain equal to range of $f$ and range equal to domain of $f$
* $f^{-1}$ itself is invertible, and $(f^{-1})^{-1}=f$
* $f(f^{-1}(x))=x$ (Identity function on range of $f$)
* $f^{-1}(f(x))=x$ (Identity function on domain of $f$)
	* though $f(f^{-1}(x))\neq f^{-1}(f(x))$ because different domains

### Example of Invertible Functions
1. If $f$ is increasing on its domain, then $f^{-1}$ exists and is also increasing
	* Since $\forall x,y \in \text{Domain}(f), f(x) < f(y)$
2. If $f$ is decreasing on its domain, then $f^{-1}$ exists and is also decreasing
3. Any other invertible function is **weird**
	* Any function you can make from another invertible function with a bunch of points swapped

#### Theorem:
* Suppose $f:I\rightarrow\mathbb{R}$ is defined on an *interval* $I$, and $f$ is continuous. 
* If $f$ is invertible, then it is monotone

### Graph of $f^{-1}$
Reflection of the graph of $f$ across line $x=y$

#### Horizontal Line Test
Shows if function is invertible

### Domain and Range
* Range + Domain of $f^{-1}$, when $f:I\rightarrow\mathbb{R}$, continuous, $I$ an interval, $f$ is invertible
	* If $I=[a,b]$, $f$ is increasing
		* Range of $f$ is $[f(a),f(b)]$
	* If $I=[a,\infty]$, $f$ is increasing
		* Range of $f$ is $(\inf\{f(x):x\in(a,\infty)\},\sup\{f(x):x\in(a,\infty)\})$
			* allowing $+\infty$ as $\sup$ and $-\infty$ as $\inf$

### Theorem 1 (Continuity)
* if $f:I\rightarrow\mathbb{R}$ is continuous, invertible, then 
	* $f^{-1}$ is continuous on its domain
* For $b \in \text{Domain}(f^\prime), f^{-1}$ is differentiable at $b$ except when $f'(f^{-1}(b))=0$

### Theorem 2 (Differentiability)
* if $f:I\rightarrow\mathbb{R}$ is continuous, invertible, and differentiable, then
	* if $f'(f^{-1}(b))=0$, $f^{-1}$ is not differentiable at $b$
	* if $f'(f^{-1}(b))\neq0$, $f^{-1}$ is differentiable at $b$ and
	* $$(f^{-1})'(b)=\frac{1}{f'(f^{-1}(b))}$$


