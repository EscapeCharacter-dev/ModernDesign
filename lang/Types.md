# Types
This file is about Modern Types.
## Integer Types
Modern supports 8-bit, 16-bit, 32-bit, 64-bit and 128-bit integers.
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
### 128-bit Integer
A 128-bit Integer is called a ``octa``. This type is signed by default.
To make it unsigned, use ``uocta``.
## Floating Types
Modern supports 16-bit, 32-bit, 64-bit, 80-bit and 128-bit floating point numbers.
### 16-bit Floating Point Number
A 16-bit floating point number is called a ``half``.
### 32-bit Floating Point Number
A 32-bit floating point number is called a ``single``.
### 64-bit Floating Point Number
A 64-bit floating point number is called a ``double``.
### 80-bit Floating Point Number
A 80-bit floating point number is called a ``extended``.
### 128-bit Floating Point Number
A 128-bit floating point number is called a ``quad``.
## Booleans
Booleans are called `bool`.  
Under the hood, booleans are the same size as an `int` for performance reasons.
## Structures
Structures can be used in Modern.  
Syntax (and example):  
```
struct Point3D =    // Point3D is the name of the structure.
    X -> single,    // 32-bit floating point numbers are perfect for this case.
    Y -> single,
    Z -> single;
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
    ulong,
    octa,
    uocta;
```
## Packed Structures
Packed structures can be used in Modern.  
Syntax (and example):  
```
pstruct PackedStruct =  // PackedStruct is the name of the structure.
    first -> octa,      // Padding has to be manually done using integers or by using compiler
                        // features.
    second -> uint;
```
## Arrays
Arrays can be defined like so:  
```
array -> []type;
```  
## Pointers
Pointers can be defined like so:  
```
array -> @type;
```
## Function Pointers
Function Pointers can be defined like so:  
```
fptr -> function return_type(params);
```
## Void
``void`` is used for functions that return nothing.
## Strings
Modern supports Pascal-like strings. It supports multiple string sizes (short strings, which can hold 255 characters, "normal" strings, which can hold 65'534 and long strings for 4'294'967'292).
### Short Strings
Short strings are called ``short_string``. They can contain up to 255 characters, as the first byte is used to figure length.
### "Normal" Strings
Normal strings are called ``string``. They can contain up to 65'534 characters, as the first two bytes are used for length. This is the type used for literal strings.
### Long Strings
Long strings are called ``long_string``. They can contain up to 4'294'967'292 characters, as the first four bytes are used for length. This type is rarely used.
### C strings
C strings are called `cstring`. These strings can contain an unlimited amount of characters, but the string must end with a zero.