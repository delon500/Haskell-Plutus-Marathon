# Recursive Budget Analyzer – Mini Console Project

You've just completed **Chapter 6**, where we unlocked the power of recursion and folds in Haskell:

1. **Why recursion?**
2. **Thinking recursively** – breaking down problems into base & recursive steps
3. Recursive patterns: `sum`, `product`, `and`, `length`, `reverse`, `drop`, `take`, `map`, `filter`
4. **Steps to create your own recursive function**
5. **Extracting the `foldr` pattern**
6. **The `foldl` and `foldl'` functions**
7. **When to use `foldr`, `foldl`, and `foldl'`**

This marathon task is to build a **Recursive Budget Analyzer** – a simple command-line app that tracks and analyzes monthly spending, showcasing recursion and folding concepts.

---

## Objectives

- **Define recursive functions** like:
  - `totalSpending`, `countItems`, `findMax`, `findMin`
  - Implement them manually before switching to folds

- **Extract patterns** from recursion to rewrite functions using:
  - `foldr` (right-associative, lazy)
  - `foldl` (left-associative, strict)
  - `foldl'` (from `Data.List` for performance)

- **Apply folds** to:
  - Sum expenses
  - Calculate average spending
  - Reverse the spending list
  - Filter categories (e.g. groceries, transport)

- **Compare when to use `foldr` vs `foldl` vs `foldl'`**:
  - Large datasets → prefer `foldl'` for performance
  - Lazy processing (e.g., infinite lists) → use `foldr`

---

## Deliverables

Create a CLI program that:

- Accepts a list of expenses (category, amount)
- Outputs:
  - Total, average, max, min
  - Reversed list
  - Filtered category views
- Implements and shows both **recursive** and **fold-based** versions
- Uses clear type signatures and modular design

---

## Bonus

- Visualize spending using ASCII bars
- Tag highest and lowest expenses
- Chain folds with point-free style

---

## How to Run

- Test functions in **GHCi** interactively
- Build with **Stack** or **Cabal**
- Include demo usage in your `README.md`