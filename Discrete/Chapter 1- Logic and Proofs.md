# Chapter 1: Logic and Proofs
## Propositional Logic
### Proposition
* declarative statement
* Has truth value

### Compound Proposition
* More than one proposition

### Logical Operators
#### Negation ($\lnot p$)
|$p$|$\lnot p$|
|:--|:-------|
| T | F         |

#### Conjunction ($\land$)
|$p$|$q$|$p\land q$ |
|:--|:--|:---------|
| F | F  | F |
| F | T  | F |
| T | F  | F | 
| T | T  | T |

#### Disjunction ($\lor$)
|$p$|$q$|$p\lor q$ |
|:--|:--|:---------|
| F | F  | F |
| F | T  | T |
| T | F  | T | 
| T | T  | T |

#### Exclusive Or ($\oplus$)
|$p$|$q$|$p\oplus q$ |
|:--|:--|:---------|
| F | F  | F |
| F | T  | T |
| T | F  | T | 
| T | T  | F |

* Equivalent to $(p\land\lnot q) \land (q\land\lnot p)$

### Implication/Conditional ($\rightarrow$)
|$p$|$q$|$p\rightarrow q$ |
|:--|:--|:---------|
| F | F  | T |
| F | T  | T |
| T | F  | F | 
| T | T  | T |

#### Contrapositive ($\lnot q \rightarrow \lnot p$)
|$p$|$q$|$\lnot q \rightarrow \lnot p$ |
|:--|:--|:---------|
| F | F  | T |
| F | T  | T |
| T | F  | F | 
| T | T  | T |

* Equivalent to implication

#### Converse ($q \rightarrow p$)
|$p$|$q$|$q\rightarrow p$ |
|:--|:--|:---------|
| F | F  | T |
| F | T  | F |
| T | F  | T | 
| T | T  | T |

#### Inverse ($\lnot p \rightarrow \lnot q$)
|$p$|$q$|$\lnot p \rightarrow \lnot q$ |
|:--|:--|:---------|
| F | F  | T |
| F | T  | F |
| T | F  | T | 
| T | T  | T |

* Equivalent to converse

#### Biconditional
|$p$|$q$|$p\iff q$ |
|:--|:--|:---------|
| F | F  | T |
| F | T  | F |
| T | F  | F | 
| T | T  | T |

## Order of operations
$$\lnot,\land,\lor,\rightarrow,\iff$$

## Tautology
* Always true
* $s$ is equivalent to $t$ when $s\iff t$ is a tautology
## Contradiction
* Always false
## Contingency
* Sometimes true or false

# Predicate Logic
## Quantifiers
### Universal Quantifier
$$\forall$$

* It's distributive with "and" but not with "or"
* Negation is exists 
### Existential Quantifier
$$\exists$$

## Rules of Inference 
* Turn argument into an argument form and show it's a tautology
	* Separate the premises by ands and say it implies conclusion
	* Then it's valid

### Argument Form
$$\begin{matrix}p  \\ p\implies q \\ \hline \therefore q\end{matrix}$$

### Examples Rules of Inference
#### Modus Ponens
* $$(p\land(p\implies q) \implies q)$$
#### Modus Tollens
* $$(\lnot q \land(p\implies q) \implies \lnot p)$$
#### Simplification
* $$(x\land y)\implies x$$

### Fallacies
#### Affirming Conclusion
* $$(q\land(p\implies q) \implies p)$$
#### Denying Hypothesis
* $$(\lnot p\land(p\implies q) \implies \lnot q)$$

### With Quantifiers
#### Universal Instantiation
* If $\forall x P(x)$ 
* if specific $c\in x$ then $P(c)$

#### Universal Generalization
* If $P(c)$ for arbitrary $c\in x$, then $\forall x P(x)$

#### Existential Instantiation
* If $\exists x P(x)$ then there must be some $c\in x$ such that $P(c)$

#### Existential Generalization
* If $P(c)$ for some $c\in x$, then $\exists x P(x)$ 

## "Informal Proofs" 
### Trivial and Vacuous
* Vacuous knows that $p$ is false so statement in true
* Trivial knows that $q$ is true, and so statement is true
### Direct Proof
* Show $p\implies q$
### Contraposition
* Show that if not $q$ then $p$
### Contradiction
* Show that $\lnot p\implies F$ is a tautology
* Negate the implication or the contrapositive


## Proofs By Cases
* Divide domain and prove for each domain

## Proof by Exhaustion
* Like induction

## Without Loss of Generality