 #programming #python #semester-1 
 
# Tuples

**Tuples**, similar to **lists**, are used to store **multiple** **items** in a single variable.
They are **ordered**, **unchangeable**, and **allow duplicate values**. 

## Declaring a Tuple

A **tuple** can be **declared** using **regular brackets**: *()*
```python
a_tuple = ("apple", "bannana", "cherry")
```

To **declare** a **tuple** with **one item**, use a comma after the item:

```python
a_tuple = ("apple",) # Notice the Comma
```

## Tuples with Multiple Data Types

**Tuples** can have **multiple data types** in them:
```python
a_tuple = ("apples", 1, True, 3.0)
```

## Accessing the Items in a Tuple

**Tuple** items can be accessed with the following syntax: **tuple**[i]
```python
a_tuple = ["apple", "bannana", "cherry"]

x = a_tuple[0] # "apple"
y = a_tuple[1] # "bannana"
z = a_tuple[2] # "cherry"
```
Note how the **index** starts at *0*, not *1*

### Negative Indexing

We can also use a **negative index** to access items from the end of the **tuple**, with *-1* being the last item, *-2* being the second last, etc.
```python
a_tuple = ["apples", 1, True]
print(a_tuple[-1]) # True
print(a_tuple[-2]) # 1
```

### Range of Indexes

We can specify a **range** of indexes:
```python
a_tuple = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(a_tuple[2:5]) 
# from index 2 (inclusive) to index 5 (exclusive) - > [3, 4, 5]

print(a_tuple[:5])
# from the start to index 5 (exclusive) -> [1, 2, 3, 4, 5]

print(a_tuple[5:])
# from index 5 (inclusive) to the end of the list -> [6, 7, 8, 9, 10]

print(a_tuple[-4:-1])
# from 4th last item (inclusive) to the last item (exclusive) -> [7, 8, 9]
```
## Changing the Items in a Tuple

**Tuples** are **immutable**, meaning they **cannot** be changed.

If you want to **change** the items in a **tuple**, you can change it into a **list**, then back into a **tuple**
```python
a_tuple = ("apple", "bannana", "cherry")
b_list = list(a_tuple)
b_list[1] = "pear"
a_tuple = tuple(b_list)
print(a_tuple) # ["apple", "pear", "cherry"]
```


## Adding Items to the Tuple

You can **add tuples to tuples**
```python
a_tuple = ("apple", "banana", "cherry")
b_tuple = ("pear")
a_tuple += b_tuple

print(a_tuple) # ("apple", "banana, "cherry", "pear")
```

## Removing Tuple Items

You **cannot remove** items from a **tuple**, unless it is converted to a **list** first

## Unpacking a Tuple

When you **create a tuple**, you normally **assign values** to it. This is called **packing** a **tuple**

We can then **unpack** the **items** **back into variables**:
```python
a_tuple = ("apple", "banana", "cherry")
(a, b, c) = a_tuple

print(a) # "apple"
print(b) # "banana"
print(c) # "cherry"
```

### Using Asterisk \*

We can also use an **asterisk** *\** in order to unpack the remainder of a **tuple** into a variable as a **list**

```python
a_tuple = ("apple", "banana", "cherry", "pear", "blueberry")
(a, b, c*) = a_tuple

print(a) # "apple"
print(b) # "banana"
print(c) # ["cherry", "pear", "blueberry"]
```
 
## Looping Through a Tuple

### Looping Through Items

You can **loop** through the **items** in a **tuple** by using a **for loop**:
```python
a_tuple = ("apple", "banana", "cherry")
for x in a_tuple:
	print(x)
	
# "apple"
# "banana"
# "cherry"
```

### Looping Through the Index

We can **loop** through the **index** of the **list** too:
```python
a_tuple= ("apple", "banana", "cherry")
for i in range(len(a_tuple)):
	print(a_tuple[i])
```

## Checking if an Item is in a Tuple

You can use the **in** keyword to check if an item is in a **list**:
```python
a_tuple= ("apple", "orange", "cherry")
if "apple" in a_tuple:
	print("blah blah blah")
```

## Joining Tuples

We can **join** two **tuples**:
```python
a_tuple = ("apple", "orange", "cherry")
b_tuple = ("pear", "blueberry", "strawberry")

c_tuple = a_tuple + b_tuple
print(c_tuple) # ("apple", "orange", "cherry", "pear", "blueberry", "strawberry")
```

## Multiply Tuples

We can also **multiply the contents of a tuple**:
```python
a_tuple = ("apple", "orange", "cherry")
b_tuple = a_tuple \* 2

print(b_tuple) # ("apple", "orange", "cherry", "apple", "orange", "cherry")
```


## All Tuple Methods

| **Method**  | **Description**                                                                           |
| ----------- | ----------------------------------------------------------------------------------------- |
| **count()** | *Returns the number of times a specified value occurs in a tuple*                         |
| **index()** | *Searches the tuple for a specified value and returns the position of where it was found* |
