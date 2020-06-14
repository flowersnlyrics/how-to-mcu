# Loops galore!
ALL THE LOOPS! Let's learn about not hoops, not dupes, but LOOPS.

### Notes on indexing
All loops, arrays and generally things you iterate over in code are zero-based. For example, the first element in array is considered the 0th element, the second element is the 1st element, so on and so forth. Same with loops, the first iteration is the 0th iteration, the second iteration the 1st iteration, yada, yada, yada. That's why when you see the stop conditions it's usually the number of times the loop ran. In the example below the `for` loop stops after 4 iterations: it runs the 0th, 1st, 2nd and 3rd iterations. 
```c
for(int i = 0; i < 4; i++)
{
  printf("yada, yada, yada\r\n"); 
}
```
### Notes on legacy
Some old firmware may declare the iterator (`i` in the example above) outside of the loop. The compiler (I think) was later updated so that you could declare the iterator in the body of the loop. But you may see the below from time to time or in old firmware and it's not just because someone was being explicit, I think it used to not be allowed. 
```c
int i;

for(i = 0; i < 4; i++)
{
  printf("yada, yada, yada\r\n"); 
}
```

# The `for` loop
Runs a statement a set number of times. You know in advance, pre-compile and pre-run how many time that loop should run. Let's say you want to print the numbers 0 to 9 each on a new line. 
```c
for(int i = 0; i< 10; i++)
{
  printf("#%d\r\n", i);
}
```
Also acceptable (and understand why) is this answer...
```c
for(int i = 0; i<= 9; i++)
{
  printf("#%d\r\n", i);
}
```

# The `while` loop
Runs a statement until a certain condition is true. Using a `while` loop over a `for` loop would be wise when you don't know how many iterations of the loop it will take for a certain condition to be true. For example, if you're waiting for a person to press a button, you don't when they will press the button, or how many times the loop will have to check if they pressed the button. You just know that they will press the button. 
```c
while(!button_pressed)
{
  // Wait here
  printf("why haven't you pressed that dang button\r\n"); 
}
```
The `for` loop in the previous section was great when we knew we wanted to print something *exactly* 4 times, but what if we want to keep printing something until the user presses the dang button?! How damn long is the user going to wait to press the button!!! We keep bugging them until `button_pressed` is `true` (Imagine `button_pressed` being a variable that gets set when a user presses a button on the nucleo...something we will do in a later lesson).

### Side bar
If it helps, you can actually create a for loop with a while loop, and sometimes you have to do this if there's a condition *and* a set number of iterations. For example, let's say we're only going to ask nicely four times (for the user to press the button). After four times we'll get belligerent. The below isn't the best way to code this example, but it illustrates the concept nicely. 
```c
int i = 0; 

while(i < 4 && !button_pressed)
{
  printf("Please press the button :-)\r\n"); 
  i++; 
}

while(!button_pressed)
{
  printf("PRESS THE STUPID BUTTON\r\n"); 
}
```

# The `do...while` loop
If you want to do something at least once before you check the while loop condition then the do-while loop is for you! Let's continue on with this button example. Note that the while loop checks the condition before running anything while the do-while checks the condition after running the contents of the loop. The do while might be preferable here,  seeing as we should at least ask the user once or else how are they supposed to know they have to press the button?
```c
do 
{
  printf("Please press the button!\r\n"); 
} while(!button_pressed); 
```
I honestly think do-while loops are underrated. The alternative to the above do-while loop is redundant and ugly (in my *opinion*). What if some yahoo comes in to edit your code later and only changes one of the two print statements. Unsolicited piece of advice: if you're copy-pastaing code it's spaghetti! But really, if you find yourself Ctrl-C and Ctrl-Ving a lot (been there, done that) stop, pause, Google, reflect. There must be a better way to do it! 
```c
printf("Please press the button!\r\n");
while(!button_pressed)
{
  printf("Please press the button!\r\n");
}
```

# Infinite Loops
Loops that go on forever, and ever and ever and ever and ever andddd evvvveeeeerrrr

### Infinite while loop

The number `1` will always be true, because *it is* `true`. The only way to break an inifinite loop is to use the keyword `break` inside somewhere. For the sake of consistency let's keep using the button example. This loop will forever bug the user to press the button, until the user actually does press the button in which case it will `break` out of the loop and say goodbye. 
```c
while(1)
{
  if(button_pressed)
  {
    break; 
  }
  
  printf("why haven't you pressed that dang button\r\n"); 
}

printf("FINALLY, BYE\r\n"); 
```
### Infinite for loop
Although more rare, still good to be aware of is in the infinite for loop, it's basically a for loop without conditions to stop it. I really don't like these as I think they kind of go against what for loops are meant to be, but you may encounter them and not know what it is so I'm telling you about it. But if you can use a while loop for something with unknown iterations. 
```c
for(;;)
{
  // probably something you could've done in while loop 
  ...
}
