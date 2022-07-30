# The modifier 'static' in C

> The modifier 'static' have three common usages in C: 
> * Modifier of local variables.
> * Modifier of global variables.
> * Modifier of functions.

## 1. Modifier of Local variables 

If 'static' used in one block or function, this variable can only be called inside this function.

These variables are called **local static variable**, which could keep the value of last call instead of being initialized each time.

The local static variable without initialization will be set as '0'.

For example:

```cpp
void my_function()
{
    int x=0;
    static int y=0;

    printf("x: %d,y:%d\n",x,y);
    x+=5;
    y+=5;
}
int main()
{
    my_function();
    my_function();
    my_function();
    return 0;
}
```

We can find that the static local variable 'y' keep the last call value while the 'x' initialized each time when it was called.

## 2. Modifier of Global variables 

The 'static' variables defined in global can be visited by all the functions in **this file**, but cannot be visited by other file in a project.(Even 'external' cannot)

## 3. Modifier of functions 

The static function can only be called in this file but cannot be called externally.

