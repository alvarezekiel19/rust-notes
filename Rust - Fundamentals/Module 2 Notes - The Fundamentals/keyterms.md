# Module 2 - The Fundamentals | Key Terms

- **_Binary Application/Package_**: Executables generated from Rust source files, typically containing a main function.
- **_Library_**: A collection of Rust modules providing functionality meant to be shared among multiple projects.
- **_Cargo.toml_**: A configuration file read by Cargo, listing metadata (e.g., name, version) and dependencies required by the package.
- **_Shadowing_**: Reassigning a variable to a new value while preserving its original binding, enabling changes to its type or scope.
- **_Control Flow_**: Conditional execution paths based on evaluation of logical expressions, including if, else, and else if clauses.
- **_Scope_**: A region within source code where names (e.g., functions, variables) are accessible; determined by enclosing braces ({...}) or indentation levels.
- **_Semicolons_**: Terminators denoting statement boundaries, required in most cases except inside blocks, expressions, and macros.

### Rust simple example

```rust
// Demonstrating 'Rust': Basic program structure and comments
fn main() {
    // Printing greeting message
    println!("Hello, world!");
}
```

### `Cargo.toml` example

```toml
# Cargo.toml example
[package]
name = "example_project"
version = "0.1.0"
authors = ["Your Name <your@email.com>"]
edition = "2025"

[dependencies]
rand = "0.8.5" # Add random library dependency
```

### Shadowing

```rust
fn main() {
    // Original integer variable declaration
    let x = 42;
    println!("x: {}", x);

    // Variable reassignment (Shadowing) within the same scope
    let x = "forty-two";
    println!("x: {}", x);

    {
        // Creating a nested scope where 'x' has a new binding
        let x = 42.5;
        println!("x: {}", x);

        // Leaving the inner scope - original bindings restored
    }
}
```
