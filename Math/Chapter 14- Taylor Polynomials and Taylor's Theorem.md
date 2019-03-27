# Chapter 14: Approximating Functions (Taylor Polynomials and Taylor's Theorem)

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
	* $$\lim_{x-a}\frac{f(x)-g(x)}{(x-a)^n}=0$$
* If $f,g$ agree to order $n$ at $a$, then they also agree to orders less than $n$ at $a$
* "agreeing" is an equivalence relation

## Theorem 1
* If $f$,$f'$,$f''$,...,$f^{(n)}$ exist at $a$m then
	* $P_{n,a,f}(x)$ agrees with $f$ to order $n$ at $a$

## Theorem 2 (corollary of Theorem 2.5)
* Suppose $f$ is $n$ times differentiable at $a$ (meaning taylor polynomial exist) and that $q$ is a polynomial of degree $n$ in $(x-a)$ that a green with $f$ to order $n$ at $a$ then
	* $q = P_{n,a,f}$
	* If function has taylor polynomial, then any polynomial of degree $n$ is that taylor polynomial

## Theorem 2.5
If $q,p$ are polynomials of degree $\leq n$ in $x-a$ that agree to order $n$ at $a$, then $p=q$

## Techniques to finding Taylor Polynomial

