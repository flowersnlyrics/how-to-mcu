# Number Representation 

### Binary Numbering System  
Binary is a base 2 numbering system, as opposed to the decimal system which is base 10. Binary consists of just two numbers - 0 and 1 (off and on). Binary is the primary language for computers.  

For a binary number, the most significant bit (MSB) is the digit furthest to the left and the least significant bit (LSB) is the digit furthest to the right. For large binary strings, they are often grouped in sets of 4 bits (aka a nibble, or half-byte).  

**Converting Binary to Decimal**  
Each bit represents the number 2 raised to an exponent, which increases by one as you move from right to left. To convert a number from binary to decimal, add together the values of the 2 raised to the exponent for all *on* bits (1s).
|1|0|0|1|0|1|1|1|  
|---|---|---|---|---|---|---|---|  
|2<sup>7</sup>|2<sup>6</sup>|2<sup>5</sup>|2<sup>4</sup>|2<sup>3</sup>|2<sup>2</sup>|2<sup>1</sup>|2<sup>0</sup>|  
|128|64|32|16|8|4|2|1|  
  
128 + 16 + 4 + 2 + 1 = **151** 
  
This means the maximum value of a byte (8 bits) is 255.  
|1|1|1|1|1|1|1|1| 
|---|---|---|---|---|---|---|---|  
|2<sup>7</sup>|2<sup>6</sup>|2<sup>5</sup>|2<sup>4</sup>|2<sup>3</sup>|2<sup>2</sup>|2<sup>1</sup>|2<sup>0</sup>|  
|128|64|32|16|8|4|2|1|

128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = **255** 

**Converting Decimal to Binary**  
Remainder method: Divide the number by 2 continuously until you get to 0. The remainder after each division is the value of the bit from LSB to MSB.  

100 / 2 = 50 Remainder 0 (LSB)  
50 / 2 = 25 Remainder 0  
25 / 2 = 12 Remainder 1  
12 / 2 = 6 Remainder 0  
6 / 2 = 3 Remainder 0  
3 / 2 = 1 Remainder 1  
1 / 2 = 0 Remainder 1 (MSB)  
  
Result: 110 0100
 
### Hexadecimal Numbering System  
Hexadecimal is a base 16 numbering system, and is often used to represent long binary numbers because the format is compact and easier to understand than a long binary string. Hex consists of 16 number symboles, 0 through 15. Becuase there could be confusion between the number systems, hex uses letters to identify the values of 10 to 15 i.e. A, B, C, D, E, and F respectively.  
*Fun Fact:* Hexadecimal Numbers is a more complex system than using just binary or decimal and is mainly used when dealing with computers and memory address locations.  

As mentioned, long binary strings are often grouped in sets of 4 bits. In relation to hex, this allows a min of 0 (0000) and max of 15 (1111). So each digit in hex represents a nibble in binary.

|Decimal|Binary|Hex  
|---|---|---|  
|0|0000|0|  
|1|0001|1|  
|2|0010|2|  
|3|0011|3|  
|4|0100|4|  
|5|0101|5|  
|6|0110|6|  
|7|0111|7|  
|8|1000|8|  
|9|1001|9|  
|10|1010|A|  
|11|1011|B|  
|12|1100|C|  
|13|1101|D|  
|14|1110|E|  
|15|1111|F|  

**Converting Binary to Hex**  
1001 0111 = 0x97  
1111 1111 = 0xFF  
0110 0100 = 0x64  

### Two's Compliment  
Pending...  
  
# References
*  [Computer Hope - Binary](https://www.computerhope.com/jargon/b/binary.htm)
*  [Electronics Tutorials](https://www.electronics-tutorials.ws/binary/bin_3.html)
