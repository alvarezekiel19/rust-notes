# 4 Ways to Create a Rust Project

Cargo is a helpful tool to organize everything for you, making it easier to start your project.
You can create a project in two main ways: using `cargo init` for an existing directory or
`cargo new` to create a new directory for your project.

When you use `cargo init`, it sets up your project in the current folder, creating files like
`Cargo.toml` (which holds important information about your project) and `main.rs` (where your main
code goes). If you want to create a library instead of a binary application, you can use `cargo init --lib`,
which will create a `lib.rs` file instead of `main.rs`. On the other hand, `cargo new` creates a whole
new folder for your project, keeping everything neatly organized. This way, you can choose whether you
want a simple project or a more complex one, just like deciding whether to keep your tools in one box
or have separate box for different projects.

## What Is The Difference Between Binary and Library?

#### Binary Packages

    - **Executables**: A Binary Package is designed to be an executable program. When you run it, it performs a specific task.
    - **Main Function**: It contains a `main.rs` file with a `main` function, which is the entry point of the program.
    - **Usage**: Typically used for applications that you want to run directly, like command-line tools or desktop applications.

#### Library Packages:

    - **Reusable Code**: A library package is meant to provide reusable code that can be used by other programs. It does not run on its own.
    - **No `main` Function**: It contains a `lib.rs` file instead of `main.rs`, and it does not have a `main` function.
    - **Usage**: Used to define functions, structs, and traits that can be shared across multiple binary packages or other libraries.

## What Is The Difference Between The 4 Ways of Creating a Rust Project?

#### 1. Using `cargo init .`

    - **Purpose**: Initializes a new Rust project in the current directory.
    - **Output**: Creates a binary applications with `Cargo.toml` and `main.rs`.
    - **Use Case**: Ideal for starting a project in an existing folder.

#### 2. Using `cargo init --lib`

    - **Purpose**: Initializes a new Rust library project in the current directory.
    - **Output**: Creates a library application with `Cargo.toml` and `lib.rs` (no `main.rs`).
    - **Use Case**: Suitable for creating reusable code that can be shared with other projects.

#### 3. Using `cargo new <project_name>`

    - **Purpose**: Creates a new Rust project in a separate subdirectory.
    - **Output**: Generates a binary application with its own folder containing `Cargo.toml` and `main.rs`.
    - **Use Case**: Best for starting a completely new project with its own structure.

#### 4. Using `cargo new <project_name> --lib`

    - **Purpose**: Creates a new Rust library project in a separate subdirectory.
    - **Output**: Generates a library application with its own folder containing `Cargo.toml` and `lib.rs`.
    - **Use Case**: Ideal for starting a new library that can be used by other projects.
