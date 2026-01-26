#programming #programming/bash 

# Bash Parameter Expansion

In **bash**, **parameter expansion** allows us to **substitute a parameter reference with its value**. This is useful for modifying the parameter in some way in an expression **without** changing its actual value. We do a **parameter expansion** by using **curly braces**: *{}*

```bash
var1="YES"
echo $var1 ${var1}
```

# Getting the Lowercase Version of a Parameter

We can get the lowercase version of a string with the ,, operator:

```bash
var1="YES"
echo $var1 ${var1,,}
```

This is useful for confirmations (y/n)

