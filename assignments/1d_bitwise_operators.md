# Bitwise Operators 
C has operators that can perform bit manipulation on variables. 

| **Operator** | **Description** |  
|----|----|
| `&` | The AND operator. Operates like and AND Gate. | 
| `\|\|` | The OR operator. Operates like an OR Gate. | 
| `^` | The XOR operator. Operates like an XOR Gate. | 
| `~` | The NOT operator. Operates like a NOT gate (inverter).  | 
| `>>` | Shifts bits to right. After hitting the LSB (least significant bit) the left side will be filled with zeros. | 
| `<<` | Shifts bits to the left. After hitting the MSB (most significant bit) the right side will be filled with zeros. | 

For convenience here are the truth tables for some of the operators. Let the inputs (`A` and `B`) and output (`Y`) be 1-bit numbers.      
**OR Gate `Y = A | B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `1`|
| `1` | `0`| `1`|
| `1` | `1`| `0`|

**AND Gate `Y = A & B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `1`|
| `1` | `0`| `1`|
| `1` | `1`| `0`|

**AND Gate `Y = ~A`**
| **A** | **Y** | 
|----|----|
| `0` | `1`| 
| `1` | `0`| 

### What is the difference between logical and bitwise operators?
The difference between `||` and `|` is that `||` evaluation two operands logically and returns either `true` or `false`, while `|` acts and changes the variable itself. For example, if `A` is `0xC` and `B` is `0x3`...
* `A || B` will check if `A` or `B` is non-zero and return `true` because both numbers are non-zero
* While `Y = A | B` will return `0xC | 0x3` or `Y = 0xF` because `1 | 0` and `1 | 1` both equal `1`
The difference between `&&` and `&` is that `&&` evaluates two operands logically and returns either `true` or `false`, while `&` acts and changes the variable itself. For example, if `A` is `0xA` and `B` is `0x0`...
* `A && B` will check if `A` and `B` are non-zero and return `false` because both numbers are not non-zero
* While `Y = A & B` will return `0xA & 0x0` or `Y = 0x0` because `1 & 0` is `0`.

# Questions
