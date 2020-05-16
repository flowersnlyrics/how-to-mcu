# Bitwise Operators 
C has operators that can perform bit manipulation on variables. Below is a summary of the bitwise operators available in the C language.  
| **Operator** | **Description** |  **Example** |
|----|----|----|
| `&` | The AND operator. Operates like and AND Gate. | |
| `\|\|` | The OR operator. Operates like an OR Gate. | |
| `^` | The XOR operator. Operates like an XOR Gate. | |
| `~` | The NOT operator. Operates like a NOT gate (inverter).  | |
| `>>` | Shifts bits to right. After hitting the LSB (least significant bit) the left side will be filled with zeros. | |
| `<<` | Shifts bits to the left. After hitting the MSB (most significant bit) the right side will be filled with zeros. | |
For convenience here are the truth tables for an OR gate and an AND gate. Let `A` and `B` be 1-bit numbers. 
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

### What is the difference between logical and bitwise operators?
The difference between `\|\|` and `|` is that `\|\|` evaluation two operands logically and returns either `true` or `false`, while `|` acts and changes the variable itself. For example, if `A` is `0xF` and `B` is `0x3`...
* `A || B` will check if `A` or `B` is non-zero
* While `A | B` will return `0xF | 0x3` 

# Questions
