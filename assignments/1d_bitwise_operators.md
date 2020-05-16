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

# Truth Tables
For convenience here are the truth tables for some of the operators. Let the inputs (`A` and `B`) and output (`Y`) be 1-bit numbers.  
### **OR Gate `Y = A | B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `1`|
| `1` | `0`| `1`|
| `1` | `1`| `0`|

### **AND Gate `Y = A & B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `1`|
| `1` | `0`| `1`|
| `1` | `1`| `0`|

### **AND Gate `Y = ~A`**
| **A** | **Y** | 
|----|----|
| `0` | `1`| 
| `1` | `0`| 

### Shift operations
Shift operations can be a little tricky when you're first learning them. Think of binary! When you shift something left you are multiplying it by 2 because you are moving it up one binary place. When you shift something right you are dividing it by 2 because you are moving it down one decimal place. Think of a 4-bit binary number.
**4-bit binary number**
| **bit place** | **power of two** | **4-bit representation***|
| ----| ----| ----|
| `0` | `2^0` | `0b0001` |
| `1` | `2^1` | `0b0010` |
| `2` | `2^2` | `0b0100` |
| `3` | `2^3` | `0b1000` |
Let's say that a 4-bit binary number `A` is equal to `4`, which is equal to `0b0100`. If you multiply `4` by `2` you get `8`. The binary representation of `8` is `0b1000`. Notice that the multiplication of the number shifted it one binary place left. Now let's divide the number by `4`. Note that `4` is `2^2`, that means when we divide by four we are shifting the decimal place 2 places right. The result of `8` divided by `4` is `2`. The number `2` represented in binary is `0b0010`. Notice that from the number `8` (which is `0b1000`) that the binary shifts two places to the right, because we divided by `4` which is `2^2` which is why we shifted **2** places.  These operations will get a lot more complicated, but knowing the basics will help. 

### What is the difference between logical and bitwise operators?
The difference between `||` and `|` is that `||` evaluation two operands logically and returns either `true` or `false`, while `|` acts and changes the variable itself. For example, if `A` is `0xC` and `B` is `0x3`...
* `A || B` will check if `A` or `B` is non-zero and return `true` because both numbers are non-zero
* While `Y = A | B` will return `0xC | 0x3` or `Y = 0xF` because `1 | 0` and `1 | 1` both equal `1`
The difference between `&&` and `&` is that `&&` evaluates two operands logically and returns either `true` or `false`, while `&` acts and changes the variable itself. For example, if `A` is `0xA` and `B` is `0x0`...
* `A && B` will check if `A` and `B` are non-zero and return `false` because both numbers are not non-zero
* While `Y = A & B` will return `0xA & 0x0` or `Y = 0x0` because `1 & 0` is `0`.

# Questions


