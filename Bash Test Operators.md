#programming #programming/bash 

# Bash Test Operators

By enclosing an **expression** in **square brackets** *\[\]* we can evaluate if it is **true (1) or false (0)**.

```bash
[ hello = hello ]
echo $?
[ 1 = 0 ]
echo $?
[ 1234 = 1234 ]
echo $?
```

The **$? variable** returns the exit code of the last comand