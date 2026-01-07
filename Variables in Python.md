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

## All Casting 

# More Ways of Assigning Values
## Assigning Multiple Values at Once

We can assign multiple values at once by:
```python
x, y, z = 1, "meow", 5.0
print(x) # prints 1
print(y) # prints meow
print(z) # prints 5.0
```

## Assigning One Value to Multiple Variables

We can assign one value to multiple variables by:
```python
x = y = z = 1
print(x) # prints 1
print(y) # prints 1
print(z) # prints 1
```
# Local Variables

Variables created inside of a [[scope]]/[[Functions in Python|function]] are **local** by default. This means that they are only valid **inside** that scope or function. For example:
```python
def function():
	x = 1 
	print(x) #prints x 
	# scope ends, x is no longer valid
	
function()
	
print(x) # program will have an error as x does not exist
```
# Global Variables

Variables created outside of a [[scope]]/[[Functions in Python|function]] are **global**. This means that they can be used anywhere in the program, inside or outside of functions.

for example:
```python
x = 5

def function():
	y = x + 1 # y is 6
	print(y) # prints 6
	print(x) # prints 5
	
function()
```

However, when we change the value of a global variable inside of a function, it is **not** changed outside of the function:
```python
x = 3

def function():
	x = x + 1 # x is now 4
	print(x) # prints 4
	# scope ends
	
function()

print(x) # prints 3
```

To change the **global value** of x we can use the *global* keyword:

```python
x = 3

def function():
	global x
	
	x = x + 1 # x is now 4
	print(x) # prints 4
	# scope ends
	
function()

print(x) # prints 4
```