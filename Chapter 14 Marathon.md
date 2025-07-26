# AmortiCalc – Mini Console Project

You have just wrapped up **Chapter 14**, where we focused on project scaffolding and modern compiler features:

1. **Cabal**

   * Introduction to Cabal
   * Creating a new Haskell project
   * Inspecting the `.cabal` file and adding an external library
   * Building and running an executable
2. **Language extensions & pragmas**

   * `NumericUnderscores`
   * `TypeApplications`

Your mission is to build a compact **command‑line loan & savings planner**—**AmortiCalc**—that lets users calculate monthly repayments, total interest, or savings growth. Every feature must showcase at least one of the Chapter 14 concepts above.

---

### **Objectives**

By completing this Marathon you will be able to:

* **Initialize a Cabal project** (`cabal init`) and understand each major stanza in the generated `.cabal` file.
* **Add and use at least one external library** (e.g. `time`, `cassava`, `optparse-applicative`, or `ansi-terminal`) by editing the `build-depends` field.
* **Build and run** your executable with `cabal build` / `cabal run`, and verify the binary in `dist-newstyle`.
* Enable **language extensions** via file‑top pragmas:

  ```haskell
  {-# LANGUAGE NumericUnderscores #-}
  {-# LANGUAGE TypeApplications   #-}
  ```

  and actually use them in code (e.g. `let principal = 1_000_000 :: Double`, `read @Double input`).
* Demonstrate **TypeApplications** for parsing/printing without ambiguous types.
* Keep your business logic pure (loan formulas, compounding) and isolate IO in `main`.
* Deliver a runnable console program and document exact build steps in a concise README.

---

### **Core requirements**

Your CLI must at minimum:

1. **Offer a menu or CLI flags** to choose actions, e.g.:

   * Calculate monthly repayment for a loan (`amount`, `rate`, `months`).
   * Show total interest paid over the loan term.
   * Estimate savings growth given a monthly deposit and interest rate.
2. **Use `NumericUnderscores`** at least once for readability of large literals.
3. **Use `TypeApplications`** at least once for `read`/`show` or generic functions.
4. **Pull in and use an external library** (e.g. format tables with `ansi-terminal`, parse CSV scenarios with `cassava`, or parse options with `optparse-applicative`).
5. Compile and run through **Cabal** (screenshots or command transcript encouraged in README).

---

### **Suggested file structure**

```
amorticalc/
├─ app/Main.hs              -- CLI / menu & IO
├─ src/Finance/Loan.hs      -- pure loan math
├─ src/Finance/Savings.hs   -- pure savings math
├─ src/Util/Format.hs       -- pretty printers (maybe uses external lib)
└─ amorticalc.cabal
```

---

### **Deliverables**

* **Source code** with top‑of‑file LANGUAGE pragmas where used.
* A **README.md** (≤ 250 words) that lists:

  * Exact Cabal commands you ran (`cabal init`, `cabal build`, `cabal run`).
  * Which external library you added and why.
  * Where `NumericUnderscores` and `TypeApplications` appear (function names or line numbers).
  * Sample inputs/outputs.
* A **working executable** (verified by `cabal run`) that performs the calculations.

---

### **Bonus challenges**

* Add **CSV import/export** for what‑if scenarios (requires an additional dependency like `cassava`).
* Colourise warnings or results using `ansi-terminal`.
* Use `optparse-applicative` to parse flags instead of an interactive menu.
* Split logic into additional modules and expose only what’s necessary via explicit export lists.
* Turn on `-Werror` and fix all warnings to practice professional build hygiene.

Build it, extend it, and let Cabal plus language extensions make your Haskell smoother and safer.
