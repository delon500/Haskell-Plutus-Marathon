# Pocket Ledger – Mini Console Project

You have just wrapped up **Chapter 2**, where we dug deeper into Haskell Data types, Signatures, and Polymorphism:

1. A **pragmatic view on types**
2. Writing **function signatures** that serve as mini‑specs
3. **Playing with functions** – partial application, sections, and higher‑order style
4. Using **variables** (immutable bindings) via `let … in` and `where` blocks
5. Crafting **infix vs prefix functions** and custom operators
6. Leveraging **common data types** (Int,`Bool`, tuples, lists)
7. Creating and consuming **polymorphic values / type variables**
8. Having **fun with lists** – `map`, `filter`, `fold`, recursion, comprehensions

Your mission is to build a compact **command‑line expense tracker**—**Pocket Ledger**—that lets users add purchases, list them, total spending, and undo the last entry. Every feature should showcase one or more of the Chapter 2 concepts above.

---

### **Objectives**

By completing this Marathon you will be able to:

* Write **type‑driven code** with clear signatures and minimal ambiguity.
* Employ **higher‑order functions** (`map`, `filter`, folds) and experiment with **partial application**.
* Declare and use your own **infix operator** to make list manipulation more readable.
* Distinguish between **prefix** and **infix** forms and know when each improves clarity.
* Model data with **tuples, lists, and `Maybe`**, and pattern‑match over them fluently.
* Design one or two **polymorphic helpers** (e.g., a generic `groupOn`) to see type variables in action.
* Keep your logic pure while using `IO` only for interaction, reinforcing functional thinking.
* Package and run your program with **GHCi**, **Stack**, or **Cabal**, providing a short README.
* Deliver a runnable console program and document its usage in a README file
