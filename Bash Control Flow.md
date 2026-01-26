#programming #programming/bash 

# Bash Control Flow

## If Statements

We can use an **if statement** with the following syntax:

```bash
if [ hello = hello ]; then
	echo hello
fi
```

Notice the **fi** keyword at the end of the statement

## Else If Statements

**Bash** also supports **elif** statements:

```bash
if [ hello = world ]; then
	echo Hello, World!
elif [ hello = hello ]; then
	echo hello
fi
```

## Else Statements

**Bash** also supports **else** statements:

```bash
if [ hello = world ]; then
	echo Hello, World!
else
	echo hello
fi
```

Notice there is no **then** statement after **else**

## Case Statements

