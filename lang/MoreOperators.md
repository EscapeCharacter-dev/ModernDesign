# More Operators
This file is about operator variants.  
Compiler implementations should generate messages, warnings or even errors on this if the user  doesn't want these variants to be used.
## Equality Operator
The equality operator can be used on data types.
### With structures
With structures, the equality operator will check if all of the members are equal.  
Technical notice: This check is done byte per byte.  
Syntax:  
``struct1 == struct2``
### With unions
With unions, the equality operator will check if the data stored in the unions (bytes) are equal.  
Syntax:  
``union1 == union2``
## Not Equal Operator
The not equal operator can be used on data types.
### With structures
With structures, the not equal operator will check if all of the members aren't equal.
Technical notice: This check is done byte per byte. Also, the check will be done in the order  specified by your endianess. Once it finds an incompatible byte, the check stops immediatly.  
Syntax:  
``struct1 != struct2``
### With unions
With unions, the not equal operator will check if the data stored in the union (bytes) aren't  equal.  
Technical notice: The check will be done in the order specified by your endianess. Once it finds  an incompatible byte, the check stops immediatly.  
Syntax:  
``union1 != union2``
## Direct Assignment Operator
The direct assignment operator can be used to copy members from a structure to another. Improper  casting can result in undefined behaviour.    
Technical notice: This assignment is done byte per byte.  
Syntax:  
``struct1 = struct2``