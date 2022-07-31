# The 'Pass-by-Value' and 'Pass-by-Reference' in C

## Pass-by-Value 

As a simple but classic example of pass-by-value, we cannot use the method below to swap two values:

```cpp
void swap(int a,int b)
{
    int temp = a;
    a = b;
    b = temp;
    printf("swap a = %d,b = %d\n",a,b);
}
swap(a,b);
```
If we call the 'swap(a,b)', then print the a and b, the answer will show that the 'a' and 'b' still keep the original value. That is cause the function call in C are *pass-by-value*. 

The *pass-by-value* means when passing by the parameters, the function only pass a 'copy' of the origin parameters, so the 'swap()' can only change the value of the 'copy' instead of the origin values. After the call of the function 'swap()', the 'copy' value will be 'undefined' again.

In order to operate the original value, we have to use *pass-by-reference*, which can simply treated as **'use pointers'** at beginning.

## Pass-by-Reference 

Still focus on the swap function, if we use the pointers (pass-by-value) as the parameter of function, the code will be:

```cpp
void swap(int *a,int *b)
{
    int temp = *a;
    *a = *b;
    *b = temp;
    printf("swap a = %d,b = %d\n",*a,*b);
}
swap(&a,&b);
```

In fact, the pointers are also kind of *pass-by-value*, but the type of the value is pointer.

## Summary 

* The parameters in function are only 'copy', which cannot be changed inside the function.
* The only way to change the parameters in function is to **input the address (pointer) of the parameter**, use indirection to change what it points to.
