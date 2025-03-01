### **1. Collection Interface Hierarchy**
The **Collections Framework** in Java has a structured hierarchy of interfaces and classes. At the top, we have the `Collection` interface, which is extended by `List`, `Set`, and others.

---

### **2. Iterable Interface**
- The `Iterable` interface is not part of the Collections Framework but is important because all collections implement it.
- It allows objects to be iterated using a `for-each` loop:
  ```java
  for (String element : collection) {
      // Do something with element
  }
  ```
- It requires implementing an `Iterator`.

---

### **3. Collection Interface (Core Operations)**
The `Collection` interface provides basic functionalities like:
- **Adding & Removing Elements**
- **Checking if an Element Exists**
- **Getting the Size of the Collection**
- **Performing Set Operations** (union, intersection, complement)
- **Iterating Over Elements**

---

### **4. List Interface (Ordered Collection)**
- A `List` maintains the order of elements as they were added.
- **Indexes** are used to access elements.
- Key operations include:
  - Get an element by index
  - Insert, update, or delete elements at a specific position
  - Extract a sublist

---

### **5. Set Interface (Unique Elements)**
- A `Set` does **not allow duplicate elements**.
- Adding an element may fail if it already exists.
- Unlike `List`, elements in a `Set` do not have an index.

---

### **6. SortedSet & NavigableSet (Ordered Sets)**
- **`SortedSet`**: Maintains elements in sorted order (ascending).
- Sorting is based on:
  - The `Comparable` interface (`compareTo()` method)
  - A custom `Comparator`
- Additional operations:
  - Get the **smallest** and **largest** elements
  - Extract subsets (headSet, tailSet)
  - Iterate from smallest to largest

- **`NavigableSet`** (Extends `SortedSet`):
  - Adds more methods like **reverse iteration** (descending order).

---

### **7. Sorting vs Ordering**
- **Sorting**: Elements are arranged in order based on a comparison logic (`SortedSet`).
- **Ordering**: Elements remain in the order they were added (`List`).

Let me know if you need further clarification! 🚀
