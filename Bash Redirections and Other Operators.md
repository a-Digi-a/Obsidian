#programming #programming/bash 

# Bash Redirections and Other Operators

## Piping Bash Commands

**Piping** sends the output of one command to another command:

```bash
ls | grep Downloads
```

This command feeds the **output** of *ls* into *grep*

## Redirecting Output

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

## Redirecting Input

By using the *<* operator we can **redirect the input** of a command/file:

```shell
wc -w hello.txt # Will print the name of the file as the file is an argument
wc -w < hello.txt # Will not print the name of the file as the file is not an argument
```

By using the *<<* operator we can **read lines from a source until a line with only the delimiter appears**

```bash
cat << EOF
```

This command will allow us to write text until a line that contains **only** the text **EOF** (does not work inside of obsidian)

The *<<<* operator allows us to **feed a string into a command**:

```bash
wc -w <<< "Hello There Wordcount!"
```

