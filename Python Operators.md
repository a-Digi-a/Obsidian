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

**Identity Operators** are used to compare objects, not if they are equal but if they are the same object with the same memory location.

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

