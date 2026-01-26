#programming #programming/bash 

# Bash Variables

**Bash variables** are **declared** using the **name=value** syntax, and used with a **dollar sign** following the **variable name**:

```bash
variable1=1
echo $variable1
```

We can **declare** a **local variable** with the **local** keyword:
```bash
function1(){
	local variable1=1
	echo $variable1
}
function1
```