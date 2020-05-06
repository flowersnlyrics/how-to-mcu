# Printf Specifiers - Submission 1
**DATE** WED MAY 5TH 2020

# Answers
1. What is the format specifier for printing a number in scientific notation?  
  **Answer:** %e or %E  
  Print 1000 in scientific notation.  
  **Answer:**
  >```c
  >printf("The answer to Number 1: %e\n",123456.789);
  >```
  Output: `The answer to Number 1: 1.234568e+05`  
    
2. Print the number -10.  
  **Answer:**
  >```c
  >printf("The answer to Number 2: %d\n",-10);
  >```
  Output: `The answer to Number 2: -10`  
    
3. Print `2.123456` with a minimum width of 3.  
  **Answer:**
  >```c
  >printf("The answer to Number 3: %3.6f\n",2.123456);
  >```
  Output: `The answer to Number 3: 2.123456`  
    
4. Print `5` zero-padded with 3 zeros.  
  **Answer:**
  >```c
  >printf("The answer to Number 4: %04d\n",5);
  >```
  Output: `The answer to Number 4: 0005`  
    
5. Print `12800` in hex.  
  **Answer:**
  >```c
  >
  >```
  Output: ``  
    
6. Print your name using the string format specifier `%s`.  
  **Answer:**
  >```c
  >printf("The answer to Number 6: %s\n","Amanda");
  >```
  Output: `The answer to Number 6: Amanda`  
    
7. Print the 5th letter in your name by indexing a string of your name (learn how to index one character of a string).  
  **Answer:**
  >```c
  >char name[] = "Amanda";
  >printf("The answer to Number 7: %c\n",name[4]);
  >```
  Output: `The answer to Number 7: d`  
    
8. Print the numbers 0 - 10 each with a carriage return escape code and a new line escape code at the end of each number. *Challenge* Try doing this with a for loop.  
  **Answer:**
  >```c
  > for (int i = 0; i < 11; i++){
  >printf("The answer to Number 8: %d\r\n",i);
  >}
  >```
  Output: `The answer to Number 8: 0`  
  `The answer to Number 8: 1`  
  `The answer to Number 8: 2`  
  `The answer to Number 8: 3`  
  `The answer to Number 8: 4`  
  `The answer to Number 8: 5`  
  `The answer to Number 8: 6`  
  `The answer to Number 8: 7`  
  `The answer to Number 8: 8`  
  `The answer to Number 8: 9`  
  `The answer to Number 8: 10`  
    
9. Edit the below `printf` to *only* print out 9 decimal places.
   >```c
   >printf("this is Pi to 9 decimal places: %f \r\n", 3.141592653589793238462643);
   >```
   **Answer:**
   >```c
   >printf("The answer to Number 9: This is Pi to 9 decimal places: %.9f \r\n", 3.141592653589793238462643);
   >```
   Output: `The answer to Number 9: This is Pi to 9 decimal places: 3.141592654`
     
8. Describe the difference between `strlen` and `sizeof`. Write code to show the difference and put it here?  
   **Answer:** sizeof() is used to get the actual size of storage being used (in bytes).  
               strln() is used to get the length of a string stored in an array.  
               Fun fact: a terminating character will be included in the sizeof(), because it takes up a byte, but the strln() will not include it.  
   >```c
   >char lastName[] = "Rovito";
   >int lengthOfString = strlen(lastName);
   >int sizeOfDataType = sizeof(lastName);
   >printf("The answer to Number 10:\n\tThe length of the string is: %d\n\tThe size of the data is: %d\n", lengthOfString,sizeOfDataType);
   >```
   Output `The answer to Number 10:`  
                `The length of the string is: 6`  
                `The size of the data is: 7`  
                  
9. Why is the null terminating character `\0` important? What is it? Use it to print a string and the length of the string you printed.  
   **Answer:** The null character indicates the end of a sequence of characters. It is appended by default in C.  
     
10. Print four random sentences, each on it's own line. Start every other sentence with a tab.  
   **Answer:**  
   >```c
   >printf("The answer to Number 12:\n\tI am learning so much.\nBut there is still so much to learn.\n\tTeach me more please!");
   >```
   Output: `The answer to Number 12:`  
                  `I am learning so much.`  
            `But there is still so much to learn.`  
                  `Teach me more please!`  
     
11. What is `UTF-8`? Why is it needed?  
   **Answer:** UTF-8 is a "multi-byte" encoding scheme. More to come.....
