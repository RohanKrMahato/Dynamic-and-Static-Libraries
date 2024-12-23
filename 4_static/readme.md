## Here we will try to `archive` the object files, so as to store together
- All we have to distribute to our friend is the `main.o` and the `mymath.a`
```
cd 4_static
gcc -c ./src/main.c -I./include
gcc -c ./src/mymath.c -I./include
gcc -c ./src/mymath2.c -I./include
```
This will create 3 library files (object file), having .o extension

- Try to `archive` the 2 library files created
```
ar rcs mymath.a mymath.o mymath2.o
```
`.a` for archive
r-does insertion (by replacement) into the archive
c-creates the archive
s-adds an index into the archive (see ranlib as well)

- run the program including the archive
```
gcc main.o mymath.a -o prog
./prog.exe
```

Note:`ar tool` is specifically designed for creating static libraries (i.e., collections of object files), which is different from compression formats like `.zip` or `.rar`.

### When we 'statically link' everything is bundled together. This simplifies distribution to anyone who wants to run './prog'. However, we are packaging *everything* together, so think carefully if this is what you want.