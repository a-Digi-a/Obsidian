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

Here is a list of all string methods:

| Method                                                                         | Description                                                                                   |
| ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **capitalize**()                                                               | Converts the first character to upper case                                                    |
| **casefold**()                                                                 | Converts string into lower case                                                               |
| **center**()                                                                   | Returns a centered string                                                                     |
| [count()](https://www.w3schools.com/python/ref_string_count.asp)               | Returns the number of times a specified value occurs in a string                              |
| [encode()](https://www.w3schools.com/python/ref_string_encode.asp)             | Returns an encoded version of the string                                                      |
| [endswith()](https://www.w3schools.com/python/ref_string_endswith.asp)         | Returns true if the string ends with the specified value                                      |
| [expandtabs()](https://www.w3schools.com/python/ref_string_expandtabs.asp)     | Sets the tab size of the string                                                               |
| [find()](https://www.w3schools.com/python/ref_string_find.asp)                 | Searches the string for a specified value and returns the position of where it was found      |
| [format()](https://www.w3schools.com/python/ref_string_format.asp)             | Formats specified values in a string                                                          |
| format_map()                                                                   | Formats specified values in a string                                                          |
| [index()](https://www.w3schools.com/python/ref_string_index.asp)               | Searches the string for a specified value and returns the position of where it was found      |
| [isalnum()](https://www.w3schools.com/python/ref_string_isalnum.asp)           | Returns True if all characters in the string are alphanumeric                                 |
| [isalpha()](https://www.w3schools.com/python/ref_string_isalpha.asp)           | Returns True if all characters in the string are in the alphabet                              |
| [isascii()](https://www.w3schools.com/python/ref_string_isascii.asp)           | Returns True if all characters in the string are ascii characters                             |
| [isdecimal()](https://www.w3schools.com/python/ref_string_isdecimal.asp)       | Returns True if all characters in the string are decimals                                     |
| [isdigit()](https://www.w3schools.com/python/ref_string_isdigit.asp)           | Returns True if all characters in the string are digits                                       |
| [isidentifier()](https://www.w3schools.com/python/ref_string_isidentifier.asp) | Returns True if the string is an identifier                                                   |
| [islower()](https://www.w3schools.com/python/ref_string_islower.asp)           | Returns True if all characters in the string are lower case                                   |
| [isnumeric()](https://www.w3schools.com/python/ref_string_isnumeric.asp)       | Returns True if all characters in the string are numeric                                      |
| [isprintable()](https://www.w3schools.com/python/ref_string_isprintable.asp)   | Returns True if all characters in the string are printable                                    |
| [isspace()](https://www.w3schools.com/python/ref_string_isspace.asp)           | Returns True if all characters in the string are whitespaces                                  |
| [istitle()](https://www.w3schools.com/python/ref_string_istitle.asp)           | Returns True if the string follows the rules of a title                                       |
| [isupper()](https://www.w3schools.com/python/ref_string_isupper.asp)           | Returns True if all characters in the string are upper case                                   |
| [join()](https://www.w3schools.com/python/ref_string_join.asp)                 | Joins the elements of an iterable to the end of the string                                    |
| [ljust()](https://www.w3schools.com/python/ref_string_ljust.asp)               | Returns a left justified version of the string                                                |
| [lower()](https://www.w3schools.com/python/ref_string_lower.asp)               | Converts a string into lower case                                                             |
| [lstrip()](https://www.w3schools.com/python/ref_string_lstrip.asp)             | Returns a left trim version of the string                                                     |
| [maketrans()](https://www.w3schools.com/python/ref_string_maketrans.asp)       | Returns a translation table to be used in translations                                        |
| [partition()](https://www.w3schools.com/python/ref_string_partition.asp)       | Returns a tuple where the string is parted into three parts                                   |
| [replace()](https://www.w3schools.com/python/ref_string_replace.asp)           | Returns a string where a specified value is replaced with a specified value                   |
| [rfind()](https://www.w3schools.com/python/ref_string_rfind.asp)               | Searches the string for a specified value and returns the last position of where it was found |
| [rindex()](https://www.w3schools.com/python/ref_string_rindex.asp)             | Searches the string for a specified value and returns the last position of where it was found |
| [rjust()](https://www.w3schools.com/python/ref_string_rjust.asp)               | Returns a right justified version of the string                                               |
| [rpartition()](https://www.w3schools.com/python/ref_string_rpartition.asp)     | Returns a tuple where the string is parted into three parts                                   |
| [rsplit()](https://www.w3schools.com/python/ref_string_rsplit.asp)             | Splits the string at the specified separator, and returns a list                              |
| [rstrip()](https://www.w3schools.com/python/ref_string_rstrip.asp)             | Returns a right trim version of the string                                                    |
| [split()](https://www.w3schools.com/python/ref_string_split.asp)               | Splits the string at the specified separator, and returns a list                              |
| [splitlines()](https://www.w3schools.com/python/ref_string_splitlines.asp)     | Splits the string at line breaks and returns a list                                           |
| [startswith()](https://www.w3schools.com/python/ref_string_startswith.asp)     | Returns true if the string starts with the specified value                                    |
| [strip()](https://www.w3schools.com/python/ref_string_strip.asp)               | Returns a trimmed version of the string                                                       |
| [swapcase()](https://www.w3schools.com/python/ref_string_swapcase.asp)         | Swaps cases, lower case becomes upper case and vice versa                                     |
| [title()](https://www.w3schools.com/python/ref_string_title.asp)               | Converts the first character of each word to upper case                                       |
| [translate()](https://www.w3schools.com/python/ref_string_translate.asp)       | Returns a translated string                                                                   |
| [upper()](https://www.w3schools.com/python/ref_string_upper.asp)               | Converts a string into upper case                                                             |
| [zfill()](https://www.w3schools.com/python/ref_string_zfill.asp)               | Fills the string with a specified number of 0 values at the beginning                         |
## String Concatenation

To **concatenate** (combine) 2 strings you can add them together:
```python
a = "Hello"
b = "World"
c = a + b # HelloWorld
d = a + ' ' + b # Hello World
```

## F Strings

Formatting strings allow you to add curly brackets as a placeholder for variables and other operations:
```python
name = "Jim"
x = f"My name is {Jim}"
```
A placeholder can contain variables, operations and functions.

A placeholder can have a **modifier** to format the value:
```python
price = 59
txt = f"The price is {price:2f} euro"
print(txt) # "The price is 59.00 euro"
```

## Escape Characters
