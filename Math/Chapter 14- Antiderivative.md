# Chapter 14: Antiderivative
## Definition
$F$ is an **antiderivative** (or a primitive) of $f$ if $F'=f$

## Notation
If $F$ is a primitive of $f$, then 
	$$F = \int f$$
	or
	$$F(x) = \int f(x)~dx$$
Where $\int$ is indefinite integral

## Main Use
If $F=\int f$ then by FTOC,
	$$\int_a^bf = F(b)-F(a)=F(x)|_a^b$$
As long as $f$ is defined on $[a,b]$.

## Theorem
Every continuous function has a primitive:
	$$\int_c^x f(t)~dt$$

# Techniques
## Know a bunch of integrals
Obvious

## Linearity
Literally get integral of linear combinations

## Integration by Parts
* Derived from product rule
* As long as $f'$ and $g'$ are continuous
$$\int f~g' = fg - \int f'~g$$
$$\int u~dv = uv - \int v~du$$

Reduces more complicated problem to slightly less complicated problem

$$\int f = xf - \int xf'$$

Useful for reduction formulae

### Reduction Formula
Find recurrence relation with integrals

### Definite Integral Form
$$\int_a^b f~g' = fg|_a^b - \int_a^b f'~g$$

## Integration by Substitution
* Inverting the Chain Rule
* 
* $f,g'$ both continuous
* Suppose $F$ is primitive of $f$
* Then $$(F\circ g)'= F'(g)\cdot g'=f(g)\cdot g'$$
* So $$\int f(g(x))g'(x)~dx=F(g(x))$$

### More General Substitution Method (kinda useless but good to know)
* $f,g'$ are both continuous, and $g'$ never zero, and $g$ is invertible
* $$\int h(x)f(g(x))~dx = \int \frac{h(x)}{g'(x)}f(g(x))g'(x)~dx$$
* Suppose $H$ is a function with $$H'(u)=\frac{h(g^{-1}(u))f(u)}{g'(g^{-1}(u))}$$
* So $$(H\circ g)'=H'(g(x))g'(x)=h(x)f(g(x))$$
* Therefore
* $$\int h(x)f(g(x))~dx = H(g(x))$$

### Shorthand
* let $u=g(x)$, and $g=^{-1}(u)$
* $du = g'(x)~dx$
* $f(g(x))=f(u)$
* $h(x) = h(g^{-1}(u))$
* So $$\int h(x)f(g(x))~dx=\int H(g(x))$$

### Important Formulas
* $$\cos^2x=\frac{1+\cos2x}{2}$$
* $$\cos^2x=\frac{1-\cos2x}{2}$$

### Trigonometric Substitutions
1. $$\sqrt{a^2+(bx)^2}$$
	* $$x=\frac{a}{b}\sin{u}$$
2. $$\sqrt{a^2+(bx)^2}$$ 
	* $$x=\frac{a}{b}\tan{u}$$
3. $$\sqrt{(bx)^2-a^2}$$ 
	* $$x=\frac{a}{b}\sec{u}$$

### Trig Functions with Powers
* $$\int\cos^px\sin^qx~dx$$
* where $p,q\in\mathbb{Z}$
	* If $q$ is odd
		* let $u = \cos x$
	* If $p$ is odd
		* let $u = \sin x$
	* If $p$ and $q$ are both even and nonnegative
		* use $\cos^2x$ and $\sin^2x$
	* Default
		* Magic Bullet substitution

### Last-Resort (Magic Bullet) Substitution
Eliminates all trig functions

let $$t=\tan\frac{x}{2}$$
and so $$\sec^2\frac{x}{2}=1+t^2$$
and so $$dx = \frac{2}{1+t^2}~dt$$

$$\sin x = \frac{2t}{1+t^2}$$

Substitution is only valid for $\mathbb{R}\setminus\{\pm\pi,\pm3\pi,\pm5\pi,...\}$

## Integration by Partial Fraction
### Step 1
Reduce $\frac{P(x)}{Q(x)}$ such that $\deg(P)<\deg(Q)$

### Step 2
Fully factorize $Q$ into linear and quadratic factors

### Step 3: Do Partial Fractions Decomposition

$$\frac{P(x)}{Q(x)}=\frac{P(x)}{(x-a_1)^{m_1}(x-a_2)^{m_2}...((x-b_1)^2+c_1^2)^{n_1}}$$

Which is equal to

$$\frac{A_1}{x-a_1}+\frac{A_2}{(x-a_1)^2}+...+\frac{A_3}{(x-a_1)^{m_1}}+...+\frac{B_1x+C_1}{(x-b_1)^2+c_1^2}+\frac{B_2x+C_2}{(x-b_1)^2+c_1^2}$$

### Step 4
cry (Integrate)
