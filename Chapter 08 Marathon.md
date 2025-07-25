# Student Profile Manager – Mini Console Project

You have just finished **Chapter 8**, where you explored how to design and organise your own **types** in Haskell:

1. **Type synonyms** – giving long types short, meaningful names
2. **New types with `data`** – building custom, domain‑specific structures
3. Creating and using those types in real code
4. **Value parameters** – adding polymorphic flexibility
5. **Record syntax** – readable field names and automatic getters

Your marathon is to build a small **command‑line Student Profile Manager** that lets users add, view, search, and update student records. The program must demonstrate every concept above.

---

### **Objectives**

By completing this Marathon you will be able to:

* Define and use **type synonyms** such as `Name`, `StudentID`, and `CGPA`.
* Declare a **custom `Student` data type** with **record syntax**.
* Update and access record fields clearly and expressively.
* Experiment with **value‑parameterised records** for reusable structures.
* Organise input/output through a clean, menu‑driven flow that separates pure logic from `IO`.

A suggested function breakdown:

```haskell
addStudent    :: IO Student
showStudents  :: [Student] -> IO ()
searchByID    :: [Student] -> IO ()
updateCGPA    :: [Student] -> IO [Student]
```

---

### **what to deliver**

A runnable console application that:

1. Greets the user and shows a menu:

   * Add Student
   * Show All Students
   * Search by ID
   * Update CGPA
   * Exit

2. Demonstrates Chapter 8 concepts:

   * Uses **type synonyms** in signatures for clarity.
   * Defines a **`Student` record** via `data` and record syntax.
   * Stores student records in memory and manipulates them with pattern matching and list functions.
   * Keeps logic modular through helper functions.

---

### **bonus challenges**

* Implement a “Delete Student” option by ID.

* Persist data with basic file I/O (`readFile`, `writeFile`).

* Create a **generic record** type using value parameters:

  ```haskell
  data Record a = Record { recordId :: Int, content :: a }
  ```

* Nest a `Course` type inside each student for multi‑course tracking.

* Split code into modules, exposing only safe access functions and hiding internals.

---

### **build instructions**

1. Develop and test interactively in **GHCi**.
2. Place all logic in a `Main.hs` module, broken into small, focused functions.
3. (Optional) package the project with **Stack** or **Cabal** and provide build commands.
4. Include a concise `README.md` that explains:

   * What the app does.
   * How to compile and run it.
   * Example inputs and outputs.
