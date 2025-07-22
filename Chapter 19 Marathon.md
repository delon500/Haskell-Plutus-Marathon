# Student Eligibility Checker – Mini Console Project

You have just finished **Chapter 19**, where we dove into the art of *applicative programming in Haskell*:

1. **Function application at the Functor level**
2. **Purity vs effectful computation**
3. **The `Applicative` type class**
4. **Applicative laws** (identity, composition, homomorphism, interchange)
5. **Programming with effects** (`Maybe`, `IO`)
6. **`Control.Applicative` helpers** (`pure`, `<*>`, `<$>`, `liftA2`, `optional`, etc.)

This marathon is to design a small **command‑line app**—**Student Eligibility Checker**—that helps school administrators determine scholarship eligibility while showcasing **every** concept above in a meaningful way.

---

### **Objectives**

* **Separate pure logic from `IO`** – gather user input interactively, then run validation in a side‑effect‑free pipeline.
* **Apply applicative style elegantly** – combine optional fields with `pure`, `<$>`, `<*>`, and `liftA2` instead of explicit case analysis.
* **Respect Haskell’s layout rule** – use clear indentation, descriptive comments, and informative **type signatures** (e.g., `Student`, `isEligible :: Student -> Maybe Bool`).
* **Demonstrate `Maybe` as a validation context** – treat missing data (`Nothing`) naturally while propagating failure.
* **Encode scholarship criteria declaratively** –

  * GPA ≥ 3.5
  * **and** extracurricular participation
  * **and** (financial need **or** a recommendation letter)
* **Leverage laziness for ergonomics** – ask only for the data you actually need.
* **Build & test in GHCi**, then package with **Stack** or **Cabal**; document usage and build steps in a concise **README**.

Deliver a runnable console program that prompts for each field (allowing the user to *skip* any question), reports the eligibility result, and exemplifies the applicative patterns explored in Chapter 19.