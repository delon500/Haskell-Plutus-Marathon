# SafeBudget – Mini Console Project

You have just wrapped up **Chapter 15**, where we explored how Haskell handles things that can go wrong:

1. **There’re always Exceptions to the rule**
2. **Speed‑running Exceptions with a dumb self‑driving car**

   * *I’m the Exception ’cause I have class*
   * *Throw all the Exceptions you want. I’ll catch them all!*
3. **Maybe give me a value?** – benefits of optional values
4. **Ok, you Either give me a value or a reason why you didn’t!**
5. **From Exceptions to optional values**
6. **Tradeoffs** – *So, what should I use?*

Your mission is to build a compact **command‑line budget tool**—**SafeBudget**—that reads an expenses file, lets users add/inspect entries, and robustly handles every kind of “oops”: missing data, malformed numbers, and IO failures. Every feature should showcase one or more of the Chapter 15 concepts above.

---

### **Objectives**

By completing this Marathon you will be able to:

* **Raise and catch runtime Exceptions** for IO problems (e.g., missing file, permission denied) using `throwIO`, `catch`, or `try` from `Control.Exception`.
* Use **`Maybe`** to represent optional/missing fields (e.g., a note on an expense). Explain its benefits in your README.
* Use **`Either error value`** to return rich error info when parsing lines (e.g., `Either ParseError Expense`).
* **Convert Exceptions to `Either`/`Maybe`** (e.g., `try @IOException` → `Either IOException …`) and discuss when that’s preferable.
* Demonstrate **tradeoffs**: when to choose Exceptions vs `Maybe` vs `Either`, and justify your choices.
* Implement a small “**crash test**” mode (inspired by the *dumb self‑driving car* section) that deliberately triggers a few errors so you can prove your handlers work.
* Keep pure parsing/validation logic separate from impure IO; surface errors at the edges.
* Package and run your program with **GHCi**, **Stack**, or **Cabal**, providing a short README.
* Deliver a runnable console program and document its usage (plus error‑handling strategy) in a README file.

---

**Suggested features**

* `load expenses.csv` → parse each line with `Either` to collect successes and failures.
* `add <amount> <category> [note]` → validate input, store in memory; write back to file safely.
* `list` / `total [category]` → show data; handle empty/missing values via `Maybe`.
* `crash-test` → intentionally open a non‑existent file and divide by zero (caught!), then report how each error was handled.

Design it so failures are *expected* and gracefully managed—because in the real world, they are.
