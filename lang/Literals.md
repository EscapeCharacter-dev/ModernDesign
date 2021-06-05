# Literals
This file describes how literal types can be used.
## Literal Numbers
These numbers are the numbers you write on your keyboard and hardwire into your code.
### Decimal Representation
Literal numbers can be represented as decimal by simply writing them out. For example:  
```
300 // the number 300
```
### Hexadecimal Representation
Literal numbers can be represented through hexadecimal, AKA base 16. Syntax:  
```
0x12C   // the number 300, as hexadecimal. 0x is the prefix.
```
### Binary Representation
Literal numbers can be represented through binary. Syntax:  
```
0b100101100 // the number 300, as binary. 0b is the prefix.
```
### Octal Representation
Literal numbers can be represented through octal, AKA base 8. Syntax:  
```
0o454 // the number 300. 0o is the prefix.
```
## Character Literals
Character literals are used to represent text characters. Syntax:  
```
'A' // the A letter in ASCII
```
### Suffixes
Suffixes can be used to alter character literals.  
 - a/A, for ASCII. `'A'a` means the letter A in ASCII. ASCII is the default encoding used.
 - u/U, for UTF-8. `'A'u` means the letter A in UTF-8.
## String Literals
String literals are used to represent text.  
Unicode *strings* is not supported as of this standard.
### Short Strings
Short string literals can be used like so:  
```
S"The quick fox jumps over the lazy dog."
```
### "Normal" Strings
Normal string literals can be used like so:  
```
"The quick fox jumps over the lazy dog."
// or
N"The quick fox jumps over the lazy dog."
```
### Long Strings
Long string literals can be used like so:  
```
L"The quick fox jumps over the lazy dog."
```
