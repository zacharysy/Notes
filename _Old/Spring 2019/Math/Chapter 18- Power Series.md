# Chapter 18: Power Series

## Maclaurin Series (Taylor Series of $f$ at $a$)
If $f(x)$ has $R_{n,0,f}(x)\rightarrow 0$ as $n\rightarrow\infty$ for all $x\in$ some set $A$, then $$f(x)=\sum_{n=0}^{\infty}\frac{f^{(n)}(0)}{n!}x^n$$
Which is the Taylor series of $f$ at $0$  

## Taylor Series
if $R_{n,a,f}(x)\rightarrow 0$ as $n\rightarrow\infty$ for all $x\in$ some set $A$, then $$f(x)=\sum_{n=0}^{\infty}\frac{f^{(n)}(a)}{n!}(x-a)^n$$
Which is the Taylor series of $f$ at $a$.

## Examples
* $$e^x=\sum\frac{x^n}{n!}$$
* $$\sin x=\sum(-1)^n\frac{x^{2n+1}}{(2n+1)!}$$
* $$\cos x=\sum(-1)^n\frac{x^{2n}}{(2n)!}$$
* $$\tan^{-1} x=\sum(-1)^n\frac{x^{2n+1}}{2n+1}\,\{x\in[-1,1]\}$$ 

## Shorthand Notation
$$P_{2n,0,\cos}(x)=\cos_n(x)$$
$$P_{2n,0,\sin}(x)=\sin_n(x)$$

## Pointwise Convergence
* $f_n\rightarrow f$ on $A$ pointwise if $\forall x \in A$, $$\lim_{n\rightarrow\infty}f_n(x)=f(x)$$
* Not a great notion of convergence
* $\forall\varepsilon > 0$, $\forall x\in A$, $\exists N$, such that $$n>N\implies |f_n(x)-f(x)|<\varepsilon$$

## Uniform Convergence
$f_n\rightarrow f$ on $A$ uniformly if $\forall\varepsilon > 0$, $\exists N$ such that for all $x\in A$, $$n>N\implies |f_n(x)-f(x)|<\varepsilon$$

## Basic Properties of Uniform Convergence

### Theorem 1
If $f_n\rightarrow f$ uniformly on $[a,b]$, and each $f_n$ is continuous on $[a,b]$ then $f$ is continuous on $[a,b]$ (because uniformly continuous)

### Theorem 2
If $f_n\rightarrow f$ uniformly on $[a,b]$, each $f_n$ is integrable, then $f$ is integrable and $$\int_a^b f = \lim_{n\rightarrow\infty}\int_a^b f_n$$

### Theorem 3
* If $f_n\rightarrow f$ pointwise on $[a,b]$, each $f_n$ is differentiable, $f'_n$ is integrable and $(f_n')\rightarrow g$ uniformly on $[a,b]$ to some continuous limit $g$ 
	* Sequence of derivative converges to something that is continuous
* then $f$ is differentiable on $[a,b]$ and $$f'(x)=\lim_{n\rightarrow\infty}f_n'(x)$$

## Application to Power Series
### Power Series (at or about $0$)
Any expression of the form $$f(x)= a_0+a_1x+a_2x^2+a_3x^3+\cdots$$

* converges if $(a_nx^n)$ is summable or equivalently if $(S_n)$ is summable where $S_n$ is a partial sum.
* Converges Absolutely if $(|a_n||x^n|)$ is summable

### Hypothesis
Suppose that there exists $x_0\geq0$ such that
$$\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|}x_0$$ exists and equals some $\ell < 1$

#### Convergence
$\forall x\in[-x_0,x_0]$, $f(x)$ is a finite number

#### Uniform Convergence and Continuity
$(S_n(x))\rightarrow f(x)$ uniformly on $[x_0,x_0]$ so in particular, since $S_n$ is continuous, then $f$ is continuous

Also, $(S_n(x))$ converges absolutely uniformly to a limit

#### Differentiability
$f$ is differentiable on $[-x_0,x_0]$, and $$f'(x)=a_1+2a_2x+3a_3x^2+\cdots+(n+1)a_{n+1}x^n+\cdots$$ and the power series for $f'$ converges absolutely on $[-x_0,x_0]$

#### Integration
$f$ is integrable on $[a,b]$ and if $g(x)=\int_0^x f(t)~dt$ then $$g(x)=a_0x+\frac{a_1x^2}{2}+\frac{a_2x^3}{3}+\cdots$$

### Radius of Convergence ($R$)
The supremum of all $x_0$ for which $\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|}x_0$ exists and is less than $1$

* If $$\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|}=0$$
	* $R$ is $+\infty$
* If $$\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|}=\frac{1}{R}>0$$
	* Radius of convergence is $R$
* If $$\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|}=+\infty$$
	* $R=0$
* If $$\lim_{n\rightarrow\infty}\frac{|a_{n+1}|}{|a_n|} \text{ dne }$$
	* Things can be said

### Power Series inside its Radius of Convergence 
$$a_n = \frac{f^{(n)}}{n!}$$

* Therefore the Power Series of $f$ inside $R$ is equal to the Taylor Series of $f$
	* And so the Taylor Series of $f$ is the unique Power Series that converges to $f$ inside $R$

## Applications of Power Series
### Transcendental Numbers
$$e^x = \sum_{n=0}^{\infty}\frac{x^n}{n!}$$

### Estimating Integrals
$$e^{-x^2} = 1-x^2+\frac{x^4}{2!}-\frac{x^6}{3!}+\frac{x^8}{4!}\cdots$$

Taking integral

$$\int_0^xe^{-t^2}~dt =  = x-\frac{x^3}{3}+\frac{x^5}{5(2!)}-\frac{x^7}{7(3!)}+\frac{x^9}{9(4!)}\cdots+(-1)^n\frac{x^{2n+1}}{(2n+1)n!}+\cdots$$

Then using Leibniz' Test

$$\int_0^xe^{-t^2}~dt = \left(\sum_{k=1}^n(-1)^k\frac{x^{2k+1}}{(2k+1)k!}\right)\pm\frac{1}{(2n+3)(n+1)!}$$


### Closed Form of Recursive Sequences
Let the coefficients of the power series be the terms of the recursive function

#### Aside
If $(\frac{|a_{n+1}|}{|a_n})$ is eventually bounded above by $M>0$, then everything is valid for $Mx_0<1$