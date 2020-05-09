# 2: Turing Machine and Finite State Automaton Basics

## Turing Complete
* Set of operations that can compute any computable problem

## Combinational Logic 
* Does not keep track of state
* $y=f(x)$
	* output is input passed to a function
* No 

## Sequential Logic
* Has present state 
* $s$ is state, $i$ is current state
* $s_{i+1} = f(s_{i}, x)$ 
* $y = f(s) | s_{i+1}$

## Finite State Automaton/Machine (FSM)
### States ($S$)
* Finite set of possible states in the FSM

### Alphabet
* Nonempty set of symbols indicating intended use in operations
* Input Alphabet ($\Sigma$)
	* Set of possible inputs
* Output Alphabet ($O$)
	* Set of possible outputs

### Transition Function
* $$T: S_i\times\Sigma \rightarrow S_{i+1}$$

### Output Function
* $$G: S_i\times\Sigma \rightarrow O$$

## Mealy Machine
* Type of FSM used today
* Output values are functions of current state and current inputs
* $F:(\Sigma, S)\rightarrow O$

## Moore Machine
* Output values are functions of current state only
* $\Sigma = \{0,1\}$
* $y_k = f_k(S)$