# Chapter 13: The Logarithm and Exponential Function

## Theoretical Exponential Function

If $\text{exp}_a$ is a function that represents raising base $a$ to a power, then these are the properties $\text{exp}_a$ should satisfy:

* Domain of $\text{exp}_a$ is $\mathbb{R}$
* $\text{exp}_a(0)=1$, $\text{exp}_a(1)=a$
* $\text{exp}_a(x+y)=\text{exp}_a(x)\text{exp}_a(y)$
* $\text{exp}_a$ is continuous, differentiable, and invertible
 
 ## Inverse of Exponential ($\log(x)$)
 $$(\text{exp}_a^{-1})'(x)=\frac{1}{\text{exp}_a'(\text{exp}^{-1}_a(x))\text{exp}_a'(0)}$$
 
 $$(\text{exp}_a^{-1})'(x)=\frac{1}{x\,\text{exp}_a'(0)}$$
 
 $$\log(x)=\int_1^x\frac{1}{t}\,dt$$
 
 * **Domain:** $(0,\infty)$
	 * $0$ is not in domain of $\log$
 * **Range:** $(-\infty,\infty)$


## Exponential Function ($\exp(x)$)
Inverse of $\log(x)$

## Base of Natural Logarithms ($e$)
### Definition
That number s.t. 
	$$\int_1^e\frac{1}{t}\,dt=1$$
And so
	$$\log(e)=1$$
and
	$$\exp(1)=e$$
	
### Other Characteristics of $e$
$$e=\lim_{n\rightarrow\infty}\left(1+\frac{1}{n}\right)^n$$
$$e=\lim_{n\rightarrow\infty}\sum_{i=1}^n\frac{1}{i!}$$
$$e=\lim_{n\rightarrow\infty}\frac{n^n}{[n!]^{\frac{1}{n}}}$$


## Properties of Logarithm and Exponents
* $$\log ab = \log a + \log b$$
	* $$\int_1^{ab}\frac{1}{t}~dt=\int_1^{a}\frac{1}{t}~dt+\int_1^{b}\frac{1}{t}~dt$$
* $$\log \frac{a}{b}=\log a - \log b$$
* $$\exp(a+b)=\exp(a)\exp(b)$$
* $$\exp(a-b)=\frac{\exp(a)}{\exp(b)}$$

## Definition
$e^x$ means $\exp(x)$

$\exp(x)$ is continuous extension to reals of natural definition of $e^x$

* $$\log a^x = x\log a$$
	* $$a^x = e^{x\log a}$$

## Properties of $a^x$
* $$a^0 = e^0 = 1$$
* $$a^1 = e^{\log a} = a$$
* $$a^{b+c}=e^{bc \log a} = a^ba^c$$
* $$(a^b)^c = e^{c \log a^b} = a^{bc}$$
* if $f(x)=a^x$ then
	* $$f'(x)=a^x \log a$$
* $f$ is invertible, with inverse
	* $$\log_a$$
	* $$\log_a x = \frac{\log x}{\log a}$$

## Theorem
If $f:\mathbb{R}\rightarrow\mathbb{R}$ and $f$ is differentiable, and $f'=f$, then $f(x)=ce^x$ for some $c>0$, $c=f(0)$


## Very Important Limit
$$\forall n\in\mathbb{N}, \lim_{x\rightarrow\infty}\frac{e^x}{x^n}=\infty$$
$$\text{for } a > 1\text{ and }b<\infty, \lim_{x\rightarrow\infty}\frac{a^x}{x^b}=\infty$$

## Trigonometric Functions
### Definition
$$\pi=2\int_{-1}^1\sqrt{1-x^2}~dx$$
$$A(x)=\int_x^1\sqrt{1-t^2}~dt + \frac{x\sqrt{1-x^2}}{2}$$
$$\cos\theta = A^{-1}\left(\frac{\theta}{2}\right)$$
$$\sin\theta = \sqrt{1-\cos^2\theta}$$