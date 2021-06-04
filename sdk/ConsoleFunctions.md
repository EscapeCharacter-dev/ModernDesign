# Console Functions
This file documents the functions that interact with the console.
## ``PrintShortString``
Usage: ``PrintShortString(text -> short_string) -> void``  
Writes a short string to the console.
## ``PrintString``
Usage: ``PrintShortString(text -> string) -> void``  
Writes a "normal" string to the console.
## ``PrintLongString``
Usage: ``PrintShortString(text -> long_string) -> void``  
Writes a long string to the console.
## ``PrintLineShortString``
Usage: ``PrintLineShortString(text -> short_string) -> void``  
Writes a short string to the console then passes a line.
## ``PrintLineString``
Usage: ``PrintLineString(text -> string) -> void``  
Writes a "normal" string to the console then passes a line.
## ``PrintLineLongString``
Usage: ``PrintLineLongString(text -> long_string) -> void``  
Writes a long string to the console then passes a line.
## ``ReadC``
Usage: ``ReadC() -> char``  
Reads a character from stdin.
## ``ReadCCount``
Usage: ``ReadCCount(buffer -> @char, count -> int) -> int``  
Reads multiple characters from stdin then puts them into a buffer.  
Returns the number of characters read.
## ``ReadCCountString``
Usage: ``ReadCCountString(buffer -> @string, count -> int) -> int``  
Reads multiple characters from stdin then puts them into a string buffer.  
Returns the number of characters read.
## ``ReadLine``
Usage: ``ReadLine(buffer -> @string) -> int``  
Reads a line from stdin then puts it into a buffer.  
Returns the number of characters read.