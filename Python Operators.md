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
| **not**      | ***Reverses** the result*                            |

# Identity Operators

