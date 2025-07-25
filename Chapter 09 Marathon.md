# MicroLog – Mini Console Project

You have just completed **Chapter 9**, where we level‑up from flat records to *truly custom* data modelling:

1. **Parameterising types** – adding type variables for flexibility
2. **Parameterising type synonyms** – giving one alias many concrete meanings
3. **Parameterising data types** – `data Foo a = …`
4. **Recursive data types**

   * *Tweet me a river* – a custom list/stream
   * *A sequence of nodes* – linked structures
   * *A tree of nodes* – nested reply trees
5. **Kinds** – understanding `*`, `* → *`, and compiler kind errors
6. The **`newtype` keyword** – zero‑cost domain wrappers

Your mission is to build a compact **command‑line micro‑blog**—**MicroLog**—where users post short messages, list a timeline, and reply to tweets. Each feature must illuminate at least one of the Chapter 9 concepts above.

---

### **Objectives**

By completing this Marathon you will be able to:

* Define **parameterised type synonyms** (e.g., `type Id a = Int`) and use phantom types for extra safety.
* Create **parameterised, recursive data types** such as a custom `Stream` and a threaded `Tweet` reply tree.
* Wrap raw primitives in domain‑specific \*\*`newtype`\*\*s (`Username`, `Body`) without runtime overhead.
* Read and reason about **kinds**, recognising why `Stream :: * → *` differs from `Tweet :: * → *`.
* Traverse and mutate recursive structures purely, keeping `IO` only for user interaction.
* Compile and run the program with **GHCi**, **Stack**, or **Cabal**, and document the steps in a README.
* Deliver a runnable console application that clearly demonstrates each Chapter 9 idea.
