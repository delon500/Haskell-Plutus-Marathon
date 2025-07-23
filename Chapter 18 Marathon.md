# Error-Tolerant Form Validator - Mini Console Project

## Description

Create a console application that validates user input for a form (e.g., registration form with name, email, age, etc.). Each validation may succeed or fail, and the program should:

- Map transformations and validation logic over input using **Functor**.
- Combine multiple validations and accumulate errors using **Semigroup** and **Monoid**.
- Demonstrate working with `Either`, `(,)`, and function `Functor` instances.
- Emphasize **error tolerance**: collect all validation errors instead of failing fast.

---

## Objectives

By completing this Marathon, you will:

- Understand how to **abstract the map function** using the **Functor** type class.
- Define and apply **Functor instances** for custom and standard types.
- Discover how `Either a`, `(,) a`, and `(->) r` are valid (though unintuitive) functors.
- Use `<$>` and **function lifting** to transform data in functorial contexts.
- Nest and compose multiple functor layers (Functor nesting dolls 🪆).
- Use **Semigroup** to combine error messages and **Monoid** for identity fallback.
- Build a real-world form validation system using purely functional principles.

---

## Outline

1. Define a `Validation` type using `Either [String] a` or a custom type like:

    ```haskell
    data Validation e a = Failure e | Success a
      deriving (Show, Eq)
    ```

2. Create `Functor` instances for:
   - `Validation`
   - `(,)`
   - `(->)`

3. Write validation functions for each form field:
   - **Name**: Must not be empty
   - **Email**: Must contain `@`
   - **Age**: Must be a number greater than 0

4. Use `<$>` and `<*>` to apply validations over user input.

5. Use `Semigroup` to **combine multiple error messages**:

    ```haskell
    instance Semigroup e => Applicative (Validation e) where
      pure = Success
      Success f <*> Success x = Success (f x)
      Failure e1 <*> Failure e2 = Failure (e1 <> e2)
      Failure e <*> _ = Failure e
      _ <*> Failure e = Failure e
    ```

6. Use `Monoid` to define **identity values** for error accumulation.

7. Create a `User` record type to collect valid input:

    ```haskell
    data User = User {
      name :: String,
      email :: String,
      age :: Int
    } deriving Show
    ```

8. Return either:
   - a fully validated user: `Success User`
   - or a list of all validation failures: `Failure [String]`

9. Print the results clearly to the console.

---

## Example Question

> **Scenario:**  
> You are tasked with creating a form validation system that checks a user’s input (`name`, `email`, and `age`). If the form contains multiple issues (e.g., empty name *and* invalid email), the system should display **all errors together**.
>
> ### Your Task:
>
> 1. How can you use the **Functor** abstraction to map over potentially failing values?
> 2. How can `Either` or a custom `Validation` type help you represent both **success** and **multiple failures**?
> 3. How can you use **Semigroup** and **Monoid** to accumulate error messages?
>
> **Implement**:  
> A console application that:
> - Validates user input
> - Accumulates and reports multiple validation errors
> - Returns a `User` record if validation succeeds

---
