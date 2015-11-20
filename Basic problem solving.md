Balanced Brackets problem:
A programmer is writing code inside a text processing application. This application needs to catch missing brackets inside any code that is saved. Consider that a programmer typed the following program:
```bash
#include <stdio.h>
 
main()
{
   int value = 1;
 
   while(value<=3)
   {
      printf("Value is %d\n", value);
      value++;
   }
 
   return 0;
}
```
The application will internally filter out the text and extract the brackets in sequence:
###<>(){(){()}}
It is a balanced string as all brackets are properly matched with their respective closing brackets. The nesting within the brackets is also properly balanced.
However consider an example when someone accidentally forgets a closing bracket in the while loop of the above program.
```bash
…
...
while(value<=3)
   {
      printf("Value is %d\n", value);
      value++;


    return 0;
}


…
…
```
The bracket string returned from the whole program would become:
###<>(){(){()}
which is an imbalanced pair of brackets.
There can be many similar mistakes leading to compiler errors, and we need a function to catch such mistakes by taking a given string of brackets as an argument. Only properly matched and nested brackets in the string is a balanced combination. Write a function to return true for a balanced combination and false for an imbalanced combination.
##INPUT:
A string containing 3 different kinds of brackets: <>,{},()
##OUTPUT:
True or false, depending on whether the given string is a properly balanced and nested combination.
#EXAMPLES:
###({{}}) : True
###{}{{}) : False
###{}{}{}{{(}}) : False
###(<>{}{}<{}>) : True
