 #programming #python #semester-1 

# Declaring a Variable

We declare a variable using the following syntax:
```python
x = 5 # x is assigned the value 5 
y = "meow" # y is assigned the value meow
```
The variable on the left hand side of the equals sign will have the value on the right hand sign **assigned** to it.

We can also overwrite variable values:
```python
x = 5
x = "meow"
# This is valid code
```

# Casting

Casting is when we specify data type of a variable. This can be done with the following syntax:
```python
x = str(3) # x will be '3'
y = int(3) # y will be 3
z = float(3) # z will be 3.0
```
This functionality is not very useful as python **implicitly** guesses the type of variables, however it has **another** use:

Casting can be used to **change** the data type of a variable:
```python
x = '3' # x is a string that says 3
x = int(x) # x is now the integer 3, we can now to maths with it, etc.
```
This is very useful, especially when it comes to getting user input and using it!

# More co