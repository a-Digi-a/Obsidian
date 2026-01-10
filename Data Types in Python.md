 #programming #python #semester-1 

# [[Python Integers|Integers]]
# [[Python Floats|Floats]]
# [[Python Complex Numbers|Complex]]
# [[Python Strings|Strings]]
# [[Python Booleans|Booleans]]
# [[Python Lists|Lists]]
# [[Python Booleans|Booleans]]
# [[Python Booleans|Booleans]]
# [[Python Booleans|Booleans]]

# Lists

**Lists** are used to store **multiple** **items** in one variable. They are **ordered**, the values and length **can** be changed and allow **duplicate** values. The **items** in a list can be **different** data types.

## Declaring a List

A **list** can be **declared** using **square brackets**: *[]*
```python
a_list = ["apple", "bannana", "cherry"]
```

## Lists with Multiple Data Types

**Lists** can have **multiple data types** in them:
```python
a_list = ["apples", 1, True, 3.0]
```

## Accessing the Items in a List

**List** items can be accessed with the following syntax: **list**[i]
```python
a_list = ["apple", "bannana", "cherry"]

x = a_list[0] # "apple"
y = a_list[1] # "bannana"
z = a_list[2] # "cherry"
```
Note how the **index** starts at *0*, not *1*

### Negative Indexing

We can also use a **negative index** to access items from the end of the **list**, with *-1* being the last item, *-2* being the second last, etc.
```python
a_list = ["apples", 1, True]
print(a_list[-1]) # True
print(a_list[-2]) # 1
```

### Range of Indexes

We can specify a **range** of indexes:
```python
a_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(a_list[2:5]) 
# from index 2 (inclusive) to index 5 (exclusive) - > [3, 4, 5]

print(a_list[:5])
# from the start to index 5 (exclusive) -> [1, 2, 3, 4, 5]

print(a_list[5:])
# from index 5 (inclusive) to the end of the list -> [6, 7, 8, 9, 10]

print(a_list[-4:-1])
# from 4th last item (inclusive) to the last item (exclusive) -> [7, 8, 9]
```
## Changing the Items in a List

You can **change** the items in a **list** by accessing them:
```python
a_list = ["apple", "bannana", "cherry"]

a_list[1] = "pear"
print(a_list) # ["apple", "pear", "cherry"]
```

You can also **change** **multiple** **items**:
```python
a_list = [1, 2, 3, 4]
a_list[1:3] = ["apple", "orange"]
print(a_list) # [1, "apple", "orange", 4]
```

## Adding Items to the List

### insert()

You can **add** items to the **list** by calling the **insert**() method:
```python
a_list = [1, 2, 4]
a_list.insert(2, 3) # insert(index, item)
print(a_list) # [1, 2, 3, 4]
```

### append()

You can **append** an item to the end of the list with the **append()** method:
```python
a_list = [1, 2, 3]
a_list.append(4)
print(a_list) # [1, 2, 3, 4]
```

### extend()

You can also **append** items from other **lists** using **extend**:
```python
a_list = [1, 2, 3]
b_list = [4, 5, 6]
a_list.extend(b_list)
print(a_list) # [1, 2, 3, 4, 5, 6]
```
This works with **any iterable object** such as **strings**, **tuples**, **dictionaries**, **sets**, **arrays**, etc.
## Removing List Items

### remove()

To **remove** a **specified item** we can call the **remove()** method:
```python
a_list = ["apple", "banana", "orange"]
a_list.remove("banana")
print(a_list) # ["apple", "orange"]
```

If there are **multiple instances** of the item in the **list**, the **remove()** method removes the **first** instance:
```python
a_list = ["apple", "banana", "apple"]
a_list.remove("apple")
print(a_list) # ["banana", "apple"]
```

### pop()

You can use the **pop()** method to remove the specified **index**:
```python
a_list = [1, 2, 3, 4, 5]
a_list.pop(2)
print(a_list) # [1, 2, 4, 5]
```
If you do not specify the **index**, **pop()** removes the **last item**:
```python
a_list = [1, 2, 3, 4, 5]
a_list.pop()
print(a_list) # [1, 2, 3, 4]
```

### clear()

The **clear()** method **empties** the **list**:
```python
a_list = [1, 2, 3, 4, 5]
a_list.clear()
print(a_list) # []
```

## Looping Through a List

### Looping Through Items

You can **loop** through the **items** in a **list** by using a **for loop**:
```python
a_list = ["apple", "banana", "cherry"]
for x in a_list:
	print(x)
	
# apple
# banana
# cherry
```

### Looping Through the Index

We can **loop** through the **index** of the **list** too:
```python
a_list = ["apple", "banana", "cherry"]
for i in range(len(a_list)):
	print(a_list[i])
```

## Checking if an Item is in a List

You can use the **in** keyword to check if an item is in a **list**:
```python
a_list = ["apple", "orange", "cherry"]
if "apple" in a_list:
	print("blah blah blah")
```

## Sorting Lists

You can **sort lists** by using the **sort()** method:
```python
# alphabetically
a_list = ["orange", "mango", "kiwi", "pineapple", "banana"]
a_list.sort()
print(a_list) # ['banana', 'kiwi', 'mango', 'orange', 'pineapple'] 

# numerically
b_list = [3, 4, 2, 1, 5]
b_list.sort()
print(b_list) # [1, 2, 3, 4, 5]
```

### Descending Sort

You can also **reverse** the order of the sort:
```python
# alphabetically
a_list = ["orange", "mango", "kiwi", "pineapple", "banana"]
a_list.sort(reverse = True)
print(a_list) # ['pineapple', 'orange', 'mango', 'kiwi', 'banana'] 

# numerically
b_list = [3, 4, 2, 1, 5]
b_list.sort(reverse = True)
print(b_list) # [5, 4, 3, 2, 1]
```

### Customize Sort Function

You can also customize your own sort function using the **keyword** argument *key = function*
The function returns a number that will be used to sort that list
```python
def function(n):
	return abs(n)
	
a_list = [100, 35, 55, -23, -1, 0]
a_list.sort(key = function)
print(a_list) # [0, -1, -23, 35, 55, 100]
```
You can also use **built in functions** to sort a list, such as *key = str.lower* to do a case insensitive sort

### Reversing the Order of a List

To **reverse the order** of a **list** you can use the **reverse()** method:
```python
a_list = ["apple", "orange", "banana"]
a_list.reverse()
print(a_list) # ["banana", "orange", "apple"]
```

## Copying Lists

We cannot **copy** a **list** using *list1 = list2*, as that will create a **reference** to the original list.
To **copy** a **list**, we can use either use the **copy()** method, **list()** function, or **slice operator**: *:*
```python
a_list = [1, 2, 3]
copy1 = a_list.copy()
copy2 = list(a_list)
copy3 = a_list[:]
```

## All List Methods

| **Method**    | **Description**                                                                |
| ------------- | ------------------------------------------------------------------------------ |
| **append()**  | *Adds an element at the end of the list*                                       |
| **clear()**   | *Removes all the elements from the list*                                       |
| **copy()**    | *Returns a copy of the list*                                                   |
| **count()**   | *Returns the number of elements with the specified value*                      |
| **extend()**  | *Add the elements of a list (or any iterable), to the end of the current list* |
| **index()**   | *Returns the index of the first element with the specified value*              |
| **insert()**  | *Adds an element at the specified position*                                    |
| **pop()**     | *Removes the element at the specified position*                                |
| **remove()**  | *Removes the item with the specified value*                                    |
| **reverse()** | *Reverses the order of the list*                                               |
| **sort()**    | *Sorts the list*                                                               |

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



# Dictionaries
 