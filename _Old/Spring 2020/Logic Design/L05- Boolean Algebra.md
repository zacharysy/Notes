# L05: Boolean Algebra

## Product Term and Minterms
### Literal
* Just one variable 

### Product Term
* All variables are being `and`ed
* Examples: `a,b,ab,a'b`

### Minterm
* Minterms, has all the variables
* Examples (if variables are `a,b,c`): `abc,a'bc,ab'c,abc'` 

## Forms
### Sum-of-Products
* A bunch of product terms `or`d with other product terms

### Sum-of-minterms
* A bunch of minterms `or`d with other minterms
 
 
## NAND/NOR Duality and Universality
* Because of demorgan's law these two things are basically the same with some inverters
*  Everything can be make out of NAND and NOR gates
	*  An inverter is just a NAND/NOR gate with a singe variable put into both inputs