 #programming #python #semester-1 
 
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
