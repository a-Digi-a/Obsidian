
 #programming #programming/python #semester-2 

# Python Shebang

The **shebang** in python, denoted by *!#* is used to tell the shell running the script where the [[Python Interpreter]] is located on the system. On **windows** this is usually not needed, as it is stored in an environment variable.

For example:

```python
#! /usr/bin/python
print("Hello World")
```

This allows us to run:
```shell
./hello.py
```
Instead of:
```shell
python hello.py
```