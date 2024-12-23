Here let's create 2 header files

```
cd 3_static
gcc -c ./src/main.c -I./include
gcc -c ./src/mymath.c -I./include
gcc -c ./src/mymath2.c -I./include
```
This will create 3 library files (object file), having .o extension

Try to run the program
```
gcc main.o mymath.o mymath2.o -o prog
./prog.exe
```
