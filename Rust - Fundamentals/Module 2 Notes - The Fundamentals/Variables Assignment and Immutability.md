# Variable Assignment and Immutability

## Sample Code

```rust
fn main() {
    let message = "Name: John, Weight: ";
    let weight = 190;

    let kilos = weight / 2.2;
    println!("{}{}", message, weight);
}
```

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
let kilos = weight / 2.2;
```

In the code expression above, when you try to divide an integer by a float, you encounter an error
because Rust does not allow this operation directly. The variable `weight` is an integer (in this case,
`190`), and `2.2` is a float. **_Rust is strict about types_**, meaning it wants to ensure that the
operations you perform make sense with the types involved.

Think of it like trying to divide a whole number of apples by a fraction of an apple. It just doesn't
work without converting the whole number into a fraction first. To fix this, you need to make sure both
numbers are of the same type. You can do this by converting `weight` to a float.

```rust
let weight = 190.0; // Now weight is a float
let kilos = weight / 2.2; // This works because both are floats
```

Alternatively, if you want to keep `weight` as an integer, you can convert it to a float during the
division:

```rust
let weight = 190; // weight is an integer
let kilos = weight as f64 / 2.2; // Convert weight to float for the division
```

By ensuring both values are of the same type, you can perform the division without any errors.
