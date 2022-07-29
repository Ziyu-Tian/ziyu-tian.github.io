# A Simple Understanding of Time & Space Complexity
## 1: Time Complexity
> In computer science, the time complexity is the computational complexity that describes the amount of computer time it takes to run an algorithm.[<sup>1</sup>](#refer-anchor).
>The most obvious method to judge an algorithm is the response speed, which is the base of algorithm: time & space complexity.

### The big O notation 

We use the initial 'O' to express the time complexity of algorithm, such as $O(1)$,$O(n)$,$O(logn)$, $O(nlogn)$ and $O(n^2)$.

The **time complexity** is used to represent the relation between execution time and the increasing of data size. This method cannot express the precise execution time, but *'tendency'* and *'relationship'*instead.

Here are some examples below.

### O(1) Constant Time 

The '1' in $O(1)$ means 'constant',refer to the **constant efficiency** no matter how the data size changing, which have the most efficient algorithm.

```cpp
int a=1;
int b=2;
int sum=a+b;
printf("%d",sum);
```
Without **loop**, **recursive** and other complex structure, the complexity will be constant no matter how much the lines are.

### O(n) Linear time 

For example:

```cpp
int a=0;
for(int i=0;i<n;i++)
{
    a+=i;
    printf("%d\n",a);
}
```
If we treat that the execution time for each line code are same 'T' and only consider the for() loop part, as the loop times are 'n', the total time will be nT, so the relationship will be $O(n)$.

### $O(n^2)$ Quadratic time 

The double nested loop will produce $O(n^2)$ and 'k' nested loop will be $O(n^k)$.

The code below is $O(n^2)$:

```cpp
int sum=0;
for(int i=0;i<n;i++)
{
    for(int j=0;j<0;j++)
    {
        sum+=j;
    }
}
```

### $O(logn)$ Logarithmic time 

For example:
```cpp
int i=1;
while (i<=n)
{
    i=i*2;
}
```
To analyze the iteration times 'x', we can find that $2^x=n$, so that $x=\log_{2}{n}$, which also is the time complexity $O(\log{n})$.

### $O(n\log{n})$ Linear Logarithmic time 

If we add an outer phase of for() out of the $\log{n}$, we will get $O(n\log{n})$.

```cpp
for(int j=1;j<=n;j++)
{
    int i=1;
    while(i<=n)
    {
        i=i*2;
    }
}
```
We can find that the time complexity of nested code will be the multiplication of inner and outer.

## Space Complexity
>The space complexity of an algorithm or a computer program is the amount of memory space required to solve an instance of the computational problem as a function of characteristics of the input. It is the memory required by an algorithm until it executes completely.[<sup>2</sup>](#refer-anchor).
> The big O notation can also be used to describe the space complexity.

### $O(n)$ Linear time 

```cpp
int a=0;
int array[] =new int [n];
for (int i=0;i<n;i++)
{
    array[i]=n;
}
```
We can simply summarize:
- For limit (constant) variables, $O(n)$
- For linear array, $O(n)$
- For second order array, $O(n^2)$


<div id="refer-anchor"></div>

## Reference 
[1] Time complexity,https://en.wikipedia.org/wiki/Time_complexity

