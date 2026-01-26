#programming #programming/rust 

# Compound Types

Compound types can group multiple values into one type. Rust has two primitive compound types: **tuples** and **arrays**.

# The Tuple Type

A **tuple** is a way of grouping a number of values with a variety of types together. They have a **fixed length**, and **cannot** **grow** or **shrink** in size. We declare a tuple by putting the values inside a set of brackets, separated by commas, as shown below:

```rust
fn main() {
    let tup: (i32, f64, u8) = (500, 6.4, 1);
}
```

We can extract the values from a tuple two ways, as shown below:

```rust
fn main() {
    let tup = (500, 6.4, 1);

    let (x, y, z) = tup; // binds x to 500, y to 6.4, z to 1

    println!("The value of y is: {y}");
}
```

```rust
fn main() {
	let tup = (500, 6.4, 1);
	
	let x = tup.0 // binds x to 500
	let y = tup.1 // binds y to 6.4
	let z = tup.2 // binds z to 1
	
    println!("The value of y is: {y}");
}
```

Both of these code snippets do the exact same thing.

### The Array Type

Similar to a **tuple**, an **array** is a collection of multiple values with a fixed length. Unlike tuples, however, every element of an array must be of the **same type**. An array is declared using square brackets, and you can also specify its size and length:

```rust
fn main() {
    let a = [1, 2, 3, 4, 5];
    
    let b: [i32: 5] = [1, 2, 3, 4, 5];
	
	let c = [3;5]; // an array of length 5 with all elements set to 3
	// c = [3, 3, 3, 3, 3]; 
}
```

To access elements of an array we do array[n] : 

```rust
fn main() {
    let a = [1, 2, 3, 4, 5];

    let first = a[0];
    let second = a[1];
}
```

if you attempt to access an element outside of an arrays index, rust will output a runtime error.


