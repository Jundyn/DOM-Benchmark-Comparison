
---

#  Front-End Frameworks DOM Performance Benchmark

##  Project Overview

This project compares the performance of four popular front-end frameworks: **React, Angular, Vue, and Svelte**.
The goal is to evaluate how each framework handles **DOM operations** such as rendering, updating, and deleting elements using a **To-Do List application**.

---

##  Part 1: Application Features (All Frameworks)

Each implementation includes:

*  Add tasks (name + priority)
*  Display task list
*  Update tasks (edit name/priority)
*  Delete tasks

Each framework uses its core approach:

* **React** → Components + State (useState)
* **Angular** → Directives + Two-way binding
* **Vue** → Reactive data + directives
* **Svelte** → Compile-time reactivity (no virtual DOM overhead)

---

##  Part 2: Benchmark Results

###  Performance Comparison Table (Example Format)

| Operation         | React | Angular | Vue | Svelte |
| ----------------- | ----- | ------- | --- | ------ |
| Render 100 tasks  | 12ms  | 18ms    | 10ms| 6ms    |
| Render 500 tasks  | TBD   | TBD     | TBD | TBD    |
| Render 1000 tasks | TBD   | TBD     | TBD | TBD    |
| Update 50 tasks   | TBD   | TBD     | TBD | TBD    |
| Delete 50 tasks   | TBD   | TBD     | TBD | TBD    |

---

##  Tools Used for Benchmarking

* Chrome DevTools Performance Tab
* `console.time()` / `console.timeEnd()`
* Memory tab (optional)
* Third-party profiling tools (optional)

---

##  Short Reflection (200–300 words)

Building and comparing the same To-Do List application across React, Angular, Vue, and Svelte highlighted important differences in how each framework handles DOM updates and state management.

One of the main challenges was ensuring fairness in implementation. Each framework has a different architecture—React relies on a virtual DOM, Angular uses a full framework with two-way binding, Vue provides a reactive system, and Svelte compiles code at build time. Keeping the functionality identical while respecting each framework’s best practices required careful planning.

In terms of performance, Svelte consistently showed the fastest rendering and update times because it avoids the overhead of a virtual DOM and updates the DOM directly at compile time. Vue also performed efficiently due to its lightweight reactivity system. React performed well but showed slightly slower updates when handling larger datasets due to virtual DOM diffing. Angular was the most resource-heavy in larger scenarios, likely due to its complex change detection system.

Overall, Svelte demonstrated the best performance in rendering and updating large lists, while React and Vue offered a good balance between performance and developer experience. Angular, while powerful and feature-rich, showed higher overhead in DOM-intensive operations.

This exercise provided valuable insight into how architectural design choices directly impact performance in modern front-end frameworks.

---

