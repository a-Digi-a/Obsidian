#programming #programming/bash 

# Bash Loops

## For Loops

We can write **for loops** in bash with the following syntax:

```bash
var1=( 1 2 3 4 )

for item in ${var1[@]}; do 
	echo $item
done
```

note that the **$item** variable is used for the value of the current item being iterated upon.