 #programming #rust

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

When defining a parameter we need to specify its **type**, just like any other piece of code.

```rust
fn main() {
	another_function(5);
}

fn another_function(x: i32) {
	println!("The value of x is: {x}");
}
```