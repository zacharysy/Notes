# Chapter 17: Series
## Informally
$$a_1+a_2+a_3+...$$
or
$$\sum_{n=1}^{\infty}a_n$$

## Main Definition
$(a_n)$ is summable if the sequence of partial sums $(S_n)=(\sum_{i=1}^n a_i)$ converges.

If limit of $(S_n)$ is $L$, say that $$\sum_{i=1}^{\infty}a_i$$ converges and $$\sum_{i=1}^{\infty}a_i=L$$

## Examples
1. If $a_n$ is eventually $0$, $(a_n)$ is summable
2. $(-1)^n$ is not summable because partial sums don't converge
3. $(\frac{1}{n})$ is not summable
4. $(r^n)_{n=1}^{\infty}, |r|<1$ (geometric series)
	* $$\sum_{i=1}^{\infty}=\frac{1}{1-r}$$  
	* (important)

## Criteria for Summability
### Basic Closure Properties
*  If $\sum_{i=1}^{\infty}a_i = \ell_a$ 
*  and $\sum_{i=1}^{\infty}b_i = \ell_b$
*  then $$\sum_{i=1}^{\infty}(ca_i+db_i) = c\ell_a+d\ell_b$$
*  Changing finitely many terms of $(a_n)$ does not change summability status

### Cauchy Criterion
* $(a_n)$ is summable iff $(S_n)$ is Cauchy
* $$\forall\varepsilon>0,\exists n_0 \text{ s.t. }m>n>n_0 \implies |a_n+a_{n-1}+\cdots+a_{m+1}|<\varepsilon$$   
* Basically finding a tail that converges

### Vanishing Condition 
* If $(a_n)$ is summable, $$\lim_{n\rightarrow\infty}|a_n| = 0$$ 
* so $$\lim_{n\rightarrow\infty}a_n = 0$$
* basically if $\lim_{n\rightarrow\infty}a_n \neq 0$ then $(a_n)$ is not summable
* Converse (if $(a_n)\rightarrow 0$, $(a_n)$ is summable) not true

### Boundedness Criterion
* Only of theoretical importance
* If $a_n\geq 0$, then $S_n$ is non-decreasing, so in this case $(a_n)$ is summable iff $(S_n)$ is bounded above.

### Comparison Test (Very important and practical)
* If $b_n\geq a_n \geq 0\,\forall n$ (or at least for all large $n$), if $(b_n)$ is summable, so is $(a_n)$
* 
* **Contrapositive**
	* if $(a_n)$ is not summable, then neither is $(b_n)$

### Limit Comparison Test (Even more important and practical)
* Suppose $a_n,b_n>0$, and $$\lim_{n\rightarrow\infty}\frac{a_n}{b_n}=c>0$$
* then either 
	* $(a_n),(b_n)$ both summable
	* or both not
	* 
* **Helpful Hint**
	* Compare to something v similar by removing stuff that just disappear eventually
		* like compare $\frac{2}{\sqrt[3]{n^2+1}}$ with $\frac{1}{n^{\frac{2}{3}}}$, since no one cares about the $2$ on top or that $+1$
 
### Ratio Test (probs the most useful test)
* Special case of limit comparison test, basically getting out a geometric series
* If $a_n>0$ for all sufficiently large $n$, and if $$\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}=r$$
* If
	* $r>1$
		* $(a_n)$ is not summable
	* $r<1$
		* $(a_n)$ is summable
	* $r=1$
		* who knows, no conclusion can be drawn

### Integral Test
* A series is just summing a bunch of bars with length $a_n$ and width $1$
	* So there should be a function where the series is a upper/lower partition
* Suppose that $f:[1,\infty]\rightarrow(0,\infty)$ is non-increasing with $f(n)=a_n\,\forall n$ then
	* $(a_n)$ is summable iff $\int_1^\infty$ exists

### Leibniz' Theorem on Alternating Series (helpful for non-negative sequences)
* If $(a_n)$ is non-negative, decreasing, and $a_n\rightarrow 0$ as $n\rightarrow\infty$, then $((-1)^{n-1}a_n)$ is summable
	* $(a_n)$ doesn't need to be convergent
* Also
	* If Leibniz series is truncated at the $n$ th term, 
		* if $n$ is even, partial sum falls short of limit by no more than $a_{n+1}$
		* if $n$ is odd, partial sum exceeds limit by no more than $a_{n+1}$

## Absolute Convergence
$\sum a_n$ is absolute convergent if $\sum |a_n|$ converges. Else, $\sum a_n$ is conditionally convergent

### Infinite Commutativity Theorem 1
If $\sum a_n$ is conditionally convergent, then for all $\alpha\in[-\infty,\infty]$ there exists a rearrangement of $\sum a_n$ whose sum is $\alpha$


### Infinite Commutativity Theorem 2
If $\sum a_n$ is absolutely convergent, then for any rearrangement $(b_n)$ of $(a_n)$, $$\sum b_n = \sum a_n$$ and $$\sum |b_n| = \sum |a_n|$$

### Theorem about Convergence and Absolute Convergence
If $\sum a_n$ is absolutely convergent, then it is convergent