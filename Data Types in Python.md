 #programming #python #semester-1 

# Numbers

## Integers

Integers are **whole numbers**, and can be both positive or negative.
```python
x = 1
y = 734566222155
z = -23425565
```

You can cast to an integer using:
```python
x = int(x)
```
## Floats

Floats are numbers which **contain decimals**, and can be positive or negative
```python
x = 1.10
y = 1.0
z = -73.24
```

Floats can also contain scientific numbers, *e* for example means to the power of 10:
```python
x = 53e3
y = 12E4
z = -87.7e100
```

You can cast to a float using:
```python
x = float(x)
```

## Complex

Complex numbers are written with a *j* as the imaginary part:
```python
x = 3+5j
y = 5j
z = -5j
```

You can cast to a complex using:
```python
x = complex(x)
```

# Strings

**Strings** in python are surrounded by either **single** *or* **double** quotes:
```python
x = "hi"
y = 'hello'
```


Strings are **arrays**, therefore you can access the characters in a string using:
```python
string = "a string"
x = string[0] # "a"
y = string[1] # " "
z = string[2] # "s"
```

You can use the len() function to get the length of a string:
```python
x = "string"
print(len(string)) # 6
```

## String Slicing

We can return a range of characters from a string:
```python
string = "Hello World!"
print(x[2:5]) # Characters from the position to position 5 -> "llo"
print(x[:5]) # Characters from the start to position 5 -> "Hello"
print(x[2:]) # Characters from position 2 to the end -> "llo World!"
print(x[-5:-2]) # Characters from the end -5 to the end -2 -> "orl"
```

## String Methods

The upper() method returns the string in upper case:
```python
string = "Hello World!"
print(string.upper()) # "HELLO WORLD!"
```

The lower() method returns the string in lower case:
```python
string = "Hello World!"
print(string.lower()) # "hello world!"
```

The strip() method removes the whitespace around the string:
```python
string = " Hello World! "
print(string.strip()) # "Hello World!"
```

The replace() method replaces the characters in a string:
```python
string = "Hello World!"
print(string.replace("H", "J")) # "Jello World!"
```

The split() method splits the string if it finds the seperator:
```python
string = "Hello, World!"
print(string.split(",")) # ['Hello', ' World']
```

## String Concatenation

To **concatenate** (combine) 2 strings you can add them together:
```python
a = "Hello"
b = "World"
c = a + b # H
```