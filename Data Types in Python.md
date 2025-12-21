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

You can use the **len**() function to get the length of a string:
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

The **upper**() method returns the string in upper case:
```python
string = "Hello World!"
print(string.upper()) # "HELLO WORLD!"
```

The **lower**() method returns the string in lower case:
```python
string = "Hello World!"
print(string.lower()) # "hello world!"
```

The **strip**() method removes the whitespace around the string:
```python
string = " Hello World! "
print(string.strip()) # "Hello World!"
```

The **replace**() method replaces the characters in a string:
```python
string = "Hello World!"
print(string.replace("H", "J")) # "Jello World!"
```

The **split**() method splits the string if it finds the seperator:
```python
string = "Hello, World!"
print(string.split(",")) # ['Hello', ' World']
```

### All String Methods

Here is a list of all string methods:

| **Method**         | **Description**                                                                               |
| ------------------ | --------------------------------------------------------------------------------------------- |
| **capitalize**()   | *Converts the first character to upper case*                                                    |
| **casefold**()     | *Converts string into lower case*                                                               |
| **center**()       | *Returns a centered string*                                                                     |
| **count**()        | *Returns the number of times a specified value occurs in a string*                              |
| **encode**()       | *Returns an encoded version of the string*                                                      |
| **endswith**()     | *Returns true if the string ends with the specified value*                                      |
| **expandtabs**()   | *Sets the tab size of the string*                                                               |
| **find**()         | *Searches the string for a specified value and returns the position of where it was found*      |
| **format**()       | *Formats specified values in a string*                                                          |
| **format_map**()   | *Formats specified values in a string*                                                          |
| **index**()        | *Searches the string for a specified value and returns the position of where it was found*      |
| **isalnum**()      | *Returns True if all characters in the string are alphanumeric*                                 |
| **isalpha**()      | *Returns True if all characters in the string are in the alphabet*                              |
| **isascii**()      | *Returns True if all characters in the string are ascii characters*                             |
| **isdecimal**()    | *Returns True if all characters in the string are decimals*                                     |
| **isdigit**()      | *Returns True if all characters in the string are digits*                                       |
| **isidentifier**() | *Returns True if the string is an identifier*                                                   |
| **islower**()      | *Returns True if all characters in the string are lower case*                                   |
| **isnumeric**()    | *Returns True if all characters in the string are numeric*                                      |
| **isprintable**()  | *Returns True if all characters in the string are printable*                                    |
| **isspace**()      | *Returns True if all characters in the string are whitespaces*                                  |
| **istitle**()      | *Returns True if the string follows the rules of a title*                                       |
| **isupper**()      | *Returns True if all characters in the string are upper case*                                   |
| **join**()         | *Joins the elements of an iterable to the end of the string*                                    |
| **ljust**()        | *Returns a left justified version of the string*                                                |
| **lower**()        | *Converts a string into lower case*                                                             |
| **lstrip**()       | *Returns a left trim version of the string*                                                     |
| **maketrans**()    | *Returns a translation table to be used in translations*                                        |
| **partition**()    | *Returns a tuple where the string is parted into three parts*                                   |
| **replace**()      | *Returns a string where a specified value is replaced with a specified value*                   |
| **rfind**()        | *Searches the string for a specified value and returns the last position of where it was found* |
| **rindex**()       | *Searches the string for a specified value and returns the last position of where it was found* |
| **rjust**()        | *Returns a right justified version of the string*                                               |
| **rpartition**()   | *Returns a tuple where the string is parted into three parts*                                   |
| **rsplit**()       | *Splits the string at the specified separator, and returns a list*                              |
| **rstrip**()       | *Returns a right trim version of the string*                                                    |
| **split**()        | *Splits the string at the specified separator, and returns a list*                              |
| **splitlines**()   | *Splits the string at line breaks and returns a list*                                           |
| **startswith**()   | *Returns true if the string starts with the specified value*                                    |
| **strip**()        | *Returns a trimmed version of the string*                                                       |
| **swapcase**()     | *Swaps cases, lower case becomes upper case and vice versa*                                     |
| **title**()        | *Converts the first character of each word to upper case*                                       |
| **translate**()    | *Returns a translated string*                                                                   |
| **upper**()        | *Converts a string into upper case*                                                             |
| **zfill**()        | *Fills the string with a specified number of 0 values at the beginning*                         |
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

To insert illegal characters in a string, we use the escape character: *\\*
```python
string = "This is a \"quote\" in a string"
```

Here is a list of the escape characters:

| **Code** | **Result**      |
| -------- | --------------- |
| **\'**   | *Single Quote*    |
| **\\**   | *Backslash*       |
| **\n**   | *New Line*        |
| **\r**   | *Carriage Return* |
| **\t**   | *Tab*             |
| **\b**   | *Backspace*       |
| **\f**   | *Form Feed*       |
| **\ooo** | *Octal value*     |
| **\xhh** | *Hex value*       |
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

# Lists

**Lists** are 

# Tuples

# Sets

# Dictionaries
 