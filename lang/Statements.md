# Statements
This file is about statements and code flow.
## If, Else, Else If
`if` allows to execute code depending on a condition.  
Syntax:  
```
if (condition)
{
    // code here
}
```  
Note: If the condition is *always* constant and the `const` keyword is put just after the `if` keyword, the condition will get resolved at compile-time, meaning that no dead code will get produced.
### Else and Else If
`else` can be used to execute code if the condition in the `if` statement failed.  
`else if` can also be used to check additional conditions.  
Syntax:  
```
if (condition1)
{
    // if true
}
else if (condition2)
{
    // if condition2 is true, these can be stacked
}
else
{
    // if all of the previous if and else if statements failed
}
```
## Switch Statements
A `switch` is a statement that is used to check if values are the same.  
For experienced programmers, *unchecked* `switch` statements can be used.  
**Warning**: Variables declared in a `case` statement can be used everywhere  
and might cause compilation issues.  
Syntax (checked):  
```
switch (value)
{
case 0:         // if the value is 0
    // code here
    break;      // this indicates the end of the label. Without this, the code would continue to
                //the next label.
case 1:
    // some other code here
    continue;   // jumps to the next label
default:        // if all fail
    break;
}
```  
Syntax (unchecked):  
```
switch [value]
{
// labels here
}
```  
Unchecked switch statements are slightly faster (it omits bound checking.)
## Loops
There is a couple of switch statement variants avaiable in Modern.  
Special Keywords:  
 - `break` can be used to *break out* of a loop.  
 - `continue` can be used to skip an iteration.
### While
`while` checks a condition, then, if true, executes code. Syntax:  
```
while (condition)
{
    // code here
}
```
### Do ... While
`do` executes code, then checks a condition and if false, breaks out of the loop. Syntax:  
```
do
{
    // code goes here
} while (condition);
```
### For
`for` executes a statement, the *initialization statement*. Then it checks a condition, and if it is met, it executes code and then executes another statement, the *incrementation*. Example:  
```
for (var int i = 0; i < 300; i++)
{
    // executes code until i reaches 300, iterating over this code 300 times.
}
```
### Foreach
`foreach` iterates over an array, executing code at each iteration. They can forbid or allow the modification of the element in the array. Syntax (readonly):  
```
foreach (type element in array)
{
    // code here, element can be read from, writing to it will not change the contents of the array.
}
```  
Syntax (modification allowed):  
```
foreachm (type @element in array) // foreachm means foreach modifiable.
{
    // code goes here.
}
```