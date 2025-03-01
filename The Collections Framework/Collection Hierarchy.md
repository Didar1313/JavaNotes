### ** Collection Interface Hierarchy**
The **Collections Framework** in Java has a structured hierarchy of interfaces and classes. At the top, we have the `Collection` interface, which is extended by `List`, `Set`, and others.

---

### **1. Avoiding Getting Lost in the Collection Hierarchy**

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

### **3. Storing Elements in a Container with the Collection Interface)**
The `Collection` interface provides basic functionalities like:
- **Adding & Removing Elements**
- **Checking if an Element Exists**
- **Getting the Size of the Collection**
- **Performing Set Operations** (union, intersection, complement)
- **Iterating Over Elements**
  ```java
  Collection<String> collection = new ArrayList<>();
  collection.add("Apple");     // Add element
  collection.remove("Apple");  // Remove element
  System.out.println(collection.contains("Apple"));  // Check existence
  System.out.println(collection.size());  // Get size
  collection.clear();  // Remove all elements
  ```

---

### **4. Extending Collection with List**
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

