# Shared libraries (also called dynamic libraries *.dll*, shared objec file *.so*) vs Static library

[Tutorial Link](https://www.youtube.com/watch?v=YtiPCPtmZrs&t)

## Reduced Memory Usage (Multiple Programs)

- Shared Libraries:
When multiple programs use the same shared library, the operating system can load the library into memory just once. All running programs share the same instance of the library in memory, reducing overall memory consumption.

- Static Libraries:
Each program that links against a static library includes a copy of the library’s code. This means each program has its own copy of the library code in memory, which increases the total memory usage when multiple programs are running.

## Smaller Executable Size

- Shared Libraries:
Executables that link against shared libraries are smaller because they do not include the code from the library itself. Instead, they contain references to the shared library, which is loaded at runtime.

- Static Libraries:
Static libraries are included directly into the executable, making the resulting binary larger. This can be a disadvantage, especially for large programs with many dependencies.

## Dynamic Linking Flexibility

- Shared Libraries:
Dynamic linking allows for more flexibility at runtime. For example, you can replace or upgrade a shared library without needing to recompile or modify the application. This is useful for bug fixes, security patches, or performance improvements.

- Static Libraries:
Static linking ties the program to a specific version of a library. If you need to update the library, you must rebuild the entire application with the new version of the library.