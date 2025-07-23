# Library Book Manager – Mini Console Project

You’ve just completed **Chapter 4**, where you explored the power of *pattern matching* in Haskell:

1. **Pattern matching in functions**
2. **Catch-all patterns**
3. **Closer look at lists**
4. **Lists and tuples**
5. **Case expressions**
6. **Declaration style vs. expression style**

This mini-marathon challenges you to build a simple **command-line library book manager**. You’ll manage book check-ins/check-outs and search inventory using **pattern matching** everywhere it shines.

---

### Objectives

* **Use pattern matching in function definitions** – process user actions (`CheckIn`, `CheckOut`, `Search`) with clarity.
* **Design expressive data types** – model books using **records**, tuples, or custom types.
* **Apply catch-all patterns safely** – handle unexpected input without crashing.
* **Practice `case` expressions** – perform deeper matching on book status or search queries.
* **Work with list patterns** – manipulate a catalog (`[Book]`) using head/tail splitting, empty checks, or filters.
* **Contrast declaration vs expression styles** – implement some handlers in both forms for clarity.
* **Encourage modular thinking** – split logic across pure functions (e.g., `searchBooks`, `updateInventory`, `displayBook :: Book -> String`).

---

### What to Deliver

A runnable console app that:

- Displays a simple welcome prompt and list of actions (check in, check out, search, exit)
- Uses pattern matching to route each command
- Updates the book catalog based on user input
- Outputs search results or status messages clearly
- Uses `case`, tuple, and list patterns where relevant

---

### Bonus Challenges

- Add `Maybe Book` for search results and handle `Nothing` gracefully.
- Let the catalog persist between sessions using simple file I/O.
- Use tuples for storing `(BookTitle, Status)` and match accordingly.

---

### Build Instructions

1. Run and test in **GHCi**
2. Package with **Stack** or **Cabal**
3. Add a README describing the purpose and how to run it