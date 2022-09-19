## Big O of JS Arrays

- Use when you need order
- When you need fast access / insertion and removal 

**Insertion** - it depends. Pushing to the end is **O(n)**
**Removal** - it depends. Removing from the end is   **O(n)**
**Searching** - **O(n)**
**Access**  - **O(1)**

Array methods:

- `.push` and `.pop` are **O(1)**

- most of other array methods are **O(n)**
- `_.sort()_` is **O(n * log N)**