# Delivery Route Optimizer – Mini Console Project

You have just finished **Chapter 20**, where we stepped beyond functors and applicatives into *full‑blown monadic power*:

1. **The `Maybe` monad** for optional / failing computations
2. **The list (`[]`) monad** for non‑deterministic branching and combinatorics
3. **Monad laws** – **left identity**, **right identity**, and **associativity** – and why they matter for program correctness

This marathon is to create a small **command‑line app**—**Delivery Route Optimizer**—that plans simple delivery routes while showcasing **every** concept above in a meaningful way.

---

### **Objectives**

* **Handle missing input safely with `Maybe`** – treat absent driver names or warehouse locations as `Nothing`, propagating failure without manual checks.
* **Generate route permutations with the list monad** – combine a single warehouse with many delivery points to explore *all* possible drop‑off sequences.
* **Respect monadic purity vs `IO`** – gather user data interactively, then run pure monadic logic to build routes.
* **Verify the monad laws in code** – print checks (Boolean results) demonstrating that `Maybe` obeys left/right identity and associativity for a sample function.
* **Deliver readable, well‑typed Haskell** – include clear type signatures (e.g., `planRoutes :: String -> String -> [String] -> [String]`), follow the layout rule, and comment key steps.
* **Build & test in GHCi**, then package with **Stack** or **Cabal**; document usage and build steps in a concise **README**.

---

### **Functional Spec**

1. **Prompt** the user for:

   * Driver name (or “skip”)
   * Warehouse location (or “skip”)
   * Delivery points (comma‑separated list; empty means “skip”)

2. **Parse inputs** into a `Maybe (Driver, Warehouse, [Destination])`.

3. **If any field is `Nothing`**, halt with a friendly message.

4. Otherwise, **use the list monad** to generate every ordering of delivery points and print lines like:

   ```
   Driver Alice will deliver from Central Depot to Mall → Airport → Stadium
   ```

5. **Run monad‑law tests** for `Maybe` using a sample function `f` and value `x`, printing whether each law holds.

Deliver a runnable console program that brings Chapter 20’s monads to life while keeping side‑effects isolated and code elegant.