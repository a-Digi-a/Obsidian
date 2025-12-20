  #programming #rust

# What is Cargo?
Cargo is [[Rust]]'s build system and package manager. It is used to handle large projects as it downloads and builds [[libraries]], compiles and runs your code and much more!

# Usage 
## Version
To check cargo's version we can run:
```shell 
cargo --version
```

## Creating Projects
To create a project we can run:
```shell
cargo new hello_cargo
```
This will create a new folder for our project named hello_cargo!

Inside the hello_cargo folder we will find a couple of things:
- a [[cargo.toml]] file
- a [[cargo.lock]] file
- a src directory with our code inside 
- a target directory

## Building and Running a Cargo Project

To build a cargo project we can run:
```shell
cargo build
```
This will put our compiled binary  in the target/debug directory

we can also use:
```shell
cargo run
```
to build and run the project at the same time!

If we want to build for release we can run:
```shell
cargo build --release
```
This will apply some optimizations to make your project run faster 

## Other Commands
We can run:
```shell
cargo check
```
to check if our code will compile.  This saves time over actually building the project.