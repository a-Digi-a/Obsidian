#code #programming #rust

# Standard Variables

We can declare a variable by using the **let** keyword as shown here:
```rust
let number = 5;
println!("The value of number is: {number}");
```

[[variables]] are **immutable** by default, meaning they cannot be changed. 

in order to make a variable **mutable**, we must use the **mut** keyword:
```rust
let mut number = 5;
println!("The value of number is: {number}");
number = 6
println!("The value of number is: {number}");
```

# Constants
Constants are variables which cannot be changed. They are different to immutable variables, however.
1. The **mut** keyword cannot be used with constants
2. Constants can be declared in ANY scope, this includes outside of the main function
3. Constants can be only set to a constant expression, not something that is computed at runtime such as user input.
4. Constants cannot be shadowed (next section)
5. Constants are valid for the entire time a program runs
```rust
const NUMBER: i32 = 5;
fn main() {
	println!("The value of number is: {NUMBER}");
}
```
The convention for constant names is **UPPER_SNAKE_CASE**

# Shadowing
 Shadowing is when we declare a new variable with the same name a previous variable. For example:
 ```rust
 fn main() {
    let x = 5;

    let x = x + 1;

    {
        let x = x * 2;
        println!("The value of x in the inner scope is: {x}");
    }

    println!("The value of x is: {x}");
}
```
by using shadowing, we can make a variable immutable after certain transformations, or use them in other situations such as:
```rust
    let spaces = "   ";
    let spaces = spaces.len();
```
Here we can use the same name for this variable for a specific use. Once we find out how many spaces are in this variable, we do not need it anymore. We can shadow it to avoid creating 2 variables.