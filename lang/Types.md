# Types
This file is about Modern Types.
## Integer Types
Modern supports 8-bit, 16-bit, 32-bit and 64-bit.
### 8-bit Integer
A 8-bit Integer is called a ``byte``.  
By default, a ``byte`` is unsigned, but it can be defined as signed using  
``sbyte``.
### 16-bit Integer
A 16-bit Integer is called a ``short``. This type is signed by default.  
To make it unsigned, use ``ushort``.
### 32-bit Integer
A 32-bit Integer is called a ``least32``. This type is signed by default.  
To make it unsigned, use ``uleast32``.
### About Int
The ``int`` and ``uint`` types are supported. They are at least 16-bit long, but they can be  
extended up to 32-bit.
### 64-bit Integer
A 64-bit Integer is called a ``long``. This type is signed by default.  
To make it unsigned, use ``ulong``.
## Floating Types
Modern supports 16-bit, 32-bit and 64-bit.
### 32-bit Floating Point Number
A 32-bit floating point number is called a ``single``.
### 64-bit Floating Point Number
A 64-bit floating point number is called a ``double``.
## Booleans
Booleans are called `bool`.  
Under the hood, booleans are the same size as an `int` for performance reasons.
## Structures
Structures can be used in Modern.  
Syntax (and example):  
```
struct Point3D =    // Point3D is the name of the structure.
    single X,    // 32-bit floating point numbers are perfect for this case.
    single Y,
    single Z;
```
## Unions
Unions can be used in Modern.
Syntax (and example):  
```
union MultiInteger =    // MultiInteger is the name of the union.
    byte,               // Supported types can be declared like so.
    sbyte,
    short,
    ushort,
    int,
    uint,
    least32,
    uleast32,
    long,
    ulong;
```
## Packed Structures
Packed structures can be used in Modern.  
Syntax (and example):  
```
pstruct PackedStruct =  // PackedStruct is the name of the structure.
    int first,      // Padding has to be manually done using integers or by using compiler
                        // features.
    uint second;
```
## Arrays
Arrays can be defined like so:  
```
[]type array;
```  
## Pointers
Pointers can be defined like so:  
```
@type array;
```
## Function Pointers
Function Pointers can be defined like so:  
```
function(params) return_type fptr;
```
## Void
``void`` is used for functions that return nothing.
## Strings
Strings in Modern are C strings. You can declare one using the keyword `string`. This allows you to use multiple 
string manipulation keywords, backed by low-level functions.
## References
References are "pointers" to other symbols. They can only be used as function parameters. They can be declared like so:  
```
ref int myIntReference
```  
You can pass a reference to a variable using the `to` keyword:  
```
my_function(to my_variable);
```
## Compile-time generics
Modern supports compile-time generics. They are declared just before function parameters:   
```
some_function<my_generic>();
```  
You can also create generic structures:  
```
struct my_struct<generic> =
    of generic foo;
```  
Which can be used like:  
```
var my_struct<int> my_structure_with_int;
```  
The `of` keyword allows you to create variables that use a generic type. All of the types are getting resolved at compile-time, so `sizeof(some_generic_type)` will always return constant value.