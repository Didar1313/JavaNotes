### Storing Data Using the Collections Framework  

The **Collections Framework** is a key part of Java that provides efficient ways to store and manage data in memory. It was introduced in **Java SE 2 (1998)** and improved in **Java SE 5 (with generics)** and **Java 8 (with lambda expressions and default methods).**  

### Key Concepts:  
1. **Interfaces & Implementations** – The framework provides interfaces (like `List`, `Set`, `Map`) and their implementations (`ArrayList`, `HashMap`, etc.).  
2. **Main Categories:**  
   - **Collections** (store and iterate over objects)  
   - **Maps** (store key-value pairs)  
   - **Queues & Stacks** (manage elements in a specific order)  
   - **Iterators** (traverse collections)  

### Choosing the Right Collection:  
- **List (`ArrayList`, `LinkedList`)** – Stores ordered elements, allows duplicates.  
- **Set (`HashSet`, `TreeSet`)** – Stores unique elements.  
- **Queue (`PriorityQueue`, `ArrayDeque`)** – Follows FIFO (First-In-First-Out).  
- **Map (`HashMap`, `TreeMap`)** – Stores key-value pairs for fast lookups.  

### Avoid Using Old Classes:  
- **`Vector` & `Stack`** → Use `ArrayList` & `ArrayDeque` instead.  
- **`Hashtable`** → Use `HashMap` or `ConcurrentHashMap`.  

### Why Use Collections Over Arrays?  
- Collections **automatically resize**, track the number of elements, and support powerful operations like searching, sorting, and merging.  
- Arrays are **fixed in size** and lack built-in utilities for managing data efficiently.  

Using the **right collection** improves performance and makes Java applications more scalable and maintainable! 🚀
