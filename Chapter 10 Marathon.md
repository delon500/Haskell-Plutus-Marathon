# Library Book Manager – Mini Console Project

You have just finished Chapter 10, where we explored advanced Haskell features including:

1. *Type Classes (Eq, Ord, custom classes)*
2. *Overloading functions via type classes*
3. *Creating instances for parameterized types*
4. *Subclassing (Ord as a subclass of Eq)*
5. *Using deriving and understanding its pitfalls*
6. *Implementing multiple instances and mutual recursion*

Your marathon is to develop a small *command-line application—Library Book Manager*—that models a real-world scenario: managing a collection of books in a library. The program should allow users to:

- Add new books
- List all books sorted by title
- Find books by author
- Check if a book is accepted based on custom criteria
- Remove books from the collection

### Objectives

By completing this mini project, you will be able to:

* Design and implement custom type classes and their instances to model real-world entities.
* Use overloading to enable comparison and sorting of complex data types.
* Work with parameterized types to create flexible and reusable data structures.
* Demonstrate understanding of subclassing by implementing ordering for your data types.
* Use deriving to automate instance creation, and recognize when it might cause issues.
* Write a console application that integrates these features in a meaningful way.