# DSA - Java

## ArrayList
```java
import java.util.ArrayList;

ArrayList<String> bikes = new ArrayList<String>();

bikes.add("Pulsar");    // Add an element
bikes.add(1, "Yamaha")  // Add in particular index
bikes.get(0);           // Access an element
bikes.set(0, "KTM");    // Change an item
bikes.remove(0);        // Remove an item
bikes.clear();          // Remove all items
bikes.size();           // length of arraylist
bikes.contains("KTM")   // Check if exists

System.out.println(bikes)   // printing list
Collections.sort(bikes);    // sort the list
```

## Stacks
```java
// Stack<type> s1 = new Stack<>();
// Stack s2 = new Stack();

Stack<Integer> s1 = new Stack<>();

s1.push(98);
s1.empty();       // false
s1.peek();        // top - 98
s1.search(98);    // index - 0
s1.pop();         
s1.size();
```

## Queues
```java
// LinkedList implementation of Queue
Queue<String> animal1 = new LinkedList<>();

// Array implementation of Queue
Queue<String> animal2 = new ArrayDeque<>();

// Priority Queue implementation of Queue
Queue<String> animal 3 = new PriorityQueue<>();
```
