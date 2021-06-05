# Declaration & Definition
This file is about declaring variables, constants and functions.
## Variables
Variables can be defined in Modern like so:  
```
var name -> type = value;
// or
var name -> type;
```
## Constants
Constants can be defined in Modern like so:  
```
const name -> type = value;
```  
Constants must have values assigned.
## Functions
Function definition can be done in Modern like so:  
```
function MyFunction(param -> type, more_param -> type) -> result :
{ // code here

}
```
## Symbol Qualifiers
Symbol Qualifiers change how symbols must be generated and used.
### Public
``public`` outputs the symbol to the module and makes it available to all.
### Clang
``clang`` changes how functions work to match C functions, so that you can compile your code into an object file usable by other C-compatible languages.
## Explicit string sizes
You can specify an explicit size when declaring a string like so:  
```
const myStr -> string(50) = "A string with a fixed capacity of 50."; // const is recommended
```
## Arrays (and strings)
### Specify array size
You can specify the size of an array using a variable or a literal constant. Syntax:  
```
const myArray -> [2]string(10) = {"First", "Second"}; // const is recommended
// this code declares an array with a fixed size of 2, containing 10 text characters long strings.
```
### Access
You can access values in an array using square brackets. Syntax:  
```
myArray[1]
```  
**Important Notice**: Indexing starts at 0.