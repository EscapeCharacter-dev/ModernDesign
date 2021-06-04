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