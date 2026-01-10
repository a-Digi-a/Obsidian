#programming #python #semester-1 
# Booleans

Booleans are values that are either **True** or **False**:
```python
x = True
y = False
```

When you run a condition statement python returns a Boolean:
```python
print(10 > 9) # True
print(10 == 9) # False
print(10 < 9) # False
```

The **bool**() function evaluates the value and returns a Boolean:
```python
print(bool("Hello")) # True
print(bool(15)) # True
```

Most values are **True**, unless it has some sort of content:

Any string is **True**, except **empty** **strings**
Any number is **True**, except for **0**
Any list, tuple, set and dictionaries are **True**, except for **empty ones**

The value **None** is **False**
