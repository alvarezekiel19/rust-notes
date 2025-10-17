# Basic Components of Rust Code

The `use` keyword in Rust is essential to for bringing in modules and libraries into your current code file,
making it easier to access and use their features.

- **Purpose**: The `use` keyword allows you to to import modules or libraries into your code.
- **Syntax**: You write `use <library>::<module>;` to specify which module you want to use. For example, `use http::Request;` imports the Request module from the http library.
- **Double Colon (::)**: This acts as a separator, indicating that the module belongs to a specific library.
- **Benefits**: Using `use` keeps your code clean and organized, making it easier to read and understand which resources are being utilized.
