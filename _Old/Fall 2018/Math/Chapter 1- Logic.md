# Chapter 1: Logic

## Statement
* An assertion that has a definite truth value
* Statements are Boolean
* 
* Examples of not statements
	* Questions
	* Imperatives
	* Predicates
	* Paradoxes
* Mathematics is looking at statements and determining their truth/false

## Ways of Combining/Modifying statements
### Negation (!) ($\lnot p$) 
* "not p"

### Conjunction (&&) ("and")
* $p\land q$

### Disjunction (||) ("or")
* $p \lor q$

## Implication ($p \implies q$)
* Equivalent to $\lnot p \lor q$
* P = hypothesis, q = conclusion
* 
* If p, then q
* P is sufficient for q
* Q whenever p 

* | P	| Q	| $P \implies Q$ |
|:--|:--|:-------------|
| 0	| 0 |	1 |
| 0	| 1	| 1 |
| 1	| 0	| 0 |
| 1	 | 1	| 1 |

* If the premise is false, there is no way to say that the implication would not happen and therefore results to true
			
### Contrapositive Implication
* Equivalent to implication
* $\lnot q \implies \lnot p$

* | P	| Q	| $\lnot q \implies \lnot p$ |
|:--|:--|:-------------|
| 0	| 0 |	1 |
| 0	| 1	| 1 |
| 1	| 0	| 0 |
| 1	 | 1	| 1 |
				
### Converse Implication
* $q \implies p$
* Not equal to $p \implies q$

* | P	| Q	| $q \implies p$ |
|:--|:--|:-------------|
| 0	| 0 |	1 |
| 0	| 1	| 0 |
| 1	| 0	| 1 |
| 1	 | 1	| 1 |
				
### English language forms of implication
* p only if q
	* Same as implication via contrapositive implication
* q is necessary for p
	* Same as implication via contrapositive implication
				
### Bidirectional Implication 
* $p \iff q$
* Equivalent to $(p \implies q) \land (q \implies p)$
* P if and only if q
* P is necessary and sufficient for q

* | P	| Q	| $p \iff q$ |
|:--|:--|:-------------|
| 0	| 0 |	1 |
| 0	| 1	| 0 |
| 1	| 0	| 0 |
| 1	 | 1	| 1 |
			
## De Morgan's Laws
* $\lnot (p \land q)=\lnot p\lor  \lnot q$
	* $\lnot (p_1  \land p_2\land p_3 \cdots \land p_n )  = \lnot p_1  \lor  \lnot p_2  \lor \cdots \lor  \lnot p_n$
	* $\lnot (p\lor  q)=\lnot p\land  \lnot q$
		* $\lnot (p_1  \lor p_2 \lor p_3 \cdots \lor  p_n )  = \lnot p_1\land  \lnot p_2\land  \cdots \land  \lnot p_n$

## Predicates 
* Assertions involving variables, whose truth value depends on the value of the variable
	
### Quantification
#### Universal Quantifier
* Take a predicate and assert that the predicate is true for all possible variables in the universe of discourse
* $\forall  xP(x)$

### Existential Quantifier
* True for at least one value in the universe of discourse 
* $\exists xP(x)$
				
### Negation of Quantified Statements
* If universe of discourse is finite $(x_1,x_2,x_3\cdots ,x_n)$
	* $\forall  xP(x)=P(x_1 )\land P(x_2 )\land P(x_3 )\land \cdots \land P(x_n )$
	* $\exists xP(x)=P(x_1 )  \lor  P(x_2 )  \lor  P(x_3 )  \lor \cdots \lor  P(x_n )$
* Therefore
	* $\lnot \forall  xP(x)=\lnot P(x_1 )  \lor \lnot P(x_2 )  \lor  \lnot P(x_3 )  \lor \cdots \lor  \lnot P(x_n )  =\exists \lnot P(x)$
	* $\lnot \exists xP(x)=\lnot P(x_1 )\land \lnot P(x_2 )\land \lnot P(x_3 )\land \cdots \land \lnot P(x_n )=\forall  \lnot P(x)$
		
* Example
	* A set $S$ is dense in the real numbers
	* $(\forall  x\in R)(\forall  \varepsilon>0)(\exists s\in S)(x−\varepsilon<s<x+\varepsilon)$
		* Negation
			* $(\exists x\in R)(\exists \varepsilon>0)(\forall  s\in S)((s\geq x+\varepsilon)\lor(s\leq x− \varepsilon))$

* Warning
	* Order of quantifiers matters

## Tautology
* A statement built up from smaller statements such that whatever truth value the smaller statements have, the compound statement is true
	* Always true
	* 
	* Example
		* $p \lor \lnot p$
		* $(p\land (p\implies q))\implies q$
			* Modus ponens 
				
