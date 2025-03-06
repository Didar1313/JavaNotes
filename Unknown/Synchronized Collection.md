### **What is a Synchronized Collection?**  

A **synchronized collection** is a thread-safe version of a collection (List, Set, or Map) where multiple threads can access it **without causing data inconsistency or corruption**.  

### **How It Works?**  
- The collection is wrapped with a synchronized version using `Collections.synchronizedXXX()`.  
- Internally, all methods are synchronized to ensure only **one thread can modify/access** the collection at a time.  

### **Example:**  
```java
List<String> syncList = Collections.synchronizedList(new ArrayList<>());

syncList.add("Apple");
syncList.add("Banana");
```
### **Precaution When Iterating:**  
Since iteration is **not automatically synchronized**, you need to manually **synchronize the block**:  
```java
synchronized(syncList) {
    for (String item : syncList) {
        System.out.println(item);
    }
}
```

### **Better Alternatives?**  
Synchronized collections are **not always the best choice**.  
For multi-threaded environments, use **concurrent collections** instead:  
- `CopyOnWriteArrayList` (for lists)  
- `ConcurrentHashMap` (for maps)  
- `ConcurrentLinkedQueue` (for queues)  

These are **faster and more efficient** than synchronized wrappers. 🚀
