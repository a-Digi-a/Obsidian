#code #programming #rust

Rust is a statically typed language, meaning that all data types of variables must be known at compile time.

We can declare a variables data type with the syntax below:
```rust
let x: u32 = 5;
```
This code creates a variable **x** with the type **u32**.

# Scalar Types
A **scalar** type represents a single value. Rust has 4 primitive scalar types: **integers**, **floating-point numbers**, **Booleans** and **characters**. 

## Integer Types
An **integer** is a whole number. It comes in 2 main types, **signed** and **unsigned**. A **signed** integer contains both **positive and negative** numbers, while an **unsigned** integer contains only positive numbers (including 0)


|        **Length**        | **Signed** | **Unsigned** |
| :----------------------: | :--------: | :----------: |
|         *8-bit*          |    `i8`    |     `u8`     |
|         *16-bit*         |   `i16`    |    `u16`     |
|         *32-bit*         |   `i32`    |    `u32`     |
|         *64-bit*         |   `i64`    |    `u64`     |
|        *128-bit*         |   `i128`   |    `u128`    |
| *Architecture-dependent* |  `isize`   |   `usize`    |
Every integer can only have $2^n$ values, where *n* is the number of bits used. for example, a *u8* can have 256 values, including 0 this means a *u8* integer stores values from *0-255*.

Each **signed** integer can store numbers from $-(2^{n-1})$ to $2^{n-1}-1$ **inclusive**.
Each **unsigned** integer can store numbers from 0 to $2^{n-1}-1$ **inclusive**.

The *isize* and *usize* values depend on the architecture of the computer you are using: *32 bits* for **32-bit architecture** and *64 bits* for **64-bit architecture**.

The default type of integer is *i32*.

### Integer Overflow

  An **integer overflow** occurs when we try to use a value outside of the range of the integer.
  When an integer overflow occurs, it does something called **wrapping**. Imagine a portal on either side of the integer, if you go 1 above the amount it holds, it will go through the portal and start again.
  For example, if you try to go to the value *256* on a **u8** integer, it will wrap around to *0*. If you try to go to *257*, it will wrap around to *1*. 

An integer overflow is an error, and should be treated as such.

## Floating-Point Types

A **floating point** number is a number with decimal points. They come in both *f32* and *f64* variants. The default type is *f64* because it is roughly the same speed as a *f32* on modern CPUs. All floating point types are signed.

Here is an example of floating point numbers:
```rust
let x = 2.0; // f64
let y: f32 = 4.5; // f32
```
Notice how the floating point type **needs** to have a decimal point.

## Mathematical Operations
Rust supports all of the basic mathematical operations you would expect: **addition**, **subtraction**, **multiplication**, **division** and **remainder/modulo**. This is shown in the code below:

```rust
fn main() {
    // addition
    let sum = 5 + 10;

    // subtraction
    let difference = 95.5 - 4.3;

    // multiplication
    let product = 4 * 30;

    // division
    let quotient = 56.7 / 32.2;
    let truncated = -5 / 3; // Results in -1

    // remainder
    let remainder = 43 % 5;
}
```

## The Boolean Type

The **Boolean** type has 2 possible values: **True** and **False**. They are one byte in size and are specified using bool, shown below:

```rust
fn main() {
    let t = true;

    let f: bool = false; // with explicit type annotation
}
```

## The Character Type

The **char** type is the most primitive alphabetic type in rust. It is 4 bytes in size and it is specified with **single quotes**. The **char** type represents a Unicode scalar value, which can represent not only ASCII, but also other things such as emojis and Chinese/Japanese characters. An example is shown below:

```rust
fn main() {
    let c = 'z';
    let z: char = 'ℤ'; // with explicit type annotation
    let heart_eyed_cat = '😻';
}
```

# Compound Types

Compound types can group multiple values into one type. Rust has two primitive compound types: **tuples** and **arrays**.

## The Tuple Type

A **tuple** is a way of grouping a number of values with a variety of types together. They have a **fixed length**, and **cannot** **grow** or **shrink** in size. We declare a tuple by putting the values inside a set of brackets, separated by commas, as shown below:

```rust
fn main() {
    let tup: (i32, f64, u8) = (500, 6.4, 1);
}
```

We can extract the values from a tuple two a

## The Array Type