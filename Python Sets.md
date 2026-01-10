 #programming #python #semester-1 

# Sets

**Sets** are used to store multiple items in a **single variable**.  **Sets** are **unordered**, **unchangeable**, and **unindexed**. 

## Declaring a Set

To declare a **set** we use **curly brackets**: *{}*
```python
a_set = {"apple", "banana", "orange"}

print(a_set)
```

### Unordered
**Sets** are **unordered**, meaning they can appear in a different order every time you use them, and **cannot** be referred to by index or key.

### Unchangeable

**Set items cannot be changed**, however you **can** **add** or **remove** **items**

### Duplicates Not Allowed

**Sets** **cannot** have **duplicate items**, and any duplicates will be **ignored**:
```python
a_set = {"apple", "banana", "cherry", "apple"}

print(a_set) # 'banana', 'cherry', 'apple'
```

**NOTE**:
**True** and **1** are considered the **same value**
**False** and **0** are considered the **same value**
```python
a_set = {"apple", "banana", True, 1}
b_set = {"orange", "cherry", 0, False}

print(a_set) # True, 'apple', 'banana'
print(b_set) # 0, 'cherry', 'orange'
```

Notice how the **leftmost value** will be the one printed

## Set Data Types

The **items** in a **set** can be of **any data type**

## Get the Length of a Set
We can get the **length** of a **set** with the **len()** function:
```python
a_set = {"apple", "banana", "cherry"}

print(len(a_set)) # 3
```

## Accessing Set Items

The **items** in a **set** **cannot** be accessed by referring to an **index** or **key**. Instead, we can:

### Loop Over the Set
```python
a_set = {"apple", "banana", "cherry"}

for i in a_set:
	print(i)
```

## Use the in Keyword
```python
a_set = {"apple", "banana", "cherry"}

print("apple" in a_set) # True
```

## Use the not in Keyword
```python
a_set = {"apple", "banana", "cherry"}

print("apple" not in a_set) # False
```

## Adding Set Items

###  add() Method
You can **add set items** with the **add()** method:
```python
a_set = {"apple", "banana", "cherry"}

a_set.add("orange")

print(a_set) # 'apple', 'banana', 'cherry', 'orange'
```

### update() Method
You can **add 2 sets** using the **update()** method:
```python
a_set = {"apple", "banana", "cherry"}
b_set = {"pear", "orange"}

a_set.update(b_set)
print(a_set) # 'apple', 'banana', 'cherry', 'pear', 'orange'
```

You can also use **update()** to **add any other iterable**:
```python
a_set = {"apple", "banana", "cherry"}
a_list = ["pear", "orange"]
a_string = "hi"

a_set.update(a_list)
a_set.update(a_string)

print(a_set) # 'apple', 'banana', 'cherry', 'pear', 'orange', 'h', 'i'
```

## Removing Set Items

### remove() Method

You can **remove items** by using the **remove()** method
If the item is **not in** the **set**, it will return an **error**:
```python
a_set = {"apple", "banana", "orange"}

a_set.remove("orange")

print(a_set) # 'apple', 'banana'
```

### discard() Method

You can **remove items** by using the **discard()** method 
If the item is **not in** the **set**, it will **not** return an **error**:
```python
a_set = {"apple", "banana", "orange"}

a_set.discard("orange")

print(a_set) # 'apple', 'banana'
```

### pop() Method 

You can also use the **pop()** method to **remove an item**, however as **sets** are **unordered**, it will **remove a random item**:
```python
a_set = {"apple", "banana", "orange"}

a_set.pop()

print(a_set) # 'apple', 'orange'
```

### clear() Method

You can use the **clear()** method to **empty a set**:
```python
a_set = {"apple", "banana", "orange"}

a_set.clear()

print(a_set) # {}
```

## Join Sets

There are several methods used to **join** two **sets**:

| **Method**                 | **Description**                                                 |
| -------------------------- | --------------------------------------------------------------- |
| **update()**               | *Joins all of the items from both sets*                         |
| **union()**                | *Joins all of the items from both sets*                         |
| **intersection()**         | *Keeps only the items in both sets*                             |
| **difference()**           | *Keeps items from the first set that are not in the other sets* |
| **symmetric_difference()** | *Keeps all items except the duplicates*                         |


### Union

The **union()** method returns a **set** with the **items from both sets**
```python
a_set = {"a", "b", "c"}
b_set = {1, 2, 3}

c_set = a_set.union(b_set)
print(c_set) # 'a', 'b', 'c', 1, 2, 3
```

You can also use the **|** operator instead of **union()**
```python
a_set = {"a", "b", "c"}
b_set = {1, 2, 3}

c_set = a_set | b_set
print(c_set) # 'a', 'b', 'c', 1, 2, 3
```

You can use **union** to **join sets with non sets**. This will not work with **update** *or* the **| operator** .
```python
a_set = {1, 2, 3}
a_tuple = (4, 5, 6)

c_set = a_set.union(a_tuple)
```
### Update
### Intersection

### Difference

### Symmetric Difference

### Using the Set Methods on Multiple Sets

You can use the **set methods** on **multiple sets** with the following syntax:
```python
a_set = {'a', 'b', 'c'}
b_set = {1, 2, 3}
c_set = {2.3, 4.6}

d_set = a_set.union(b_set, c_set)
```

OR

```python
a_set = {'a', 'b', 'c'}
b_set = {1, 2, 3}
c_set = {2.3, 4.6}

d_set = a_set | b_set | c_set
```

