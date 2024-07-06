# Rust Style Guide for AMALTHEA

## Table of Contents
1. [Introduction](#introduction)
2. [Code Formatting](#code-formatting)
3. [Naming Conventions](#naming-conventions)
4. [Error Handling](#error-handling)
5. [Concurrency](#concurrency)
6. [Testing](#testing)

## Introduction
This style guide is intended for developers working on AMALTHEA in Rust. The guidelines presented here aim to promote code clarity, maintainability, and safety in line with AMALTHEA and future projects based on it's codebase.

## Code Formatting
- **Indentation:** Use 4 spaces for indentation, not tabs.
- **Maximum Line Length:** Keep lines to a maximum of 80 characters where possible.
- **Braces:** Opening braces should not be on their own line. Use same-line braces.
- **Use `rustfmt`:** Run `rustfmt` before every commit to ensure consistent formatting.

## Naming Conventions
- **Variables and Functions:** Use `snake_case` for variable names and function names.
- **Types and Traits:** Use `PascalCase` for type names, including structs, enums, and traits.
- **Constants:** Use `SCREAMING_SNAKE_CASE` for constants.
- **Modules:** Keep module names short and descriptive, using `snake_case`.

## Error Handling
- **Use `Result<T, E>`:** Favor using `Result` over `panic!` or `unwrap()` for recoverable errors.
- **Custom Error Types:** Define project-specific error types that implement `std::error::Error`.
- **Documentation:** Clearly document the possible error cases of each function.

## Concurrency
- **Avoid `unsafe` Code:** Minimize the use of `unsafe` blocks, especially in concurrent contexts.
- **Use Rust's Ownership:** Leverage Rust’s ownership and borrowing rules to prevent data races.
- **RTOS Integration:** Follow best practices for integrating with the real-time operating system (RTOS) used in the project.

## Testing
- **Unit Testing:** Write unit tests for all new code where practical using `#[test]`.
- **Integration Testing:** Regularly run integration tests that reflect real-world operating conditions.
- **Mocking:** Use mocking and simulation to test components in isolation.

## Documentation
- **Commenting:** Use comments to explain "why" something is done, not "how". Rust code should be self-explanatory.
- **Doc Comments:** Use `///` for doc comments to generate software documentation with `cargo doc`.
