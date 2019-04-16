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

## Nice Theorem for Comparing
* If $f,g:[a,\infty)$ are both differentiable 
	* with $f(a)=g(a)$
	* and $f'(x)\geq g'(x)\forall x$
* then
	* $$f(x)\geq g(x) \forall x$$
* and so 
	* if $g(x) \rightarrow\infty$ as $x\rightarrow\infty$
	* then $f(x) \rightarrow\infty$ as $x\rightarrow\infty$

## Trigonometric Functions
### Definition
$$\pi=2\int_{-1}^1\sqrt{1-x^2}~dx$$
$$A(x)=\int_x^1\sqrt{1-t^2}~dt + \frac{x\sqrt{1-x^2}}{2}$$
$$\cos\theta = A^{-1}\left(\frac{\theta}{2}\right)$$
$$\sin\theta = \sqrt{1-\cos^2\theta}$$

### Derivatives
$$\cos'(\theta) = -\sin(\theta)$$
$$\sin'(\theta) = \cos(\theta)$$

### Easy Facts About Cosine and Sine
* $$\cos : \mathbb{R} \rightarrow [-1,1]$$
* $$\cos \text{ is continuous and differentiable on }\mathbb{R}, \text{ except perhaps at } \theta = k\pi ,k\in\mathbb{Z}$$
* $$\sin : \mathbb{R} \rightarrow [-1,1]$$
* $$\sin \text{ is continuous and differentiable on }\mathbb{R}, \text{ except perhaps at } \theta = k\pi ,k\in\mathbb{Z}$$
* $$\sin^2\theta + \cos^2\theta = 1$$
* Sine and cosine are both continuous

### Extending sin & cos to Real Line
$$\cos\theta = \cos(\theta+2k\pi)$$
$$\cos\theta = \cos(\theta+k\pi)$$
$$\sin\theta = \sin(\theta+2k\pi)$$
$$\sin\theta = -\sin(\theta+k\pi)$$

### Important Lemma
* If $f$ is continuous at $a$
	* and $f'$ exists near $a$
	* and $\lim_{x\rightarrow{a}}f'(x)=L$
* then $f$ is differentiable at $a$

### Important Characteristic
$\sin$ and $\cos$ or a linear combination of the two are the only solutions to the differential equation
	$$f''+f=0$$
Therefore 
	$$f(x) = a\cos{x}+b\sin{x}$$
	Where $f(0)=a$ and $f'(0)=b$

### Angle Addition Formulae
$$\sin(x+y) = \sin{x}\cos{y}+\sin{y}\cos{x}$$
$$\cos(x+y) = \cos{x}\cos{y}-\sin{x}\sin{y}$$

## Other Trigonometric Functions
### Tangent Function 
* $$\tan x = \frac{\sin x}{\cos x}$$
* **Domain:** $\mathbb{R}\setminus\left\{\left(n+\frac{1}{2}\right)\pi\right\}$
* **Range:** $\mathbb{R}$
* Periodic with **Period** $\pi$
* $$\tan'x=\frac{1}{\cos^2x}=\sec^2x$$
* $$tan(0)=0$$
* $$tan\left(\frac{\pi}{4}\right)=1$$
* $$tan^2x + 1 = \frac{1}{\cos^2x}=\sec^2x$$

### Inverse of Tangent ($\tan^{-1},\arctan$)
* Invertible on domain of $(-\frac{\pi}{2},\frac{\pi}{2})$
* Increasing in entire domain
* bounded by $-\frac{\pi}{2}$ and $\frac{\pi}{2}$
* $$(\tan^{-1})'x=\frac{1}{1+x^2}$$
* $$\tan^{-1}x=\int_0^x\frac{1}{1+t^2}~dt$$

### Inverse of Cos
* Invertible on domain $[0,\pi]$
* $$\cos^{-1}:[-1,1]\rightarrow[0,\pi]$$
* $$\cos^{-1'}=\frac{-1}{\sqrt{1-x^2}}$$
* $$\sin^{-1'}=\frac{1}{\sqrt{1-x^2}}$$

### Secant and Cosecant and Cotangent
$$\sec = \frac{1}{\cos}$$
$$\csc = \frac{1}{\sin}$$
$$\cot = \frac{\cos}{\sin}$$

## Hyperbolic Functions
$$x^2-y^2=1$$

Instead of area bounded by line and circle, is area bounded by line and hyperbola

$$\cosh{t}=\frac{e^t+e^{-t}}{2}$$
$$\sinh{t}=\frac{e^t-e^{-t}}{2}$$

### Properties
$$\cosh'=\sinh$$
$$\sinh'=\cosh$$
$$\cosh^2-\sinh^2=1$$

### Inverses
$$\cosh^{-1'}(x)=\frac{1}{\sqrt{x^2-1}}$$

