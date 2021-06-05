# The Operators
This file is all about operators.
## Arithmetic Operators
These are the arithmetic operators.
### Addition
Adds two numbers. Syntax:  
``val1 + val2``
### Subtraction
Subtracts two numbers. Syntax:  
``val1 - val2``
### Multiplication
Multiplies two numbers. Syntax:  
``val1 * val2``
### Division & Remainder
Divides two numbers. Syntax (get the quotient):  
``val1 / val2``  
Syntax to get the remainder:  
``val1 % val2``
## Unary operators
These are the unary operators.
### Post-increment
Gets the number, then increments it. Works best with variables. Syntax:  
``val1++``
### Post-decrement
Gets the number, then decrements it. Works best with variables. Syntax:  
``val1--``
### Increment
Increments and gets the number. Works best with variables. Syntax:  
``++val1``
### Decrement
Decrements and gets the number. Works best with variables. Syntax:  
``--val1``
### Negative
Gets the negative value. Syntax:
``-val1``
### Not (logical)
Performs a logical not to a value. Syntax:  
``!val1``
### Not (bitwise)
Performs a bitwise not to a value. Syntax:
``~val1``
## Logic Operators
These are the logic operators.
### Equality
Checks if two numbers/data types (see MoreOperators.md) are equal. Syntax:  
``val1 == val2``
### Not equal
Checks if two numbers/data types (see MoreOperators.md) aren't equal. Syntax:  
``val1 != val2``
### Greater
Checks if a number is greater than another one. Syntax:  
``val1 > val2``
### Lower
Checks if a number is lower than another one.
``val1 < val2``
### Greater or equal
Checks if a number is greater or equal to another one. Syntax:  
``val1 <= val2``
### Lower or equal
Checks if a number is lower or equal to another one. Syntax:  
``val1 >= val2``
### And
Checks if two values are true (not equal to 0). Syntax:  
``val1 && val2``
### Or
Checks if one of two values is true (not equal to 0). Syntax:  
``val1 || val2``
## Bitwise binary operators
These are the bitwise binary operators.
### Binary left shift
Shifts all bits to the left. Syntax:  
``val1 << val2``
### Binary right shift
Shifts all bits to the right. Syntax:  
``val1 >> val2``
### Bitwise And
Performs a bitwise and to two values. Syntax:  
``val1 & val2``
### Bitwise Xor
Performs a bitwise xor to two values. Syntax:  
``val1 ^ val2``
### Bitwise Or
Performs a bitwise or to two values. Syntax:  
``val1 | val2``
## Assignment Operators
These are the assignment operators.
### Direct Assignment
Assigns a value/data types (see MoreOperators.md) to a variable. Syntax:  
``val1 = val2``
### Direct Code Assignment
Assigns code to a function/symbol. Syntax:  
``function myFunc(a -> int, b -> int) -> int : {code}``
### Arithmetic Assignment
Assigns the result of an arithmetic operation to a variable. Syntax:  
Addition: ``val1 += val2``  
Subtraction: ``val1 -= val2``  
Multiplication: ``val1 *= val2``  
Division: ``val1 /= val2``  
Remainder: ``val1 %= val2``
### Bitwise Assignment
Assigns the result of a bitwise operation to a variable. Syntax:  
Left Shift: ``val1 <<= val2``  
Right Shift: ``val1 >>= val2``  
Bitwise And: ``val1 &= val2``  
Bitwise Xor: ``val1 ^= val2``  
Bitwise Or: ``val1 |= val2``
### Logical Assignment
Assigns the result of a logical operation to a variable. Syntax:  
Logical And: ``val1 &&= val2``  
Logical Or: ``val1 ||= val2``  
The other operators are not supported (for this version.)
## Conditional Operator
Assigns a value depending on a condition. Syntax:  
``condition ? val1_if_true : val2_if_false``
## Cast Operator
Casts a value to another type. These types must be compatible. Syntax:  
``to_cast => type``  
For unions:  
``union => type``  
``union = value => type``
## Pointer Operators
These are the pointer operators.
### Address of
Gets the address of a variable. Syntax:  
``@variable``  
Note: To get the address of a function pointer, use:  
``@function_name``
### Value of
Gets the value at the address. Can cause undefined behaviour. Syntax:  
``$pointer``
## Access Operators
These are the operators used to access members of a data type.
### Direct Access
Gets or sets the value directly of a data type (no pointers). Syntax:  
``data.member``
### Pointer Access
Gets or sets the value of a data type represented as a pointer. Syntax:  
``data->member``
## Parenthesized Expressions
Parenthesises can be used to enforce the priority of an operator. Syntax:  
``(expression)``
## Array Access Operator
Gets a value at an index in an array. This can cause undefined behaviour. Syntax:  
``array[index]``
## Other Operators
These are the other operators like ``sizeof``.
### Sizeof
Gets the size of a **type** in bytes. Syntax:  
``sizeof type``
### Lengthof
Gets the length of a fixed sized array or a string. This array must be declared in this context. Syntax:  
```
lengthof array // can also be a string
```
### Type Definition
This special operator is used when declaring a field. Syntax:  
``field -> type``
### Goto
`goto` allows to jump somewhere in memory. Syntax:  
`goto @label1`
### Labels
A `label` is a **private** name for an address to jump to code. Syntax:  
`label MyFirstLabel; // you cannot add code to this statement`