# DIY Learning 
1. What is the format specifier for printing a number in scientific notation? Print 1000 in scientific notation.
The format specifier for printing a number in scientific notation is `%E` or `%e`
>```c
>printf("%E\r\n", 1000.0);
>```
> Also acceptable answer...
>```c
>printf("%e\r\n", 1000.0);
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
4. Print `5` zero-padded with 3 zeros.
>```c
>printf("%03d\r\n", 5);
>```
5. Print 12800 in hex.
There are two ways to represent hex numbers in normal text. You can write it with a `0x` at the beginning or you can write it with an `h` at the end. So the hex number `3200` can be written as `0x3200` and `3200h`. The number `12800` in hex is `0x3200`.  
The hex format specifier for printf is `%x`. 
>```c
>printf("%x\r\n", 12800); 
>```
6. Print your name using the string format specifier %s.
>```c
>printf("%s\r\n", "Jennifer"); 
>```
7. Print the 5th letter in your name by indexing a string of your name (learn how to index one character of a string).  
> Remember that all arrays in C are **zero-based**. The printf format specifier for a character is `%c`. 
>```c
>char my_name[] = "Jennifer";
>printf("%c\r\n", my_name[4]); 
>```
8. Print the numbers 0 - 10 each with a carriage return escape code and a new line escape code at the end of each number.
>```c
>for(int i = 0; i < 11; i++)
>{
>    printf("%d\r\n", i);
>}
>```
> Also acceptable, but less sophisticated is this answer.  We're going to go over for loops and while loops in a later lesson so don't worry too much about it.  
>```c
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
>```
9. Edit the below printf to only print out 9 decimal places. 
>```c
>printf("this is Pi to 9 decimal places: %.9f \r\n", 3.141592653589793238462643);
>```

# Conceptual learning 
10. Why is the null terminating character `\0` important? What is it? Use it to print a string by manually typing out a character array and then using `%s`.  
> The null terminating character `\0` is used to end a string. The null terminating character is so important because it's a delimiter for functions that manipulate strings. The size of a string in bytes is not just the number of characters, it is the number of characters + 1 byte for the null terminating character. If not accounted for this has the potential to cause a buffer overflow. 
>```c
>char my_array[] = {'h', 'e', 'y', '\0'} ; // put your string in this array 
>printf("My string: %s\r\n", my_array );
>```
11. Describe the difference between `strlen` and `sizeof`. Write code to show the difference and put it here?
> `strlen` tells you the number of characters in a string **NOT** including the null terminating character. 
> `sizeof` tells you the number of bytes in *any data type*. Of particular note for this lesson, `sizeof` a string will return the number of characters of in string *plus one*. The plus one being for (you guessed it) the null terminating character. 
>```c
>char name[] = "Jennifer"; 
>printf("strlen my name is %lu\n", strlen(name)); 
>printf("sizeof my name is %lu\n", sizeof(name)); 
>```
12. Print four random sentences, each on it's own line. Start every other sentence with a tab.
>```c
>printf("\tmy first sentence\r\n"); 
>printf("my second sentence\r\n"); 
>printf("\tmy third sentence\r\n");
>printf("my fourth sentence\r\n");
>```
> Also acceptable is 
>```c
>printf("my first sentence\r\n"); 
>printf("\tmy second sentence\r\n"); 
>printf("my third sentence\r\n");
>printf("\tmy fourth sentence\r\n");
>```
13. What is UTF-8? Why is it needed?
> UTF-8 is an encoding scheme needed to formalize character encoding across several different languages. ASCII encoding doesn't cut it since the code can only go up to 127. 

# Follow-up Questions and Answers 
1. You used %i to print -10 and I used %d. Why should you use one over the other?
> They are the same when used for output. It can get tricky when you use them for input. Here's a [stack overflow post](https://stackoverflow.com/questions/1893490/what-is-the-difference-between-conversion-specifiers-i-and-d-in-formatted-io-f) that explains the difference well. We can figure it out later when we use functions in conjunction with `stdin`: right now we're just using `stdout` functions because that's they're easier and used more often.
2. For number 3, the question was to print 2.123456 with a minimum width of 3.
Your answer says - printf("%1.2f\r\n", 2.123456); - but that puts out 2.12. Isn't the 3 the minimum width? not the maximum? also doesn't the decimal count as part of the width? The other acceptable answer - printf("%.3f\r\n", 2.123456); - brings you out three decimal places, but that is different than the width, isn't it?
> Yeah this question is annoyingly worded (my bad). I guess I meant significant figures but I should've just said that. Your answer is fine :) 
3. For number 4, doesn't printf("%05d\r\n", 3); pad it with 4 zeros?
> Okay, this intricacy is important to understand. When you specify `05d` you are saying make sure the number is `5` digits long, and if it's not 5 digits long, pad it with zeros to make up the difference in digit width. So yes it zero-pads the number `3` with four zeros, but it will zero-pad the number `12` with three zeros (`00012`), the number `498` with two zeros (`00498`), the number `1234` with one zero (`01234`) and numbers 5 digits or more will not be zero padded because it meets that minimum width. 
4. So UTF-8 basically normalizes an encoding scheme so that it can be understood by different programming languages?
> Yup. UTF-8 can represent any Unicode character. ASCII is 7-bit so it can only represent 127 characters.
5. While loops and for loops seem to do generally the same thing. Why would you use one over the other?
> A for loop is typically used when you know the number of iterations of a certain action in advance. Like if you wanted to print something `x` number of times (`for(int i=0; i<10;i++)`). A while loop is used when you're waiting on a condition but you're not sure how many iterations of the loop it will take, or how long it will take, to satisfy that condition. For example, you could be waiting for a person to press a button (`while(!button_pressed)`). You don't know how many times we'll have to check (ie. how many times the loop will run) before the person presses the button. 
