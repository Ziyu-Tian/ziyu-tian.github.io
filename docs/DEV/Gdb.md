# Quick Guide to Gdb debug 

## 1: Preparation 

- Use '-g' option to compile:

```cmd 
g++ -g example.cpp -o example.dSYM
```
It will generate a '.dSYM' file contain the debugging parameters.

- Starting the debugging:

```cmd 
gdb example.dSYM 
```

## 2: Setting breakpoints 

```cmd
(gdb) b main 
(gdb) b 30
(gdb) info b 
(gdb) delete 2
```
## 3: Running the program being debugged 

```cmd 
(gdb) r 
(gdb) c
```

## 4: Examining the variables 

```cmd
(gdb) p variable_a 
(gdb) p array[i+1]
```

