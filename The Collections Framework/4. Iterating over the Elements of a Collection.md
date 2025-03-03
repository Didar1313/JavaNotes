### **Iterating Over a Collection in Java (Simple Explanation)**  

When working with collections like lists or sets in Java, you often need to go through each item one by one. There are different ways to do this, depending on what you want to achieve.  

---

### **1. Using for-each Loop (Best for Reading Data)**  
If you just want to look at each element and do something with it (like printing it), the **for-each loop** is the easiest way.  

🔹 **Why?** Simple and readable, but you **can't remove** elements while iterating.  

🔹 **How?** The loop automatically picks each item from the collection one by one.  

```java
Collection<String> strings = List.of("one", "two", "three");
for (String element : strings) {
    System.out.println(element);
}
```

✅ **Best for:** Just reading or processing items.  

---

### **2. Using Iterator (When You Need More Control)**  
If you need to **remove elements while looping**, a simple for-each won't work. Instead, use an **Iterator**.  

🔹 **Why?** The `Iterator` allows you to safely remove elements while iterating.  

🔹 **How?** You first check if there are more elements (`hasNext()`) left, then get the next one (`next()`), and optionally remove it (`remove()`).  

```java
Collection<String> strings = new ArrayList<>(List.of("one", "two", "three"));
Iterator<String> iterator = strings.iterator();
while (iterator.hasNext()) {
    String element = iterator.next();
    if (element.length() == 3) {  // Remove words with 3 letters
        iterator.remove();
    }
}
```

✅ **Best for:** When you need to modify (remove) elements while iterating.  

---

### **3. Using removeIf() (Shortcut for Removing Items)**  
Instead of using an `Iterator`, Java provides a simpler way: `removeIf()`.  

🔹 **Why?** It removes items **in one line** without needing an iterator.  

🔹 **How?** Just provide a condition, and Java removes matching elements.  

```java
Collection<String> strings = new ArrayList<>(List.of("one", "two", "three"));
strings.removeIf(s -> s.length() == 3);
```

✅ **Best for:** Quick and clean removal of elements based on a condition.  

---

### **4. Creating a Custom Iterable (For Custom Iteration Needs)**  
Sometimes, you need to loop over a **range of numbers** or custom objects. You can create a **class that behaves like a collection** by implementing the `Iterable` interface.  

🔹 **Why?** If Java's built-in collections don't fit your needs, you can define how iteration should work.  

🔹 **How?** Define a class that implements `Iterable<T>`, and provide an `Iterator`.  

Example: A **Range class** that lets you loop over numbers from `start` to `end`:  

```java
class Range implements Iterable<Integer> {
    private final int start, end;
    public Range(int start, int end) { this.start = start; this.end = end; }

    @Override
    public Iterator<Integer> iterator() {
        return new Iterator<>() {
            private int index = start;
            public boolean hasNext() { return index < end; }
            public Integer next() { return hasNext() ? index++ : throw new NoSuchElementException(); }
        };
    }
}
```
✅ **Best for:** When you need a **custom** looping structure.  

---

### **Summary (When to Use What?)**  

| Method            | Use Case |
|------------------|---------|
| **for-each** | Best for reading elements easily. |
| **Iterator** | Use when modifying while looping (removing elements). |
| **removeIf()** | Best for simple removal with one line of code. |
| **Custom Iterable** | Use if you need special looping behavior. |
