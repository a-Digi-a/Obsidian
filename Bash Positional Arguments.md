#programming #programming/bash 

# Bash Positional Arguments

A **positional argument** in **bash** lets us pass values into a bash script. They are separated by spaces and start at 0:
echo 1 2 3 4
0 1 2 3 4

To **positional arguments** are stored in the variables $argument_number. Argument 0 is reserved as that is the command you are running.

For example:

```shell
echo $1 $2
```

If this file was named **script.sh**, and I ran:

```bash
./script.sh Hello World
```

The file would output:

**Hello World**