# Freestanding Module
ModernFreestanding is a module that is linked with all Modern programs by default. It contains non-OS specific functions. This module contains functions like `Memset` and `Strlen`.
## Allocation
These functions can be used to allocate memory.
### Important Notice
The raw functions are not made for beginners. Beginners should use the generic variants, as they are less easy to break.
### Modern::RawMalloc
Signature:  
```
function void @RawMalloc(ulong blockSize)
```  
Description:  
Allocates memory on the heap. This function is equivalent to C's `malloc()` and should be avoided by beginners. See `Modern::Malloc` for a more beginner-friendly alternative.  
Returns:
A pointer to the allocated memory.
### Modern::Malloc
Signature:  
```
function void @Malloc<T>(ulong n)
```  
Description:  
Allocates N objects of type T on the heap. For a C-like version, see `Modern::RawMalloc`.  
Returns:  
A pointer to the allocated memory.
### Modern::Free
Signature:  
```
function void Free(void @ptr)
```  
Description:  
Frees a pointer allocated with `Modern::RawMalloc` or `Modern::Malloc`.
### Modern::Move
Signature:  
```
function void @Move(void @memory)
```  
Description:  
Moves heap-allocated memory in the heap to another address. Can be used to optimize memory access in certain cases.  
Returns:  
A pointer to the moved memory.
### Modern::RawRealloc
Signature:  
```
function void @RawRealloc(void @ptr, ulong new_size)
```  
Description:  
Resizes a memory block. Keeps the data previously allocated. The block's address might have changed (typically caused by `Modern::Move`). Not beginner-friendly, see `Modern::Realloc` for a more beginner-friendly version.  
Returns:  
A pointer to the new memory block.
### Modern::Realloc
Signature:  
```
function void @Realloc<T>(void @ptr, ulong N)
```  
Description:  
Resizes a memory block to fit N objects of types T. Keeps the data previously allocated. The block's address might have changed (typically caused by `Modern::Move`). See `Modern::RawRealloc` for raw memory allocations.