#programming #programming/bash 

# Bash Arrays

**Arrays** in **bash** let us store **multiple values**. An **array** is **declared** with **brackets ()**. We can **access items** in an array using their **index**, or **the @ symbol** for the whole list.

```bash
array=(one two three four five)
echo $array
echo ${array[@]}
echo ${array[2]}
echo ${array[0]}
echo ${array[4]}
```