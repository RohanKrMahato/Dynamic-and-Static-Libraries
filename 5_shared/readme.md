```
cd 5_shared
gcc -fPIC -shared ./src/mymath.c -I./include -o libmymath.dll
gcc -fPIC -shared ./src/mymath2.c -I./include -o libmymath2.dll
```
- use `.so` for linux

```
gcc ./src/main.c -I./include -lmymath -lmymath2 -L./ -o prog
```
- Note: `-lmymath -lmymath2` we are not putting any prefix or suffix, the compiler will itself pre-pend and append it.
- Note: `-L./` means to look in the current for the libraries i.e libmymath.dll and libmymath2.dll

### for linux, we need to set up the LD_LIBRARY_PATH environment variable
```
LD_LIBRARY_PATH="./" ./prog
```