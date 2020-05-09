# L09: Introduction to Behavioral Modeling

## Verilog Arithmetic Relational Operators
### Arithmetic
* `+, -, <<, >>, * , /, %`

### Relational
* `<, >, <=, >=, =, !`

## Other Operations
### Reduction Operators
* Can do something across all the bits of something
* Example (XOR): `assign f = ^a;`

### Concatenation Operator (Joining 2 vectors)
```
input [7:0] a
input [7:0] b
input [7:0] z

assign z = {a,b}
```

#### Padding with 0s
```
output [7:0] char
input [3:0] n

assign char = {4'b0, n}
```

#### Checksum
```
input [7:0] p
output [8:0] out

assign out = {p,^p};
```

## Describing Behavior
### 2:1 Mux with "if"
* Two inputs and one bit select line

```
if (s == 0)
	f = a
else
	f = b
```

### 4:1 Mux with "case"
* four inputs and two bit select line

```
case (s)
	0: f = a
	1: f = b
	2: f = c
	3: f = d
endcase
```

### Always
* Keyword to loop continuously and keep evaluating

```
module xor_always(
	input a,
	input b,
	output reg f
	);
	
	always @(*) begin
		// reg doesn't need assign inside
		f = ~a & b | a & ~b;	
	end

endmodule
```

#### Sensitivity List
* `@(*)`
* What changes of input to listen to

## Verilog assign, initial, always
### Assign Statements
* For wires
* Outside of always/initial

### Initial Statement
* Signals are type reg
* no assign keyword
* happens only once

### Always Statement
* Continuously evaluates
* looks at sensitivity
* Uses reg, not wire
* no assign keyword

#### Sensitivity List 
* Combinatorial Logic
	* `always @(*)`
* Memory (sequential) logic
	* `always #(pos egde of clock)` 


## Latch