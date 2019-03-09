# Antiderivative
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

### Definite Integral Form

## Integration by Partial Fraction