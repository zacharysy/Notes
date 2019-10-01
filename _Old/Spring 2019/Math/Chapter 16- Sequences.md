# Chapter 16: Sequences
## Formally
An infinite sequence is a function 
	$$a:\mathbb{N}\rightarrow\mathbb{R}$$

## Informally
A list/array of numbers 
$$(a_1,a_2,a_3,a_4,...)$$

## Notation for Sequences
### Using Formal Notation
$$a:\mathbb{N}\rightarrow\mathbb{R},\, a(k)=2+(-1)^k$$
### Give a function to generate
$$a_n = n^2+1,\,n=0,1,2,3,4...$$
### Just listing them out
$$(2,3,5,7,11,13)$$
### Summation Notation
$$a_n=\sum_{k=1}^n\frac{x^k}{k!}$$
### Recursion
$a_1=1$
	$$a_{n+1}=\frac{3a_n+4}{2a_n+3}$$ 
for  $n\geq 1$
### Another Notation
$$(a_n)_{n=1}^{\infty}$$
$$(a_n)$$

## Kinds of Behavior a Sequence Can Exhibit
### Convergence
Say $(a_n)$ converges to a limit $L$ if
	$$\forall \varepsilon>0,\exists\,n_0$$
such that
	$$n>n_0 \implies |a_n-L|<\varepsilon$$
so basically
	$$\lim_{n\rightarrow\infty}a_n=L$$
	(find $n$ in terms of epsilon and let $a_0$ equal that thing)
	
### Divergence
If ($a_n$) does not converge, then it diverges

#### Goes to Infinity 
Say that $a_n$ goes to infinity if 
	$$\forall N,\,\exists\,n_0$$
such that 
	$$n>n_0 \implies a_n>N$$
	
#### Goes to Negative
Say that $a_n$ goes to negative infinity if 
	$$\forall N,\,\exists\,n_0$$
such that
	$$n>n_0 \implies a_n< N$$
	
#### Oscillations
trivial

## Facts about sequences
* Changing finitely many items in a sequence results then behavior is the same
* Shifting the sequence by a number of terms have the same behavior
* If a sequence converges to a limit, then that limit is unique
* Limit laws still hold
* and other stuff in the course notes

## Limits of Sequences vs Limits of Functions
* If $f:[1,\infty)\rightarrow\mathbb{R}$ and $\lim_{x\rightarrow\infty}=L$, and $a_n=f(n)$, then
	* $(a_n)\rightarrow L$
	* Direct converse not true
	* 
* If $(a_n)\rightarrow L$, and $f:[1,\infty)\rightarrow\mathbb{R}$ has $f(b)=a_n$, and $\lim_{x\rightarrow\infty} f(x)$ exists, then
	* $f(x)\rightarrow L$


### Very Important Theorem
* Suppose $f$ is continuous at $c$ and that $(a_n)\rightarrow c$, then
	* $$(f(a_n))\rightarrow f(c)$$
	* Converse: If $f$ is defined at and near $c$, and $lim_{n\rightarrow\infty} f(a_n)=f(c)$ for all sequences $(a_n)$ that converges to $c$, then $f$ is continuous at $c$


### Squeeze Theorem for Sequences
* If $(a_n)$,$(b_n)$ and $(c_n)$ are sequences, 
* and $a_n \leq b_n \leq c_n$ eventually, 
* and $(a_n),(c_n)\rightarrow L$ 
* then $$(b_n)\rightarrow L$$

### Stuff about monotony and boundedness of sequences
* If ($a_n$) is weakly increasing and bounded above by $\alpha=\sup\{a_n:n\in\mathbb{N}\}$, then $(a_n)\rightarrow\alpha$

## Subsequence
### Informally
* If $(a_n) = (a_1,a_2,a_3,...)$ then a subsequence is a sequence of the form 
	* $$(a_{n_1},a_{n_2},a_{n_3},...)$$
* where $n_1< n_2< n_3 < \cdots$ a restriction of the sequence

### Fundamental Lemma
Every sequence has a monotone (weakly) subsequence

#### Finite Version of This Lemma
In any finite sequence of length $n^2+1$ there is always either an increasing subsequence of length $n+1$ or a decreasing subsequence of length $n+1$

#### Bolzano-Weierstrauss Theorem
Every bounded sequence has a convergent subsequence

## Cauchy Sequences
Say that $(a_n)$ is Cauchy if 
	$$(\forall \varepsilon > 0)(\exists n_0)(\forall n,m)( |a_n-a_m<\epsilon|)$$
Basically the terms of the sequence gets arbitrarily close to each other. Lets us determine whether a sequence is convergent without knowing the limit 

### Theorem
Every Cauchy sequence converges to a limit


