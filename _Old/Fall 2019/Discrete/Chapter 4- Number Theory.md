# Chapter 4: Number Theory

## Divisibility
* $a,b\in\mathbb{Z}$
* $a|b$ if there exists $m$ such that $b=am$

### Theorems
* If $a|b$ and $a|c$ then $a|(b+c)$
* if $a|b$ then $a|bc$ for all $c\in\mathbb{Z}$
* If $a|b$ and $b|c$ then $a|c$
* $a\in\mathbb{Z}$ and $m\in\mathbb{Z}^+$
	* there are unique $q\in\mathbb{Z}$ and $r\in\mathbb{N}$ such that
		* $a = mq+r$
		* so $(a-r)|q$
	* $q = a\text{ div }m$
	* $r = a\mod m$


## Congruence
* if $m|(a-b)$ then $a \equiv b\pmod m$ 
	* $a\mod m = b\mod m$
	* $a = qm + b$


## Prime Numbers
* it's not a composite number lol

## GCD
* It's the GCD

### Euclidean Algorithm
* Find GCD yay

### Inverse
* $\overline{a}\in\mathbb{Z}$ such that $$\overline{a}a\equiv 1\pmod m$$
* if $a$ and $m$ are coprime, then inverse must exist

## Solution to $ax\equiv b \pmod m$
* If $a$ and $b$ are coprime, then solution is unique
	* else there are GCD number of solutions