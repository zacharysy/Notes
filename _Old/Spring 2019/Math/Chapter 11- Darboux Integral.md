# Chapter 11: Darboux Integral

## Integral
* Motivation: Area

## Convention
* $f :[a,b] \rightarrow \mathbb{R}$
* $f$ is bounded

## Definitions

### Partition $P$ of $[a,b]$
* A sequence (finite) $(t_0,t_1,t_2,...,t_n)$ satisfies $a=t_0 < t_1 < t_2 < ... < t_n=b$
	* $m_i = \inf\{f(x):x\in[t_{i-1},t_i]\}$
	* $M_i = \sup\{f(x):x\in[t_{i-1},t_i]\}$

### Lower Darboux Sum
* $$L(f,P)=\sum^n_{i=1}m_i(t_i-t_{i-1})$$
* Near underestimate of area
 
### Upper Darboux Sum
* $$U(f,P)=\sum^n_{i=1}M_i(t_i-t_{i-1})$$
* Near overestimate of area

### $L(f,P)\leq U(f,P)$
* Lower Darboux Sum is always less than or equal to Upper Darboux Sum for a partition $P$
 
### If $P,Q$ are any partitions of $[a,b]$, then $L(f,P)\leq U(f,Q)$
* All possible LDS is less than or equal to all possible UDS
* Set of LDS is nonempty and bounded above and therefore has a $\sup$
* Set of UDS is nonempty and bounded below and therefore has a $\inf$
* $\sup{LDS}\leq\inf{UDS}$
	* If they are equal then the function is integrable 
		* else they are not
* $L(f,P)\leq L(f,P\cup Q) \leq U(f,P\cup Q) \leq U(f,Q)$

### Darboux Integral
* __Define__
	* $L(f)=\sup\{L(f,P):$ P over all partitions $\}$
	* $U(f)=\inf\{L(f,P):$ P over all partitions $\}$
	* $L(f),U(f)$ both exist, **$L(f,P)\leq L(f) \leq U(f) \leq U(f,P)$ for any $P$**
* 
* For $a < b$ and $f:[a,b] \rightarrow \mathbb{R}$ bounded, say $f$ is *integrable* on $[a,b]$ if $L(f) = U(f)$ and write $\int^b_a f$ or $\int^b_a f(x) dx$ 

![](/lecture1summary.JPG)

## Examples
#### Constant Function: $f = c$
* For any partition $P$,
* $L(f,P) = c\sum_{i=1}^n(t_i-t_{i-1})=c[t_n-t_0]=c(b-a)$

#### Dirichlet Function: $f(x) = \bigg\{\begin{matrix}0, x \in \mathbb{Q}^\prime\\ 1, x \in \mathbb{Q}\end{matrix}$

* For any partition $P$,
* $m_i =0,M_i=1,\forall i$
* $L(f,P) = 0(b-a) \neq 1(b-a) = U(f,P)$

#### $f(x) = \bigg\{\begin{matrix}1, x \in \{1,\frac{1}{2},\frac{1}{3},\frac{1}{4},...\} \\ 0, otherwise\end{matrix}$

* For any partition $P$,
* $L(f,P) = 0, L(f)=0$
*
* **Claim:** $\forall\epsilon > 0, \exists$ Partition $P_\epsilon\,$ s.t.$\,U(f,P_\epsilon)<\epsilon$

## Criterion for Integrability
$f:[a,b]\rightarrow \mathbb{R}$ is integrable iff $\forall\epsilon > 0, \exists P_\epsilon\,$ s.t. $\,U(f,P\epsilon)-L(f,P\epsilon)<\epsilon$

## Definitions
* For any $a$
 $$\int_a^af=0$$
* and if $a>b$
 $$\int_a^bf=-\int_b^af$$
* And consequently if $a,b,c$ are any three numbers
$$\int_a^bf=\int_a^cf +\int_c^bf$$
* And also consequently $f[a,b]\rightarrow\mathbb{R},$ with points  $a=c_0 < c_1 < ... < c_n=b$ s.t. $f$ is always $\geq0$ or always $\leq0$ on $[t_{i-1},t_i]$,$\forall i$ then 
$$\sum_{i=1}^n\int_{t_{i-1}}^{t_i} f$$

* is the signed area bounded by $y=f(x)$, x-axis, $x=a$ and $x=b$

## Basic Properties of Integral
1. Fix $a < c < b$
	* If $\int_a^bf$ exists, then so does $\int_a^cf$ and $\int_c^bf$
	* and $$\int_a^bf=\int_a^cf +\int_c^bf$$
2. Converse of 1
	*  $$\int_a^cf +\int_c^bf=\int_a^bf$$
3. If $f,g$ are integrable on $[a,b]$, then so is $f+g$, 
	* and $$\int_a^b(f+g)=\int_a^bf+\int_a^bg$$
4. If $f$ is integrable on the $[a,b]$ and $c\in\mathbb{R}$, then so is $cf$ and
	$$\int_a^bcf=c\int_a^bf$$
	* **Consequence:** if $f,g$ defined $[a,b]$ differ at only finitely many places then if $f$ is integrable so is $g$ and 
		$$\int_a^bf=\int_a^bg$$
		
## Other Closure Properties
1. if $f$ is integrable on $[a,b]$ so is $|f|$
2. so is $\max\{f,0\}$ and $\min\{f,0\}$ 
3. Define $f^+=\max\{f,0\}$ and  $f^-=-\min\{f,0\}$
	* so $f=f^+-f^-$, which is a linear combination of non-negative functions
	* Have $f$ integrable on $[a,b]\iff$ both $f^+$ and $f^-$ are
4. if $f,g$ are integrable on $[a,b]$, then so is $fg$


## Integral Inequalities
1. **Triangle Inequality for Integrals**
	* If $f$ is integrable on $[a,b]$ then 
		$$\left|\int_a^bf\right|\leq\int_a^b|f|$$
2. **Cauchy-Schwarz-Bunyakovsky Inequality**
	 $$\left(\int_a^bfg\right)^2\leq\left(\int_a^bf^2\right)\left(\int_a^bg^2\right)$$
	 
	* **Discrete Version**
		* If $a_1,...,a_n$ and $b_1, ..., b_n$ are any sequences of real numbers
		* $$\left(\sum^n_{i=1}a_ib_i\right)^2\leq\left(\sum^n_{i=1}a_i^2\right)\left(\sum^n_{i=1}b_i^2\right)$$


## Uniform Continuity
### Recall: Continuity
$f:I\rightarrow\mathbb{R}$ is continuous on $I$ : $(\forall a \in I)(\forall \epsilon > 0)(\exists\delta > 0)(\forall x \in I)(|x-a| < \delta \implies \left|f(x)-f(a)\right|<\epsilon$

* for continuity, $\delta$ depends on $a$ and $\epsilon$
* Sometimes $\delta$ does not depend on $a$, just $\epsilon$

### Actual Uniform Continuity
$$(\forall \epsilon > 0)(\exists\delta > 0)(\forall c \in I)(\forall x \in I)(|x-c| < \delta \implies \left|f(x)-f(c)\right|<\epsilon)$$

* Uniform Continuity implies Continuity
* Only on an interval
* Definition is Symmetric:
	* $$(\forall \epsilon > 0)(\exists\delta > 0)(\forall x,y \in I)(|x-y| < \delta \implies \left|f(x)-f(y)\right|<\epsilon)$$


### Theorem
* If $f:[a,b]\rightarrow\mathbb{R}$ is continuous, then it is uniformly continuous
	* Corollary: Every continuous function on a closed interval is integrable


## The Fundamental Theorem of Calculus
* **Define**
	* $f$ is integrable on $I$
		* $f$ is integrable on any closed interval $[a,b]\subseteq I$
	* $$F(x)=\int^x_af=\int^x_af(t)\,dt$$

### Theorem 1
If $f:I\rightarrow\mathbb{R}$ is integrable, $a\in I, F(x)=\int^x_af(t)\,dt$, then $F$ is continuous on $I$

### Fundamental Theorem of Calculus Part 1 (Theorem 2)
If $f:I\rightarrow\mathbb{R}$ is integrable, define $F(x)=\int^x_af(t)\,dt$ then at every point $x$ where $f$ is continuous, $F$ is differentiable and 
$$F^\prime(x)=f(x)$$

### Fundamental Theorem of Calculus Part 2 (Corollary) (Theorem 3)
Suppose $f$ is continuous on $I$, and $\exists g:I\rightarrow\mathbb{R}$ which is differentiable with $g^\prime=f$

Also, $F(x)=\int_a^xf(x)\,dt$ has $F^\prime=f$

So $F(x)=g(x)+C$


$f:[a,b]\rightarrow\mathbb{R}$ is continuous, $g:[a,b]\rightarrow\mathbb{R}$, $g^\prime=f$, 
$$\int_a^bf=g(b)-g(a)$$

### Fundamental Theorem of Calculus Part 2 (Stronger) (Theorem 4)

if $f:[a,b]\rightarrow\mathbb{R}$ is integrable, and if $g:[a,b]\rightarrow\mathbb{R}$, with $g^\prime=f$, then
$$\int_a^bf=g(b)-g(a)$$

## Improper Integrals
$\int_a^\infty f$ means $\lim_{N\rightarrow\infty}\int_a^N f$, assuming this limit exists. [So: $f$ is integrable on $[a,N]$ for every $a\geq N$]

### Lemma 
$$\int_{-\infty}^\infty f\,dx = \int_{-\infty}^a f\,dx + \int_{a}^{\infty} f\,dx$$

#### Comparison Lemma
If $0\leq g(x)\leq f(x)$ on $[a,\infty]$, 
and if $\int_a^{\infty} f$ exists, 
and if $\int_a^N g$ exists for all $N\geq a$ 
then $\int_a^\infty g$ exists and $\int_a^{\infty} g \leq \int_a^{\infty}f$

### Another Improper Integral
$\int^a_b f$ where $f$ is unbounded on $[a,b]$. If $f$ is bounded on $[a+\varepsilon,b]$ for all $\varepsilon>0$. then 

$$\int_a^b f = \lim_{\varepsilon \rightarrow 0}\int_{a+\varepsilon}^b f$$ if this exists