# Declaration & Definition
This file is about declaring variables, constants and functions.
## Variables
Variables can be defined in Modern like so:  
```
var type name = value;
// or
var type name;
```
## Constants
Constants can be defined in Modern like so:  
```
const type name = value;
```  
Constants must have values assigned.
## Functions
Function definition can be done in Modern like so:  
```
function result MyFunction(type param, type more_param)
{ // code here

}
```
## Symbol Qualifiers
Symbol Qualifiers change how symbols must be generated and used.
### Public
``public`` outputs the symbol to the module and makes it available to all.
### Clang
``clang`` changes how functions work to match C functions, so that you can compile your code into an object file usable by other C-compatible languages.
### Register (2021.09)
``register`` specifies that this local variable/function argument must be stored in a register.
### Return Register (2021.09)
``return register`` specifies that this local variable/function argument must be stored in the accumulator.  
There can only be one function ``return register`` function argument.
### Static (2021.09)
``static`` statically allocates a variable. It will not get allocated on the stack, but rather in the binary.
## Arrays (and strings)
### Specify array size
You can specify the size of an array using a variable or a literal constant. Syntax:  
```
const cstring[2] myArray ->  = {"First", "Second"}; // const is recommended
// this code declares an array with a fixed size of 2, containing 2 cstrings.
```
### Access
You can access values in an array using square brackets. Syntax:  
```
myArray[1]
```  
**Important Notice**: Indexing starts at 0.