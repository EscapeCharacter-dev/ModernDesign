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
function result MyFunction(type param, type more_param) :
{ // code here

}
```
## Symbol Qualifiers
Symbol Qualifiers change how symbols must be generated and used.
### Public
``public`` outputs the symbol to the module and makes it available to all.
### Clang
``clang`` changes how functions work to match C functions, so that you can compile your code into an object file usable by other C-compatible languages.
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