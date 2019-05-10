# Chapter 15: Approximating Functions (Taylor Polynomials and Taylor's Theorem)

If we know $f$,$f'$,$f''$ at point $a$, how do we approximate $f$ near $a$

## Possible Attempts
### Use $f(a)$
$$f(x)=f(a)$$
### Linearization
$$L_{a,f}(x)=f(a)+f'(a)(x-a)$$
### Linearization++
$$f(a)+f'(a)(x-a)+\frac{f''(a)}{2}(x-a)^2$$

## Taylor Polynomial of Degree $n$ of $f$ at $a$
* Define the degree $n$ Taylor Polynomial of $f$ at $a$ is the polynomial
	* $$P_{n,a,f}(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2}(x-a)^2+...+\frac{f^{(n)}(a)}{n!}(x-a)^n$$

$$P_{n,a,f}(x)=\sum_{k=0}^n\frac{f^{(k)}(a)}{k!}(x-a)^k$$

## Some Important Taylor Expansions
### Exponential
$$P_{n,0,\exp}(x)=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+...++\frac{x^n}{n!}$$

### Sine
$$P_{2n+1,0,\sin}(x)=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+...+(-1)^n\frac{x^{2n+1}}{(2n+1)!}$$

### Cosine
$$P_{2n,0,\cos}(x)=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+...+(-1)^n\frac{x^{2n}}{(2n)!}$$

### Logarithm
$$P_{n,1,\log}(x)=(x-1)-\frac{(x-1)^2}{2}+\frac{(x-1)^3}{3}-\frac{(x-1)^4}{4}+...+(-1)^{n-1}\frac{(x-1)^n}{n}$$

## Why is the Taylor Polynomial important
* As the $n$-th degree taylor polynomial approaches $f(a)$ as $x$ approaches $a$, then the difference between the function and the nth degree taylor expansion divided by $x-a$
	* Basically $n$-th derivatives are equal

## Agreement to an Order $n$ at $a$
* Functions $f,g$, defined at and near $a$, agree to order $n$ at $a$ if
	* $$\lim_{x\rightarrow a}\frac{f(x)-g(x)}{(x-a)^n}=0$$
* If $f,g$ agree to order $n$ at $a$, then they also agree to orders less than $n$ at $a$
* "agreeing" is an equivalence relation

## Theorem 1
* If $f$,$f'$,$f''$,...,$f^{(n)}$ exist at $a$ then
	* $P_{n,a,f}(x)$ agrees with $f$ to order $n$ at $a$

## Theorem 2 (corollary of Theorem 2.5)
* Suppose $f$ is $n$ times differentiable at $a$ (meaning taylor polynomial exist) and that $q$ is a polynomial of degree $n$ in $(x-a)$ that agree with $f$ to order $n$ at $a$ then
	* $q = P_{n,a,f}$
	* If function has taylor polynomial, then any polynomial of degree $n$ is that taylor polynomial

## Theorem 2.5
If $q,p$ are polynomials of degree $\leq n$ in $x-a$ that agree to order $n$ at $a$, then $p=q$

## Taylor's Theorem with Integral Remainder Form
Suppose that $f$ is defined on an interval that includes $a$,$x$ and $f^{(n+1)}$ is integrable on that interval, then

$$R_{n,a,f}(x)=\int_a^x\frac{(x-t)^n}{n!}f^{(n+1)}(t)~dt$$

Where $R_{n,a,f}(x)$ is the remainder ($f-P$), or the error term.

## Taylor's Theorem with Lagrange Remainder Term (weak version)
Suppose $f$ is defined on interval $I$ that goes from $a$ to $x$. If $f^{(n+1)}$ is continuous on $I$, then 

$$R_{n,a,f}(x)=\frac{(x-a)^{n+1}}{(n+1)!}f^{(n+1)}(c)$$

For some $c$ between $a$ and $x$

## Taylor's Theorem with Lagrange Remainder Term (strong form)
Suppose $f$ is defined on interval $I$ that goes from $a$ to $x$. If $f^{(n+1)}$ exists, then 

$$R_{n,a,f}(x)=\frac{(x-a)^{n+1}}{(n+1)!}f^{(n+1)}(c)$$

For some $c$ between $a$ and $x$

## Important Lemma 
For $x>0$ fixed, $$\lim_{n\rightarrow\infty}\frac{x^n}{n!}$$

And so remainder goes to $0$ as $n\rightarrow\infty$

## Summary
* For every $f,a$, we have $P_{n,a,f}\rightarrow f(x)$ for some $x$'s nearby to $a$
	* $\exp,\sin,\cos,a=0$ works for all real $x$
	* $\tanh^{-1},a=0$, for all $x\in(-1,1)$, which is domain of $\tanh^{-1}$
	* $\tan^{-1},a=0$, for all $x\in[-1,1]$, which is not the domain of $\tan^{-1}$
	* $f(x)=e^{-\frac{1}{x^2}}$, only works at $a=0$

## Taylor Series
* Taylor Polynomial pushed to infinity
* $$\sum_{n=0}^{\infty}\frac{f^{(n)}(a)}{n!}(x-a)^n$$
