 #programming #programming/rust

# The main function 
The main function, denoted by:
```rust
fn main() {
	// Code here
}
```
is the entry point for your program, i.e..  it is what is run when you execute your program.

# Defining a function

We can define a function by using the **fn** keyword:

```rust
fn main() {
	println!("Hello, World!");
	
	another_function();
}

fn another_function() {
	println!("Another function.")
}
```

Note that the function was defined **outside of the main function**. It can anywhere, as long as it can be seen by the caller.

# Parameters

We can define functions that have **parameters**, which are variables inside of a function's code. You can then pass **arguments** into the function, which are the concrete values that **replace** the parameters.

When defining a parameter we **must** specify its **type**, just like any other piece of code.

```rust
fn main() {
	another_function(5);
}

fn another_function(x: i32) {
	println!("The value of x is: {x}");
}
```

In this case, the parameter of **another_function()** is **x** of type **i32**. The argument passed into the function is **5**.

You can also use **multiple parameters**:
```rust
fn main() {
	print_labeled_measurement(5, 'h');
}

fn print_labeled_measurement(value: i32, unit_label: char) {
	println!("The measurement is: {value}{unit_label}")
}
```


# Functions with Return Values

**Functions** can **return values** 

# Statements and Expressions

**Statements** are instructions that do an action but **do not** return a value.
**Expressions** evaluate to a resultant value; If you assign it to a variable, it will be valid code.

Lets look at an example:

```rust
fn main() {
	let y = 6;
}
```

in this code, **let y = 6** is a statement, while **y = 6** is an expression.

**Function definitions** are also statements, and statements do **not** return values. Therefore, you **cannot** use a **let** statement with it:

```rust
fn main() {
	let x = (let y = 6);
}
```

This code will return an error, as a statement does not return a value.
