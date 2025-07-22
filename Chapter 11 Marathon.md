# To-Do List Manager – Mini Console Project

In this chapter, we explored several key Haskell concepts related to IO and control flow:

1. *Pure functions* for data manipulation  
2. *IO actions* such as getLine, putStrLn  
3. *Composing IO actions* with >> and >>=  
4. *The do notation* for sequencing actions  
5. *Interacting with users* in a console application  
6. *Using () type, return, and let bindings* within IO  

Your marathon is to design a simple *command-line to-do list application—To-Do List Manager*—that demonstrates these concepts by solving a common real-life problem: managing a list of tasks.

---

### objectives

By completing this mini project, you will be able to:

* Write pure functions that manipulate a list of tasks  
* Use IO actions to interact with the user via the console  
* Compose multiple IO actions to create a smooth user experience  
* Use the do notation to sequence actions clearly  
* Implement simple control flow to handle user choices  
* Build a runnable console program with clear user instructions  

---

### Your task

Create a Haskell program that maintains a dynamic to-do list with the following features:

- View all current tasks  
- Add a new task  
- Remove a task by number  
- Exit the program  

Design the program so that the user can repeatedly perform these actions until choosing to exit. Use pure functions for data manipulation, and IO actions for interaction. Incorporate control flow (if statements, guards, pattern matching) to handle user input gracefully.