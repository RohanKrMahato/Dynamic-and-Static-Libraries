```
cd 2_static
gcc -c ./src/main.c -I./include
gcc -c ./src/mymath.c -I./include
```
This will create 2 library files (object file), having .o extension

Try to run the program
```
gcc main.o mymath.o -o prog
./prog.exe
```