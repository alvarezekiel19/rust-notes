# Variable Assignment and Immutability

In Rust, variable assignment is how we create and store values in our programs. To assign a value
to a variable, we use the keyword `let`, followed by the name of the variable and the value we want
to store. For example, if we want to store a person's weight we might write: `let weight = 190;`
This means we have a variable called `weight` that holds the value `190`. However, in Rust, variables
are **immutable** by default, which means once we set a value, we can't change it unless we specifically
tell Rust we want to make it mutable byu sing the `mut` keyword.

Imagine you have a box labeled "weight" that you put a 190-pound weight in. If you want to change the
weight to something else, you need to get a new box or tell the box that it can change its contents. In
Rust, if you want to change the value of a variable, you need to declare it as mutable like this:

```rust
let mut weight = 190;
weight = 200; // Now we can change the value to 200
```

This way, you can change the contents of your box whenever you need to.

```rust
fn main() {
    let message = "Name: John, Weight: ";
    let weight = 190;

    let kilos = weight / 2.2;
    println!("{}{}", message, weight);
}
```
