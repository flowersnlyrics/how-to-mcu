# Answer for one set of numbers
```c
static void get_int(char* name, int* buff);
static void get_float(char* name, float* buff);

static void get_int_no_zero(char* name, int* buff);
static void get_float_no_zero(char* name, float* buff);

int main()
{
    int x = 0, y = 0; 
    float a = 0, b = 0; 
    
    printf("**** User input ****\r\n");
    
   
    get_int_no_zero("x", &x); 
    get_int_no_zero("y", &y); 
    get_float_no_zero("a", &a); 
    get_float_no_zero("b", &b); 
    
    printf("\r\n**** FINAL ****\r\n>>x is %d\r\n>>y is %d\r\n>>a is %f\r\n>>b is %f\r\n", x, y, a, b);

    return 0;
}

static void get_int_no_zero(char* name, int* buff)
{
    get_int(name, buff);
    
    do
    {
        printf("%s cannot be 0!\r\n", name);
        get_int(name, buff);
    } while (*buff == 0) ;
}

static void get_float_no_zero(char* name, float* buff)
{
    get_float(name, buff);
    
    do
    {
        printf("%s cannot be 0!\r\n", name);
        get_float(name, buff);
    } while (*buff == 0.0) ;
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
### Don't let user enter zeros 
1. Don't let the user enter `0`. Keep asking user for a number until the number they enter is not `0`. Use this logic for the rest of the assignment.  
> See functions `get_int_no_zero` and `get_float_no_zero`. Note that part of the assignment is to not change the initial functions. A lot of times you will have to work with people's code (functions, variables, etc) as is. You need to learn to use the code and add onto it in a modular way. 

### x = 1, y = 4, a = 1.0, b = 1.0 TODO 
1. Check if `x` is equal to `y`. Print `x equals y` if it returns true. Print `x does not equal y` if it's false. 
2. Take the modulus of `x` and `y` and print the result. 
3. Divide, add, multiply and subtract `a` and `b` and print all the results in that order. 
4. If `a` is greater than `b` **and** `x` is less than `y` then print `Amanda is cool`. Otherwise print `Jennifer is cool`. 
5. If `a` is equal to `b` **or** `x` is equal to `y` then print `ah, a set of equal numbers`, otherwise print `alas, no numbers are equal`. 
6. If `x` divided by `y` is `>2` then print `2` five times. If `x` divided by `y` is `<2` then print `2` four times. If it's equal to `2` print `2` two times, otherwise just print `"too many twos"`.
7. BONUS: Ask the user to type a goodbye message and make it the last thing you print (after the results of all these questions!) 

### x = 100, y = 40, a = 471.0, b = 1000.7 TODO 
1. Check if `x` is equal to `y`. Print `x equals y` if it returns true. Print `x does not equal y` if it's false. 
2. Take the modulus of `x` and `y` and print the result. 
3. Divide, add, multiply and subtract `a` and `b` and print all the results in that order. 
4. If `a` is greater than `b` **and** `x` is less than `y` then print `Amanda is cool`. Otherwise print `Jennifer is cool`. 
5. If `a` is equal to `b` **or** `x` is equal to `y` then print `ah, a set of equal numbers`, otherwise print `alas, no numbers are equal`. 
6. If `x` divided by `y` is `>2` then print `2` five times. If `x` divided by `y` is `<2` then print `2` four times. If it's equal to `2` print `2` two times, otherwise just print `"too many twos"`.
7. BONUS: Ask the user to type a goodbye message and make it the last thing you print (after the results of all these questions!) 
