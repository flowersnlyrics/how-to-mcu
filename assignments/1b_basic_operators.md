# Basic Operators
**RELEASED** SUN MAY 10TH 2020   
**DUE DATE** WED MAY 13TH 2020  

I'm not giving as much time for lesson because it should be easy. There are a few tricky operators such as `%`, `||` and `&&` that we don't see in everyday arithmetic or sixth grade algebra but once you do a couple problems it should become pretty easy and be a powerful tool in our kit for later, harder lessons. Again, not all information you need is here. You should Google:) You can use `1_uart_printf` project, but I recommend using an [online C compiler](https://www.onlinegdb.com/online_c_compiler) as it's quicker. 

### Logical Operators
Used to compare to stuff!
| operator | description | example |
|------------------|-------------------------------|----|
| `&&` | The AND operator. Works like an [AND gate](https://en.wikipedia.org/wiki/AND_gate). |  `x && y`, check if `x` and `y` are *both* true. Also, see truth table for AND gate. |
| `\|\|` | The OR operator. Works like an [OR gate](https://en.wikipedia.org/wiki/OR_gate). |  `x \|\| y`, check if *either* `x` or `y` is true.  Also, see truth table for OR gate. |
| `!`  | The NOT operator. Takes the opposite of its operand. Works like an inverter.  | !true = false |

### Arithmetic Operators 
Used to do math. Other operators include `+`, `-`, `=` and `/`.
| operator | description | example |
|------------------|-------------------------------|----|
| `%` | The MOD operator. Finds the remainder after one integer is divided by another. | `3 % 2 = 1`, `4 % 5 = 4` |
| `++` | Cool shorthand in C for saying take the number and add one to it. | `10++ = 11` |
| `--` | Cool shorthand in C for saying take the number and subtract one from it. | `10-- = 9` |
| `*` | Multiply two numbers |  `4 * 5 = 20` |
| `+=` | Take a number, add something to it and set the result equal to the first number |  `x += 5` is the same as saying x = x + 5 |
| `-=` | Take a number, subtract something from it and make set the result equal to the first number |  `x -= 5` is the same as saying x = x - 5 |
| `*=` | Take a number, multiply it by 5 and set the result equal to the first number |  `x *= 5` is the same as saying x = x * 5 |
| `/=` | Take a number, divide it by 5 and set the result equal to the first number |  `x /= 5` is the same as saying x = x / 5 |

### Relational Operators
These are pretty much the same from whatever algebra class you took minus a few I've outlined below. Other operators include `<`, `>`, `>=`, and `<=`.
| operator | description | example |
|------------------|-------------------------------|----|
| `==` | Check if two numbers are equal to each other | `1 == 1` is true, `1 == 0` is false |
| `!=` | Check if two numbers are not equal to each other | `1 != 0` is true, `1 != 1` is false |

# Questions
For all questions: add and edit the code below. For submission show the outputs of several different sets of numbers to prove that your code is robust. Do not change the functions `get_int` or `get_float`, use them as I've used them below. We haven't gone over `scanf` and `stdin` yet which is why I got the lesson started. Don't change the values of `a`, `b`, `x` and `y`. Use intermediate variables or put the operation directly into the `printf` argument.

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
    printf("%s is %d\r\n", name, *buff);
}

static void get_float(char* name, float* buff)
{
    printf("Enter %s: ", name);
    
    scanf("%f", buff); 
    printf("%s is %f\r\n", name, *buff);
}
```
1. Don't let the user enter `0`. Keep asking user for a number until the number they enter is not `0`. Use this logic for the rest of the assignment.  
*After user enters their numbers...*
1. Check if `x` is equal to `y`. Print `x equals y` if it returns true. Print `x does not equal y` if it's false. 
2. Take the modulus of `x` and `y` and print the result. 
3. Divide, add, multiply and subtract `a` and `b` and print all the results in that order. 
4. If `a` is greater than `b` **and** `x` is less than `y` then print `Amanda is cool`. Otherwise print `Jennifer is cool`. 
5. If `a` is equal to `b` **or** `x` is equal to `y` then print `ah, a set of equal numbers`, otherwise print `alas, no numbers are equal`. 
6. If `x` divided by `y` is `>2` then print `2` five times. If `x` divided by `y` is `<2` then print `2` four times. If it's equal to `2` print `2` two times, otherwise just print `"too many twos"`.
7. BONUS: Ask the user to type a goodbye message and make it the last thing you print (after the results of all these questions!) 

# References
*  [TutorialsPoint Operators Tutorial](https://www.tutorialspoint.com/cprogramming/c_operators.htm)

