# Le answers

1. What is the format specifier for printing a number in scientific notation? Print 1000 in scientific notation.
The format specifier for printing a number in scientific notation is `%E`
>```c
>printf("%E\r\n", 1000.0);
>```
2. Print the number -10
>```c
>printf("%i\r\n", -10);
>```
3. Print 2.123456 with a minimum width of 3.
>```c
>printf("%1.2f\r\n", 2.123456);
>```
>This question is vaguely worded so another acceptable answer is 
>```c
>printf("%.3f\r\n", 2.123456);
>```
4. Print 5 zero-padded with 3 zeros.
>```c
>printf("%05d\r\n", 3);
>```
5. Print 12800 in hex.
There are two ways to represent hex numbers in normal text. You can write it with a `0x` at the beginning or you can write it with an `h` at the end. So the hex number `3200` can be written as `0x3200` and `3200h`. The number `12800` in hex is `0x3200`.  
The hex format specifier for printf is `%x`. 
>```c
>printf("%x\r\n", 12800); 
>```
6. Print your name using the string format specifier %s.
>```
>printf("%s\r\n", "Jennifer"); 
>```
7. Print the 5th letter in your name by indexing a string of your name (learn how to index one character of a string).
Remember that all arrays in C are **zero-based**. The printf format specifier for a character is `%c`. 
>```
>char my_name[] = "Jennifer";
>printf("%c\r\n", my_name[4]); 
>```
8. Print the numbers 0 - 10 each with a carriage return escape code and a new line escape code at the end of each number.
```c
>for(int i = 0; i < 11; i++)
>{
>    printf("%d\r\n", i);
>}
```
> Also acceptable, but less sophisticated is this answer.  We're going to go over for loops and while loops in a later lesson so don't worry too much about it.  
```c
>printf("%d\r\n", 0);
>printf("%d\r\n", 1);
>printf("%d\r\n", 2);
>printf("%d\r\n", 3);
>printf("%d\r\n", 4);
>printf("%d\r\n", 5);
>printf("%d\r\n", 6);
>printf("%d\r\n", 7);
>printf("%d\r\n", 8);
>printf("%d\r\n", 9);
>printf("%d\r\n", 10);
```

Edit the below printf to only print out 9 decimal places.
printf("this is Pi to 9 decimal places: %f \r\n", 3.141592653589793238462643);
Describe the difference between strlen and sizeof. Write code to show the difference and put it here?
Why is the null terminating character \0 important? What is it? Use it to print a string and the length of the string you printed.
Print four random sentences, each on it's own line. Start every other sentence with a tab.
What is UTF-8? Why is it needed?
