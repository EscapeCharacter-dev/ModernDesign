# Untilitary Functions
This file describes all of the functions declared in code used by the compiler optionally.
## For More Operators
To allow "More Operators" to work properly, you will need functions that will perform the operations under the hood.
### Equality
Function declaration in Modern: `__mo_cmpraw(a -> @void, b -> @void, len -> int) -> bool`  
Function declaration in C: `int __mo_cmpraw(void *a, void *b, int len)`  
Expected behaviour: Compares byte per byte two structures or unions to check for equality. The function should stop and return as soon as there is a difference between the two.
### Not Equal
Function declaration in Modern: `__mo_neqraw(a -> @void, b -> @void, len -> int) -> bool`  
Function declaration in C: `int __mo_neqraw(void *a, void *b, int len)`  
Expected behaviour: Compares byte per byte two structures or unions to check for equality. The function should stop and return as soon as there is a difference between the two.
### Copying
Function declaration in Modern: `__mo_copyraw(src -> @void, dest -> @void, len -> int) -> int`  
Function declaration in C: `int __mo_copyraw(void *src, void *dest, int len)`  
Expected behaviour: Copies n bytes from src to to dest (like memcpy.)