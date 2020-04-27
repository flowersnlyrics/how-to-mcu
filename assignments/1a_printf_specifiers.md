

# Printf Specifiers
**DUE DATE** Wednesday, April 29th 2020  

Printf is an important fundamental tool for debugging. In this assignment you can use the `1_uart_printf` project to complete the following problem sets. Before the problem sets, review the fundamentals. Add to this markdown file if you want, I started it for you with a quick summary but you'll need more tools to finish the assignment that you have to Google. 

### Common Specifiers
| format specifier | description                   | 
|------------------|-------------------------------|
| %c               | a character                   |  
| %s               | a string of characters        | 
| %f               | print a floating point number |
| %i | print integer |
| %x | print number in hexadecimal |

### Common Escape Codes
| escape code | description                   | 
|------------------|-------------------------------|
| \n             | new line                |  
| \r             | carriage return     | 
| \t | tab |
| \0 | null terminator (ends strings) |

# Questions
1. What is the format specifier for printing a number in scientific notation? Print 1000 in scientific notation. 
1. Print `-10` with a minimum width of 3.
2. Print `2.123456` with a minimum width of 3.
2. Print `5` zero-padded with 3 zeros. 
3. Print `12800` in hex. 
4. Print your name using the string format specifier `%s`.
5. Print the 5th letter in your name by indexing a string of your name (learn how to index one character of a string).  
6. Print the number 0 - 10 with a carriage return.
7. Edit the below `printf` to *only* print out 9 decimal places.
   >```c
   >printf("this is Pi to 9 decimal places: %f \r\n", 3.141592653589793238462643);
   >```
8. Describe the difference between `strlen` and `sizeof`. Write code to show the difference and put it here?
9. Why is the null terminating character `\0` important? What is it? Use it to print a string and the length of the string you printed. 
10. Print four random sentences, each on it's own line. Start every other sentence with a tab.

# References
*  [MIT printf tips](http://web.mit.edu/10.001/Web/Course_Notes/c_Notes/tips_printf.html)
*  [Tutorial on printf specifiers](https://alvinalexander.com/programming/printf-format-cheat-sheet/)
*  [Printf formatting for dummies](https://www.dummies.com/programming/c/how-to-format-with-printf-in-c-programming/)
