#programming #programming/bash 

# Bash Command Operators

## Piping Bash Commands

**Piping** sends the output of one command to another command:

```bash
ls | grep Downloads
```

This command feeds the **output** of *ls* into *grep*

## Writing and Appending Bash Command Output

By using the *>* operator we can **write** **the** **output** of a **command** to a file:

```bash
echo Hello, World! > hello.txt
cat hello.txt
```

By using the *>>* operator we can **append the output** of a **command** to a file:

```bash
echo Goodbye, World! >> hello.txt
cat hello.txt
```

These commands are useful for **creating log files**, **making config files** and more!


Run this command to remove the text file created (if you ran the ones above)
```bash
rm hello.txt
```

## 