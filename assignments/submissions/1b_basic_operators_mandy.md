# Basic Operators - Submission 1
**DATE** MON MAY 11TH 2020  

# Answers
1. Don't let the user enter `0`. Keep asking user for a number until the number they enter is not `0`. Use this logic for the rest of the assignment.  
*After user enters their numbers...*  
**Answer:**
```c
#include <stdio.h>

static void get_int(char* name, int* buff);
static void get_float(char* name, float* buff);

int main()
{
    int x, y; 
    float a, b; 
    
    printf("**** User input ****\r\n");
    get_int("x", &x); 
    get_int("y", &y); 
    get_float("a", &a); 
    get_float("b", &b); 
    printf("\r\n**** FINAL ****\r\n>>x is %d\r\n>>y is %d\r\n>>a is %f\r\n>>b is %f\r\n", x, y, a, b);

    return 0;
}

static void get_int(char* name, int* buff)
{
    printf("Enter %s: ", name);
    scanf("%d", buff);
    
    while (*buff == 0){
        printf("%s cannot be 0.\nEnter %s: ", name, name);
        scanf("%d", buff);           
    }
    
    printf("%s is %d\r\n", name, *buff);
}

static void get_float(char* name, float* buff)
{
    printf("Enter %s: ", name);
    scanf("%f", buff); 
    
    while (*buff == 0){
        printf("%s cannot be 0.\nEnter %s: ", name, name);
        scanf("%f", buff);           
    }
    
    printf("%s is %f\r\n", name, *buff);
}
```
User Input: `x = 0, x = 0, x = 1, y = 2, a = 1.5, b = 0, b = 1.5`  
Output:  
`**** User input ****`  
`Enter x: 0`  
`x cannot be 0.`  
`Enter x: 0`  
`x cannot be 0.`  
`Enter x: 1`  
`x is 1`  
`Enter y: 2`  
`y is 2`  
`Enter a: 1.5`  
`a is 1.500000`  
`Enter b: 0`  
`b cannot be 0.`  
`Enter b: 1.5`  
`b is 1.500000`  
  
`**** FINAL ****`  
`>>x is 1`  
`>>y is 2`  
`>>a is 1.500000`  
`>>b is 1.500000`  
  
2. Check if `x` is equal to `y`. Print `x equals y` if it returns true. Print `x does not equal y` if it's false.  
**Answer:**  
>```c
>if (x == y){
>    printf("x is equal to y\n");
>}
>else{
>    printf("x does not euqal y\n");
>}
>```
Input: `x = 1, y = 2`  
Output: `x does not euqal y`  
  
Input: `x = 2, y = 2`  
Output `x equals y`  
  
3. Take the modulus of `x` and `y` and print the result.  
**Answer:**
>```c
>printf("The modulus of x and y is: %d", x%y);
>```
Input: `x = 5, y = 3`  
Output: `The modulus of x and y is: 2`  
  
Input: `x = 10, y = 2`  
Output `The modulus of x and y is: 0`  
  
4. Divide, add, multiply and subtract `a` and `b` and print all the results in that order.  
**Answer:**
>```c
>printf("a divided by b is: %f\n", a/b);
>printf("a added to b is: %f\n", a+b);
>printf("a multiplied by b is: %f\n", a*b);
>printf("b subtracted from a is: %f\n\n", a-b);
>```
Input: `a = 2, b = 3`  
Output:  
`a divided by b is: 0.666667`  
`a added to b is: 5.000000`  
`a multiplied by b is: 6.000000`  
`b subtracted from a is: -1.000000`  
    
Input: `a = 10.5, b = 6`  
Output:  
`a divided by b is: 1.750000`  
`a added to b is: 16.500000`  
`a multiplied by b is: 63.000000`  
`b subtracted from a is: 40.500000`  
  
5. If `a` is greater than `b` **and** `x` is less than `y` then print `Amanda is cool`. Otherwise print `Jennifer is cool`.  
**Answer:**
>```c
>if (a > b && x < y){
>   printf("Amanda is the coolest\n\n");
>}
>else{
>   printf("Jennifer is ok. JK, Jennifer is cooler than Amanda\n\n");
>}
>```
Input: `x = 1, y = 2, a = 4, b = 3`  
Output: `Amanda is the coolest`  
  
Input: `x = 2, y = 1, a = 3, b = 4`  
Output: `Jennifer is ok. JK, Jennifer is cooler than Amanda`  

Input: `x = 1, y = 2, a = 3, b = 4`  
Output: `Jennifer is ok. JK, Jennifer is cooler than Amanda`  
  
Input: `x = 2, y = 1, a = 4, b = 3`  
Output: `Jennifer is ok. JK, Jennifer is cooler than Amanda`  

Input: `x = 1, y = 1, a = 2, b = 2`  
Output: `Jennifer is ok. JK, Jennifer is cooler than Amanda`  

6. If `a` is equal to `b` **or** `x` is equal to `y` then print `ah, a set of equal numbers`, otherwise print `alas, no numbers are equal`.  
**Answer:**
>```c
>if (a == b || x == y){
>   printf("ah, a set of equal numbers\n\n");
>}
>else{
>   printf("alas, no numbers are equal\n\n");
>}
>```
Input: `x = 1, y = 1, a = 2, b = 2`  
Output: `ah, a set of equal numbers`  
  
Input: `x = 1, y = 1, a = 2, b = 3`  
Output: `ah, a set of equal numbers`  

Input: `x = 1, y = 2, a = 3, b = 3`  
Output: `ah, a set of equal numbers`  
  
Input: `x = 1, y = 2, a = 3, b = 4`  
Output: `alas, no numbers are equal`  
  
7. If `x` divided by `y` is `>2` then print `2` five times. If `x` divided by `y` is `<2` then print `2` four times. If it's equal to `2` print `2` two times, otherwise just print `"too many twos"`.  
**Answer:**
>```C
>if (x/y > 2){
>   for (int i = 0; i < 5; i++){
>       printf("%d\n\n", 2);
>   }
>}
>else if (x/y < 2){
>   for (int i = 0; i < 4; i++){
>       printf("%d\n\n", 2);
>   }
>}
>else if (x/y = 2){
>   for (int i = 0; i < 2; i++){
>       printf("%d\n\n", 2);
>   }
>}
>else{
>   printf("Too many twos\n\n");
>}
>```
Input: `x = 10, y = 2`  
Output:  
`2`  
`2`  
`2`  
`2`  
`2`  
  
Input: `x = 10, y = 6`  
Output:  
`2`  
`2`  
`2`  
`2`  
  
Input: `x = 10, y = 5`  
Output:  
`2`  
`2`  

8. BONUS: Ask the user to type a goodbye message and make it the last thing you print (after the results of all these questions!) 


