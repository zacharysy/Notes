# L01: Introduction and Overview

## Two's Complement
* For a number $n$, the two's complement is a number $m$ such that for each digit $n_i$ (including carry over from $n_{i-1}$), the digit $m_i$ is given by $$n_i+m_i=2_{10}$$ 
## Additive Inverse
* let $A'$ be the complement
	* $A+A'$ is all $1$ s
* $F:A\rightarrow(A'+1)$ is additive inverse
* So two's complement is equivalent to one's complement then adding one

## Overflow
* Is not a dropped carry out
* When the sum of two numbers is opposite side

## Overflow Logic
### Mask
* To get the value of a single digit, using `and` on the number with a mask that is zero everywhere except on the digit