 #programming #python #semester-1 
 
# Arithmetic Operators

| **Operator** | **Name**                      |
| ------------ | ----------------------------- |
| **+**        | *Addition*                    |
| **-**        | *Subtraction*                 |
| **\***       | *Multiplication*              |
| **/**        | *Division*                    |
| **%**        | *Modulus (Remainder)*         |
| **\*\***     | *Exponentiation (Power)*      |
| **//**       | *Floor Division (Round Down)* |

# Assignment Operators

**Assigns** the value on the right onto the value on the left

| **Operator** | **Example**     | **Same As**         |
| ------------ | --------------- | ------------------- |
| **=**        | *x = 5*         | *x = 5*             |
| **+=**       | *x +=3*         | *x = x + 3*         |
| **-=**       | *x -= 3*        | *x = x -3*          |
| **\*=**      | *x \*= 3*       | *x = x \* 3*        |
| **/=**       | *x /=3*         | *x = x / 3*         |
| **%=**       | *x %= 3*        | *x = x % 3*         |
| **//=**      | *x //= 3*       | *x = x // 3*        |
| **=**        | *x \*\*= 3*     | *x = x \*\* 3*      |
| **&=**       | *x &= 3*        | *x = x & 3*         |
| **\|=**      | *x \|= 3*       | *x = x \| 3*        |
| **^=**       | *x ^= 3*        | *x = x ^ 3*         |
| **>>=**      | *x >>= 3*       | *x = x >> 3*        |
| **<<=**      | *x <<= 3*       | *x = x << 3*        |
| **:=**       | *print(x := 3)* | *x = 3<br>print(x)* |

# The Walrus Operator

The **walrus operator** returns and assigns a value to a certain variable.
You can use it as an inline assignment shown here:
```python
x = some_variable
if x > 10 and x < 50:
	print("blah blah blah")
```
```python
if (x := some_variable) > 10 and < 50:
	print("blah blah blah")
```
Both of these code snippets are the same.


# Comparison Operators

**Comparison Operators** return **True** or **False**:

| **Operator** | **Name**                   |
| ------------ | -------------------------- |
| **==**       | *Equal To*                 |
| **!=**       | *Not Equal To*             |
| **>**        | *Greater Than*             |
| **<**        | *Less Than*                |
| **>=**       | *Greater Than or Equal To* |
| **<=**       | *Less Than or Equal To*    |

# Logical Operators

**Logical** **operators** are used to **combine** conditional statements:

| **Operator** | **Description**                                      |
| ------------ | ---------------------------------------------------- |
| **and**      | *Returns True if **both** statements are True*       |
| **or**       | *Returns True if **one** of the statements are true* |
| **not**      | * **Reverses** the result*                           |

# Identity Operators

**Identity Operators** are used to compare objects, not if they are equal but if they are the **same object** with the **same memory location**.

| *Operator* | *Description*                                                         |
| ---------- | --------------------------------------------------------------------- |
| *is*       | *Returns **True** if both variables are the **same object** *         |
| *is not*   | *Returns **True** if both variables are **not** the **same object** * |
```python
x = ["apple", "banana"]
y = ["apple", "banana"]
z = x

print(x is z) # True
print(x is y) # False
print(x == y) # True
```

# Membership Operators

**Membership operators** are used to test if a **sequence** is presented **in an object**

| **Operator** | **Description**                                                                                 |
| ------------ | ----------------------------------------------------------------------------------------------- |
| **in**       | *Returns **True** if a sequence with the specified value **is** present in the **object** *     |
| **not in**   | *Returns **True** if a sequence with the specified value is **not** present in the **object** * |
```python
fruits = ["apple", "banana", "cherry"]

print("banana" in fruits) # True

text = "Hello World"

print("H" in text) # True
print("hello" in text) # False
print("z" not in text) # True
```

# Bitwise Operators


| **Operator** | **Name**                 | **Description**                                                                                                                 |
| ------------ | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| **&**        | **AND**                  | *Sets each bit to 1 if **both** bits are 1*                                                                                     |
| **\|**       | **OR**                   | *Sets each bit to 1 if **one** of two bits is 1*                                                                                |
| **^**        | **XOR**                  | *Sets each bit to 1 if **only one** of two bits is 1*                                                                           |
| **~**        | **NOT**                  | * **Inverts** all the bits*                                                                                                     |
| **<<**       | **Zero fill left shift** | *Shift left by **pushing** **zeros** **in** from the **right** and let the leftmost bits fall off (e.g. x << 2)*                |
| **>>**       | **Signed right shift**   | *Shift right by **pushing copies of the leftmost bit** in from the **left**, and let the rightmost bits fall off (e.g. x >> 2)* |
## Example

The binary representation of **6** is *0110*
The binary representation of **3** is *0011*
6 & 3 = *0010* = **2** in decimal
## The bin() Function
The **bin**() function can be used to see the **binary** **form** of an **integer** prefixed with *0b*:
```python
x = 6
print(bin(x)) # 0b110 -> String
```