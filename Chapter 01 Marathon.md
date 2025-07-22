# Prime Playground – Mini Console Project

You have just finished **Chapter 1**, where we explored pillars of *introductory Haskell*:

1. **What is Haskell?** & the functional‑first mindset
2. **Function composition** (`.`)
3. **Explicit effects vs pure code**
4. **Basic syntax** & the layout/indentation rule (no braces, few semicolons)
5. **Defining and using functions** with clear comments
6. The **Haskell type system** (from concrete types to polymorphism)
7. **Laziness** and infinite data structures
8. Tooling with **GHC (GHCi)**, **Cabal**, and **Stack**

Your task is to design a small **command‑line app**—**Prime Playground**—that lets users *explore prime numbers* (e.g., list the first *n* primes, check if an integer is prime) while demonstrating **every** concept above in a meaningful way.

---

### **Objectives**

By completing this Marathon you will be able to:

* Illustrate the difference between **pure** prime‑number logic and side‑effecting `IO`.
* Chain calculations elegantly using **function composition**.
* Respect Haskell’s **layout rule** with readable indentation and helpful comments.
* Declare informative **type signatures** and leverage polymorphism where sensible.
* Exploit **laziness** to create infinite streams of primes that are evaluated on demand.
* Build, run, and debug your code in **GHCi**, plus package it with **Stack** or **Cabal**.
* Make sure you have installed **GHC**, **Cabal**, and **Stack** on your system.
* Use **GHCi** to test your functions interactively and explore their behavior.
* Deliver a runnable console program and document its usage in a README file