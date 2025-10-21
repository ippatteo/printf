# ft_printf

## Project Overview
A custom implementation of the printf function from the C standard library. This project recreates the basic functionality of printf with support for various format specifiers.

## Features

### Supported Format Specifiers
- `%c` - Character
- `%s` - String
- `%p` - Pointer address
- `%d` - Decimal (Base 10)
- `%i` - Integer (Base 10)
- `%u` - Unsigned decimal
- `%x` - Hexadecimal (lowercase)
- `%X` - Hexadecimal (uppercase)
- `%%` - Percent sign

## Project Structure
```
.
├── ft_printf.c      # Main printf implementation
├── ft_printf.h      # Header file
├── ft_putchar.c     # Character output
├── ft_putstr.c      # String output
├── ft_putnbr.c      # Number output
├── ft_putnbr_u.c    # Unsigned number output
├── ft_esa.c         # Hexadecimal conversion
├── ft_esa_x.c       # Uppercase hexadecimal conversion
└── Makefile         # Build configuration
```

## Building the Library

```bash
make        # Compile the library
make clean  # Remove object files
make fclean # Remove object files and library
make re     # Recompile the library
```

## Usage

Include the header in your C file:
```c
#include "ft_printf.h"
```

Link with the library when compiling:
```bash
gcc your_program.c -L. -lftprintf
```

Examples:
```c
ft_printf("Character: %c\n", 'A');
ft_printf("String: %s\n", "Hello");
ft_printf("Number: %d\n", 42);
ft_printf("Hexadecimal: %x\n", 255);
ft_printf("Pointer: %p\n", ptr);
```

## Implementation Details
- Variable argument handling with `<stdarg.h>`
- Format string parsing
- Type-specific conversion functions
- Memory-safe string handling
- Return value tracking for printed characters

## Error Handling
- NULL pointer protection
- Invalid format specifier detection
- Buffer overflow prevention
- Return value handling

## Testing
Check `printf/subject and validation/` folder for:
- Project requirements
- Test cases
- Validation tools

## Author
Project developed for 42 school.

## Note
This project demonstrates:
- String manipulation
- Memory management
- Variable arguments
- Type conversion
- Output formatting