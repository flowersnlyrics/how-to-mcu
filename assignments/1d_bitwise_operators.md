# Bitwise Operators 
It's important that you do these exercises on paper before checking them with the online C compiler (or `1_uart_printf`). C has operators that can perform bit manipulation on variables, which comes in handy in a lot of embedded applications. For the submission of this application learn how to integrate the pictures of handwritten work into your markdown submission. Also submit the code you wrote to double check your answers. It's important to understand bitwise operations before we move on because it's a critical part of the foundation. 

| **Operator** | **Description** |  
|----|----|
| `&` | The AND operator. Operates like an AND Gate. | 
| `\|\|` | The OR operator. Operates like an OR Gate. | 
| `^` | The XOR operator. Operates like an XOR Gate. | 
| `~` | The NOT operator. Operates like a NOT gate (inverter).  | 
| `>>` | Shifts bits to right. After hitting the LSB (least significant bit) the left side will be filled with zeros. | 
| `<<` | Shifts bits to the left. After hitting the MSB (most significant bit) the right side will be filled with zeros. | 

## Truth Tables
For convenience here are the truth tables for some of the operators. Let the inputs (`A` and `B`) and output (`Y`) be 1-bit numbers.  
### **OR Gate `Y = A | B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `1`|
| `1` | `0`| `1`|
| `1` | `1`| `1`|

### **AND Gate `Y = A & B`**
| **A** | **B** | **Y** | 
|----|----|---|
| `0` | `0`| `0`|
| `0` | `1`| `0`|
| `1` | `0`| `0`|
| `1` | `1`| `1`|

### **XOR Gate `Y = A ^ B`**
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

## Shift operations
Shift operations can be a little tricky when you're first learning them. Think of binary! When you shift something left you are multiplying it by 2 because you are moving it up one binary place. When you shift something right you are dividing it by 2 because you are moving it down one decimal place. Think of a 4-bit binary number.  
| **bit place** | **power of two** | **4-bit representation***|
| ----| ----| ----|
| `0` | `2^0 = 1` | `0001` |
| `1` | `2^1 = 2` | `0010` |
| `2` | `2^2 = 4` | `0100` |
| `3` | `2^3 = 8` | `1000` |

Let's say that a 4-bit binary number `A` is equal to `4`, which is equal to `0b0100`. If you multiply `4` by `2` you get `8`. The binary representation of `8` is `0b1000`. Notice that the multiplication of the number by `2` shifted it one binary place left. As a shift operation this multiplication is represented by `A << 1`.  Now let's divide the number by `4`. Note that `4` is `2^2`, that means when we divide by four we are shifting the binary place *2* places right. The result of `8 / 4` is `2`. The number `2` represented in binary is `0b0010`. Now: from the number `8` (which is `0b1000`) the binary shifts two places to the right. When we divided by `4` we shifted the number *two* places right. This division can also be represented with a shift operation: `A >> 2`. These operations will get a lot more complicated, but knowing the basics will help. 
| **Math** | **Equivalent shift operation** | **Result** |
| ----|----|---|
| `A * 2`  | `A << 1` | `0100 << 1 = 1000 ` |
| `A / 4`  | `A >> 2` | `1000 >> 2 = 0010` |

## What is the difference between logical and bitwise operators?
The difference between `||` and `|` is that `||` evaluates two operands logically and returns either `true` or `false`, while `|` acts and changes the variable itself. For example, if `A` is `0xC` and `B` is `0x3`...
* `A || B` will check if `A` or `B` is non-zero and return `true` because both numbers are non-zero
* While `Y = A | B` will return `0xC | 0x3` or `Y = 0xF` because `1 | 0` and `1 | 1` both equal `1`  

The difference between `&&` and `&` is that `&&` evaluates two operands logically and returns either `true` or `false`, while `&` acts and changes the variable itself. For example, if `A` is `0xA` and `B` is `0x0`...
* `A && B` will check if `A` and `B` are non-zero and return `false` because both numbers are not non-zero
* While `Y = A & B` will return `0xA & 0x0` or `Y = 0x0` because `1 & 0` is `0`.

# Questions
### Round 1: Assume 8-bit unsigned numbers. Perform these operations with `A` being `60` and `B` being `123`. Give the result in binary, hex and decimal. **ALL BY HAND FOR PRACTICE**
1.  `A & B`
2. `A | B`
3. `A ^ B`
3. `A >> 5`
4. `A << 7`
5. `B >> 3`
6. `B << 1`
7. `~B`
8. `~A`  

### Round 2: Assume 16-bit unsigned numbers. Perform these operations with `A` being `20154` and `B` being `58742`.   Give the result in binary, hex and decimal. **ALL BY HAND FOR PRACTICE**
1.  `A & B`
10. `A | B`
3. `A ^ B`
11. `A >> 12`
12. `A << 9`
13. `B >> 4`
14. `B << 7`
15. `~B`
16. `~A`

### Round 3: Write C code to double check your answers. Post the C code with your submission
