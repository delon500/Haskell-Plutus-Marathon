# TimeSlice – Mini Console Project

You have just wrapped up **Chapter 13**, where we learned how to structure Haskell programs with **modules**:

1. **Importing modules**
   * Controlling environments (what is brought into scope)
   * Controlling namespaces (qualified imports, aliases, hiding)
2. **Creating our own modules**
3. **The Prelude and standard libraries**

Your mission is to build a compact **command‑line time tracker**—**TimeSlice**—that lets users log work sessions for projects, list totals, and export a report. Every feature should showcase one or more of the Chapter 13 concepts above.

---

### **Objectives**

By completing this Marathon you will be able to:

* Create and organise your own **modules** (e.g. `Domain.Session`, `UI.Menu`, `Storage.CSV`).
* Control **import environments** with explicit import lists and `hiding`.
* Control **namespaces** using `qualified` imports and `as` aliases to avoid clashes.
* Demonstrate awareness of the **Prelude**: when it’s implicit, how to hide/replace parts of it, and how to bring in standard libraries consciously.
* Keep pure business logic (totals, grouping) separate from IO concerns (reading/writing files, prompts) via module boundaries.
* Package and run your program with **GHCi**, **Stack**, or **Cabal**, providing a short README.
* Deliver a runnable console program and document its usage in a README file.
