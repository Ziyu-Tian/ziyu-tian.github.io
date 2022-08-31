# Bit Operation in C

## 1: Fundamental Basic

- Used to operate the intrigue variable (int,char,long,etc.) in binary bits. 

- C/C++ provide six **bit operators**:
    - '&': bitwise AND (binary)
    - '|': bitwise OR (binary)
    - '^': bitwise EXCLUSIVE (binary)
    - '~': bitwise NOT (unary)
    - '<<': Left move (binary)
    - '>>': Right move (binary)

## 2: Bitwise AND '&' 

- For example, the result of "21 & 18" is 16 (10000 in binary).

- '21' is '0000 0000 0000 0000 0000 0000 0001 0101'.

- '18' is '0000 0000 0000 0000 0000 0000 0001 0010'.

- So the result is '0000 0000 0000 0000 0000 0000 0001 0000'.

- Application :
    - The '&' can be used to set some bits to 0 and keep others origin.
    - For example, it we need to set the lower 8 bits of 'int n' to 0 and keep others unchanged, then we can execute 'n=n & 0xffffff00' or 'n &= 0xffffff00'
    - '0x' means hexadecimal number, 'f' means the '1111' in binary.
    - So the six 'f' means the upper 24 digits of int and '00' (0000 0000 in binary) means the lower 8 digits. The '00' will set the lower 8 digits into '0', while others keep unchanged.
    - For the 'short' type, order will be 'n &= 0xff00'.

## 3: Bitwise OR '|'

- Following the example above, "21 | 18 =23". 

- Application :
    - '|' can be used to set some bits '1' and keep others unchanged.
    - If we want to set the lower 8 bits of 'int n' to '1' and keep other bits, the order 'n |= 0xff' can be used.

## 4: Bitwise EXCLUSIVE-OR '^'

- For example, '21^18=111'.

- Application:
    - '^' used to set some bits inversely and keep others unchanged.
    - If we want to invert the lower 8 digits of 'int n' and keep others unchanged, the order will be 'n^=0xff'.
    - The '^' can be used as simple encode and decode.
    - The '^' can also be used to exchange two numbers without the temp variable:

```cpp
int x=11; // binary '1011'
int y=7; // '0111'
x=x^y;
        // x=1011^0111=1100.
        // Note that in the EX-OR operation, the 'same part' will be set as '0', only if one is '0' and another is '1', the result will be '1'.
        // If we 'EX-OR' the 'different-part', that digit will be exchange to other's digit.
        //If we 'EX-OR' the 'same-part', the result will keep unchanged.
y=x^y;
        // y=1100^0111=1011, we can find the 'y' has already exchanged to 'x'

x=x^y; 
        //x=1100^1011=0111, then the 'x' has been exchanged

```

## 5: Bitwise NOT '~'

- For example, '~21=0xffffffea'.

## 6: Bitwise LEFT-SHIFT '<<'

- The 'a << b' is used to left-shift 'b' bits of binary a, the left-bit will be discorded and right-bit will be set as '0'.
- For example, '9 << 4'.
- Binary '9' is '0000 0000 0000 0000 0000 0000 0000 1001', the result will be '0000 0000 0000 0000 0000 0000 1001 0000'
- In fact, left-shift 1 bit is same as multiply it by 2. Left-shift n bits is multiplying $2^n$.
  
## 7: Bitwise RIGHT-SHIFT '>>'

- RIGHT-SHIFT is right-moving the binary bits.
- For the signed number, such as 'long,int,short,char', the sign digit (highest digit) will move at the same time.
- If the origin sign digit is '1', then the '1' will be added after moving; if it is '0', then the '0' will be added.
- The actual result of right-shifting n bits is equal to the eft number divide $2^n$.