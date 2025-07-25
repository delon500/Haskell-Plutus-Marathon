# Type‑Savvy Calculator – Mini Console Project

You have just finished **Chapter 7**, where you explored the power of **type classes** in Haskell:

1. **What type classes are**
2. Core type classes: `Eq`, `Ord`, `Num`, `Integral`, `Floating`, `Read`, `Show`
3. Writing the most general (most polymorphic) valid types
4. Combining **multiple constraints** in a single function

This marathon is to create a **type‑driven console calculator** that showcases how Haskell’s type‑class system enables polymorphic arithmetic, comparisons, and string conversions while keeping the code clean and type‑safe.

---

### **objectives**

By completing this Marathon you will be able to:

* Use **`Eq` and `Ord`** to compare two user‑supplied values.
* Apply **`Num`, `Integral`, and `Floating`** constraints to perform arithmetic on different numeric types.
* Convert cleanly between strings and values with **`Read` and `Show`**.
* Write **polymorphic functions** featuring type variables and constraints.
* Combine **multiple constraints** in a single signature (e.g., `(Eq a, Num a) => …`).
* Aim for **maximal generality**—write each function with the most permissive, yet valid, type.

A suggested module breakdown:

```haskell
compareValues   :: (Eq a, Ord a, Show a)     => a -> a -> String
performOperation :: (Num a, Show a)          => String -> a -> a -> String
parseInput       :: Read a                   => String -> Maybe a
```

---

### **what to deliver**

A runnable command‑line program that:

1. Greets the user and displays a menu:

   * Compare Values
   * Perform Operation
   * Parse from String
   * Convert to String
   * Exit

2. Executes the chosen action, demonstrating appropriate **type‑class constraints**:

   * Equality and ordering (`==`, `>`, `<`) require `Eq`/`Ord`.
   * Arithmetic (`+`, `-`, `*`, `/`) requires `Num`, `Integral`, or `Floating`.
   * Conversions make use of `Read` and `Show`.
   * Accepts either `Int` **or** `Float` inputs where sensible.

---

### **bonus challenges**

* Handle invalid `Read` inputs gracefully with `Maybe` or `Either`.
* Define a custom numeric data type (e.g., `MyNumber`) and create `Eq`, `Ord`, and `Show` instances for it.
* Add simple file I/O to save and load past calculations.
* Provide explicit type signatures for **every** user‑defined function.
* Demonstrate **multiple constraints** in at least one non‑trivial function.

---

### **build instructions**

1. Develop and test interactively in **GHCi**.
2. Keep all code in a single `Main.hs`, structured into small, readable functions.
3. (Optional) turn the folder into a project with **Stack** (`stack new`) or **Cabal** (`cabal init`) and supply build commands in the README.
4. Include a concise `README.md` covering:

   * What the calculator does.
   * How to compile and run it with `ghc`, `stack`, or `cabal`.
   * Sample inputs and expected outputs.
