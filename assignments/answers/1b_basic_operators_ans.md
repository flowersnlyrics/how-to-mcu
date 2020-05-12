# Answer for one set of numbers
```c
#include <stdio.h>

static void get_int(char* name, int* buff);
static void get_float(char* name, float* buff);

static void get_int_no_zero(char* name, int* buff);
static void get_float_no_zero(char* name, float* buff);

int main()
{
    int x = 0, y = 0, tmp = 0; 
    float a = 0, b = 0; 
    
    // Get user input 
    printf("**** User input ****\r\n");
    get_int_no_zero("x", &x); 
    get_int_no_zero("y", &y); 
    get_float_no_zero("a", &a); 
    get_float_no_zero("b", &b); 
    printf("\r\n");
    
    // QUESTION 1
    printf("QUESTION 1 RESULT\r\n%s\r\n\r\n", x == y ? "x equals y" : "x does not equal y"); 
    
    // QUESTION 2
    printf("QUESTION 2 RESULT\r\n%d\r\n\r\n", x % y); 
    
    // QUESTION 3
    printf("QUESTION 3 RESULT\r\na/b= %f\ta+b= %f\ta*b=%f\ta-b=%f\r\n\r\n", a/b, a+b, a*b, a-b); 
    
    // QUESTION 4
    printf("QUESTION 4 RESULT\r\n%s\r\n\r\n", ( (a > b) && (x < y) ) ? 
                 "Amanda is cool" : "Jennifer is cool"); 
    
    // QUESTION 5
    printf("QUESTION 5 RESULT\r\n%s\r\n\r\n", ( (a == b) || (x == y) ) ? 
                 "ah, a set of equal numbers" : "alas, no numbers are equal"); 
                 
    // QUESTION 6
    printf("QUESTION 6 RESULT\r\n");
    tmp = x / y;
    
    if(tmp > 2)
    {
        tmp = 5;  
    }
    else if(tmp < 2)
    {
        tmp = 4;
    }
    else if(tmp == 2)
    {
        tmp = 2; 
    }
    
    for(int i=0; i<tmp;i++)
    {
        printf("2\t");
    }
    printf("\r\n\r\n");
    
    // QUESTION 7 BONUS 
    char goodbye[10];
    printf("QUESTION 7 RESULT\r\ntype goodbye\r\n");
    scanf("%s", goodbye); 
    printf("User says \"%s\"\r\n\r\n", goodbye); 
    
    
    printf("\r\n**** FINAL ****\r\n>>x is %d\r\n>>y is %d\r\n>>a is %f\r\n>>b is %f\r\n\r\n", x, y, a, b);

    return 0;
}

static void get_int_no_zero(char* name, int* buff)
{
    get_int(name, buff);
        
    while (*buff == 0)
    {
        printf("%s cannot be 0!\r\n", name);
        get_int(name, buff);
    }
}

static void get_float_no_zero(char* name, float* buff)
{
    get_float(name, buff);
        
    while (*buff == 0)
    {
        printf("%s cannot be 0.0!\r\n", name);
        get_float(name, buff);
    }
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
Don't let the user enter `0`. Keep asking user for a number until the number they enter is not `0`. Use this logic for the rest of the assignment.  
> See functions `get_int_no_zero` and `get_float_no_zero`. Note that part of the assignment is to not change the initial functions. A lot of times you will have to work with people's code (functions, variables, etc) as is. You need to learn to use the code and add onto it in a modular way. 

### Question 7
The last sentence will never happen ... my bad. 


