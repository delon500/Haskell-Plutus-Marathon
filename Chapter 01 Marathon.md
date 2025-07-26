# Savings Simulator – Mini Console Project

You have just finished **Chapter 1**, where we explored pillars of *introductory Haskell*:

1. **What is Haskell?** & the functional‑first mindset
2. **Function composition** (`.`)
3. **Explicit effects vs pure code**
4. **Basic syntax** & the layout/indentation rule (no braces, few semicolons)
5. **Defining and using functions** with clear comments
6. The **Haskell type system** (from concrete types to polymorphism)
7. **Laziness** and infinite data structures
8. Tooling with **GHC (GHCi)**, **Cabal**, and **Stack**

Your mission is to design a small **command‑line app**—**Savings Simulator** that helps a user figure out how many months it will take to reach a savings goal (and preview their balance over time). It must demonstrate **every** concept above, remain beginner‑friendly, and live comfortably in a single `Main.hs` file (no heavy file management).

---

### **Objectives**

By completing this Marathon you will be able to:

* Separate **pure** calculation logic (monthly balances, months to goal) from `IO` that reads user input.
* Chain computations cleanly with **function composition** (`.`) instead of piling on parentheses.
* Apply Haskell’s **layout rule**: consistent indentation, clear comments, no stray braces/semicolons.
* Write precise **type signatures** (including a small polymorphic function where sensible).
* Use **laziness** by generating an infinite list of running balances and only taking what you need (e.g. first 12 months).
* Build, run, and test in **GHCi**, and optionally package with **Stack** or **Cabal**.
* Ensure **GHC**, **Cabal**, and **Stack** are installed; practise running `ghci` to poke at your pure functions interactively.
* Deliver a runnable console program and document its usage in a short README file.
