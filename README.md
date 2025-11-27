# Data Structures and Algorithms in C++

> “Talk is cheap. Show me the time complexity.”

- Author: [Kintsugi-Programmer](https://github.com/kintsugi-programmer)

![alt text](image.png)

> Disclaimer: The content presented here is a curated blend of my personal learning journey, experiences, open-source documentation, and invaluable knowledge gained from diverse sources. I do not claim sole ownership over all the material; this is a community-driven effort to learn, share, and grow together.

## Table of Contents
- [Data Structures and Algorithms in C++](#data-structures-and-algorithms-in-c)
  - [Table of Contents](#table-of-contents)
- [Basics to Intermediate Data Structures and Algorithms in C++](#basics-to-intermediate-data-structures-and-algorithms-in-c)
  - [Introduction](#introduction)
    - [What is a Data Structure?](#what-is-a-data-structure)
    - [What is an Algorithm?](#what-is-an-algorithm)
    - [Why Learn Data Structures and Algorithms?](#why-learn-data-structures-and-algorithms)
  - [Data Structures](#data-structures)
    - [Stack (LIFO - Last In First Out)](#stack-lifo---last-in-first-out)
      - [Stack Operations:](#stack-operations)
      - [Stack Implementation in C++:](#stack-implementation-in-c)
      - [Stack Methods:](#stack-methods)
      - [Real-World Uses of Stacks:](#real-world-uses-of-stacks)
    - [Queue (FIFO - First In First Out)](#queue-fifo---first-in-first-out)
      - [Queue Operations:](#queue-operations)
      - [Queue Implementation in C++:](#queue-implementation-in-c)
      - [Queue Methods:](#queue-methods)
      - [Real-World Uses of Queues:](#real-world-uses-of-queues)
    - [Priority Queue](#priority-queue)
      - [Priority Queue Implementation in C++:](#priority-queue-implementation-in-c)
      - [Real-World Applications:](#real-world-applications)
    - [Linked List](#linked-list)
      - [Linked List Node Structure:](#linked-list-node-structure)
      - [Singly Linked List Implementation:](#singly-linked-list-implementation)
      - [Advantages of Linked Lists:](#advantages-of-linked-lists)
      - [Disadvantages of Linked Lists:](#disadvantages-of-linked-lists)
    - [Dynamic Array (Vector)](#dynamic-array-vector)
      - [Vector Implementation in C++:](#vector-implementation-in-c)
      - [Custom Dynamic Array Implementation:](#custom-dynamic-array-implementation)
      - [Operations Time Complexity:](#operations-time-complexity)
  - [Algorithms](#algorithms)
    - [Big O Notation](#big-o-notation)
      - [Common Big O Complexities (Best to Worst):](#common-big-o-complexities-best-to-worst)
  - [Search Algorithms](#search-algorithms)
    - [Linear Search](#linear-search)
      - [Implementation:](#implementation)
      - [Characteristics:](#characteristics)
    - [Binary Search](#binary-search)
      - [Implementation:](#implementation-1)
      - [Characteristics:](#characteristics-1)
  - [Sorting Algorithms](#sorting-algorithms)
    - [Bubble Sort](#bubble-sort)
      - [Implementation:](#implementation-2)
      - [Characteristics:](#characteristics-2)
    - [Selection Sort](#selection-sort)
      - [Implementation:](#implementation-3)
      - [Characteristics:](#characteristics-3)
    - [Quick Sort](#quick-sort)
      - [Implementation:](#implementation-4)
      - [Characteristics:](#characteristics-4)
    - [Merge Sort](#merge-sort)
      - [Implementation:](#implementation-5)
      - [Characteristics:](#characteristics-5)
  - [Advanced Data Structures](#advanced-data-structures)
    - [Graph](#graph)
      - [Adjacency List Implementation:](#adjacency-list-implementation)
    - [Binary Search Tree (BST)](#binary-search-tree-bst)
      - [Implementation:](#implementation-6)
      - [BST Time Complexities:](#bst-time-complexities)
  - [Conclusion](#conclusion)
  - [Quick Reference: Time Complexities](#quick-reference-time-complexities)
    - [Data Structures Access Patterns:](#data-structures-access-patterns)
    - [Sorting Algorithms Comparison:](#sorting-algorithms-comparison)
- [Advanced Data Structures and Algorithms in C++](#advanced-data-structures-and-algorithms-in-c)
  - [Hash Table / Unordered Map / Unordered Set](#hash-table--unordered-map--unordered-set)
    - [Concepts](#concepts)
      - [Key Terminology:](#key-terminology)
    - [C++ STL Implementation (Recommended)](#c-stl-implementation-recommended)
    - [Custom Hash Table Implementation](#custom-hash-table-implementation)
    - [Common Interview Problems](#common-interview-problems)
    - [Time Complexities (Hash Tables)](#time-complexities-hash-tables)
  - [Heaps (Min Heap \& Max Heap)](#heaps-min-heap--max-heap)
    - [Heap Properties](#heap-properties)
      - [Key Operations:](#key-operations)
    - [Min Heap Implementation](#min-heap-implementation)
    - [Max Heap Implementation](#max-heap-implementation)
  - [Balanced Trees (AVL \& Red-Black Trees)](#balanced-trees-avl--red-black-trees)
    - [AVL Tree Concepts](#avl-tree-concepts)
      - [Balance Factor:](#balance-factor)
      - [Rotations:](#rotations)
    - [AVL Tree Implementation](#avl-tree-implementation)
    - [Red-Black Tree Concepts](#red-black-tree-concepts)
  - [Trie (Prefix Tree)](#trie-prefix-tree)
    - [Trie Node Structure](#trie-node-structure)
    - [Common Trie Problems](#common-trie-problems)
  - [Disjoint Set Union (Union-Find / DSU)](#disjoint-set-union-union-find--dsu)
    - [Union-Find Implementation](#union-find-implementation)
    - [DSU Applications](#dsu-applications)
  - [Heap Sort](#heap-sort)
    - [Time Complexities (Heap Sort)](#time-complexities-heap-sort)
  - [Two-Pointer Techniques](#two-pointer-techniques)
  - [Sliding Window](#sliding-window)
  - [Backtracking](#backtracking)
  - [Dynamic Programming](#dynamic-programming)
  - [Advanced Graph Algorithms](#advanced-graph-algorithms)
    - [Dijkstra's Algorithm](#dijkstras-algorithm)
    - [Prim's Algorithm (MST)](#prims-algorithm-mst)
    - [Topological Sort (Kahn's Algorithm)](#topological-sort-kahns-algorithm)
    - [Floyd-Warshall Algorithm](#floyd-warshall-algorithm)
  - [Segment Tree](#segment-tree)
  - [Time Complexity Summary Table](#time-complexity-summary-table)
  - [Key Interview Takeaways](#key-interview-takeaways)

---

# Basics to Intermediate Data Structures and Algorithms in C++

---

## Introduction

### What is a Data Structure?

- **data structure** is a named location that can be used to store and organize da It's a way to manage and structure information efficiently.

**Real-life Example:**
- A family tree is a data structure that represents a hierarchy of family relationships
- Arrays are collections of elements stored at contiguous memory locations
- Trees organize data hierarchically

**Key Concept:** Different data structures store and organize data in different ways, each with their own advantages and disadvantages.

### What is an Algorithm?

An **algorithm** is a collection of steps to solve a probl It's a set of instructions to reach a solution.

### Why Learn Data Structures and Algorithms?
 Write code that is both **time and memory efficient** **Commonly asked questions** in coding job interviews Improve problem-solving skills in technical assessments

---

## Data Structures

### Stack (LIFO - Last In First Out)

A **stack** is a LIFO data structure that stores objects in a vertical tower-like structure, similar to a stack of books or CDs.

#### Stack Operations:
- **Push:** Add an object to the top of the stack
- **Pop:** Remove an object from the top of the stack
- **Peek:** View the object at the top without removing it
- **Empty:** Check if the stack is empty
- **Size:** Get the number of elements

#### Stack Implementation in C++:

```cpp
#include <iostream>
#include <stack>
#include <string>

using namespace std;

int main() {
    stack<string> gameStack;
    
    // Push elements
    gameStack.push("Minecraft");
    gameStack.push("Skyrim");
    gameStack.push("Doom");
    gameStack.push("Borderlands");
    gameStack.push("Final Fantasy VII");
    
    // Check if empty
    cout << "Empty: " << (gameStack.empty() ? "true" : "false") << endl; // false
    
    // Get size
    cout << "Size: " << gameStack.size() << endl; // 5
    
    // Pop element (removes and returns)
    string game = gameStack.top(); // Returns "Final Fantasy VII"
    cout << "Top: " << game << endl;
    gameStack.pop();
    
    // Peek at top element (view without removing)
    cout << "New top: " << gameStack.top() << endl; // Borderlands
    
    // Print all elements by popping
    while (!gameStack.empty()) {
        cout << gameStack.top() << " ";
        gameStack.pop();
    }
    cout << endl;
    
    return 0;
}
```

#### Stack Methods:
| Method | Description | Returns |
|--------|-------------|---------| 
| `push(E)` | Add element to top | void |
| `pop()` | Remove top element | void |
| `top()` | View top element | Element |
| `empty()` | Check if stack is empty | bool |
| `size()` | Get number of elements | size_t |

#### Real-World Uses of Stacks:
- **Undo/Redo Features** - Text editors use stacks to track changes
- **Browser History** - Back button navigation
- **Backtracking Algorithms** - Maze navigation, file directory searches
- **Function Calls** - Call stack in programming languages

---

### Queue (FIFO - First In First Out)

A- **queue** is a FIFO data structure designed for holding elements prior to processing.

#### Queue Operations:
- **Push/Enqueue:** Add an element to the back/end of the queue
- **Pop/Dequeue:** Remove an element from the front of the queue
- **Front:** Examine the front element without removing it
- **Empty:** Check if the queue is empty
- **Size:** Get the number of elements

#### Queue Implementation in C++:

```cpp
#include <iostream>
#include <queue>
#include <string>

using namespace std;

int main() {
    queue<string> peopleQueue;
    
    // Enqueue (add to back)
    peopleQueue.push("Karen");
    peopleQueue.push("Chad");
    peopleQueue.push("Steve");
    peopleQueue.push("Harold");
    
    // Display front
    cout << "Front: " << peopleQueue.front() << endl; // Karen
    
    // Dequeue (remove from front)
    peopleQueue.pop(); // Karen removed
    cout << "Front after pop: " << peopleQueue.front() << endl; // Chad
    
    // Check if empty
    cout << "Empty: " << (peopleQueue.empty() ? "true" : "false") << endl; // false
    
    // Get size
    cout << "Size: " << peopleQueue.size() << endl; // 3
    
    // Print all elements by dequeuing
    while (!peopleQueue.empty()) {
        cout << peopleQueue.front() << " ";
        peopleQueue.pop();
    }
    cout << endl;
    
    return 0;
}
```

#### Queue Methods:
| Method | Description | Returns |
|--------|-------------|---------| 
| `push(E)` | Add element to back | void |
| `pop()` | Remove and return front | void |
| `front()` | View front element | Element |
| `back()` | View back element | Element |
| `empty()` | Check if queue is empty | bool |
| `size()` | Get number of elements | size_t |

#### Real-World Uses of Queues:
- **Keyboard Buffers** - Characters typed are processed in order
- **Printer Queues** - Print jobs completed in order
- **Breadth-First Search (BFS)** - Graph traversal algorithm
- **Process Scheduling** - Operating systems

---

### Priority Queue

A **priority queue** is a queue where elements are served based on their priority rather than simple FIFO order.

#### Priority Queue Implementation in C++:

```cpp
#include <iostream>
#include <queue>

using namespace std;

int main() {
    // Default - max-heap (largest first)
    priority_queue<double> pQueue;
    
    pQueue.push(3.0);
    pQueue.push(2.5);
    pQueue.push(4.0);
    pQueue.push(1.5);
    pQueue.push(2.0);
    
    // Popping returns elements in descending order
    while (!pQueue.empty()) {
        cout << pQueue.top() << " ";
        pQueue.pop();
    }
    cout << endl; // Output: 4 3 2.5 2 1.5
    
    // For ascending order (min-heap)
    priority_queue<double, vector<double>, greater<double>> minPQueue;
    
    minPQueue.push(3.0);
    minPQueue.push(2.5);
    minPQueue.push(4.0);
    
    while (!minPQueue.empty()) {
        cout << minPQueue.top() << " ";
        minPQueue.pop();
    }
    cout << endl; // Output: 1.5 2 2.5 3 4
    
    return 0;
}
```

#### Real-World Applications:
- Task scheduling with priority levels
- Dijkstra's shortest path algorithm
- Huffman coding
- Load balancing in systems

---

### Linked List

A **linked list** is a data structure consisting of a chain of nod Each node contains data and a pointer to the next node.

#### Linked List Node Structure:

```cpp
template <typename T>
struct Node {
    T data;
    Node* next;
    
    Node(T value) : data(value), next(nullptr) {}
};

template <typename T>
struct DoublyNode {
    T data;
    DoublyNode* next;
    DoublyNode* prev;
    
    DoublyNode(T value) : data(value), next(nullptr), prev(nullptr) {}
};
```

#### Singly Linked List Implementation:

```cpp
#include <iostream>
using namespace std;

template <typename T>
struct Node {
    T data;
    Node* next;
    Node(T value) : data(value), next(nullptr) {}
};

template <typename T>
class SinglyLinkedList {
private:
    Node<T>* head;
    
public:
    SinglyLinkedList() : head(nullptr) {}
    
    // Add to front
    void addFront(T value) {
        Node<T>* newNode = new Node<T>(value);
        newNode->next = head;
        head = newNode;
    }
    
    // Add to end
    void addEnd(T value) {
        Node<T>* newNode = new Node<T>(value);
        if (head == nullptr) {
            head = newNode;
            return;
        }
        
        Node<T>* current = head;
        while (current->next != nullptr) {
            current = current->next;
        }
        current->next = newNode;
    }
    
    // Insert at specific position
    void insertAt(int position, T value) {
        if (position == 0) {
            addFront(value);
            return;
        }
        
        Node<T>* current = head;
        for (int i = 0; i < position - 1 && current != nullptr; i++) {
            current = current->next;
        }
        
        if (current == nullptr) return;
        
        Node<T>* newNode = new Node<T>(value);
        newNode->next = current->next;
        current->next = newNode;
    }
    
    // Remove from front
    void removeFront() {
        if (head == nullptr) return;
        Node<T>* temp = head;
        head = head->next;
        delete temp;
    }
    
    // Remove specific element
    void remove(T value) {
        if (head == nullptr) return;
        
        if (head->data == value) {
            Node<T>* temp = head;
            head = head->next;
            delete temp;
            return;
        }
        
        Node<T>* current = head;
        while (current->next != nullptr) {
            if (current->next->data == value) {
                Node<T>* temp = current->next;
                current->next = current->next->next;
                delete temp;
                return;
            }
            current = current->next;
        }
    }
    
    // Search for element
    int search(T value) {
        Node<T>* current = head;
        int position = 0;
        
        while (current != nullptr) {
            if (current->data == value) {
                return position;
            }
            current = current->next;
            position++;
        }
        return -1; // Not found
    }
    
    // Display list
    void display() {
        Node<T>* current = head;
        while (current != nullptr) {
            cout << current->data << " -> ";
            current = current->next;
        }
        cout << "nullptr" << endl;
    }
    
    // Check if empty
    bool isEmpty() {
        return head == nullptr;
    }
    
    // Destructor
    ~SinglyLinkedList() {
        while (head != nullptr) {
            removeFront();
        }
    }
};

int main() {
    SinglyLinkedList<string> list;
    
    list.addFront("C");
    list.addFront("B");
    list.addFront("A");
    list.addEnd("D");
    list.addEnd("E");
    
    list.display(); // A -> B -> C -> D -> E -> nullptr
    
    cout << "Search B: " << list.search("B") << endl; // 1
    cout << "Search Z: " << list.search("Z") << endl; // -1
    
    list.insertAt(2, "X");
    list.display(); // A -> B -> X -> C -> D -> E -> nullptr
    
    list.remove("X");
    list.display(); // A -> B -> C -> D -> E -> nullptr
    
    return 0;
}
```

#### Advantages of Linked Lists:
- **Dynamic data structure** - Allocates memory during runtime
- **Easy insertion/deletion** - O(1) constant time (no shifting)
- **No memory waste** - Uses only what's needed

#### Disadvantages of Linked Lists:
- **Greater memory usage** - Must store additional pointers
- **No random access** - Must traverse from head
- **Slow searching** - O(n) linear time

---

### Dynamic Array (Vector)

A **dynamic array** is an array with resizable capaci In C++, this is represented by `vector`.

#### Vector Implementation in C++:

```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<string> vec;
    
    // Add elements
    vec.push_back("A");
    vec.push_back("B");
    vec.push_back("C");
    
    // Insert at specific index
    vec.insert(vec.begin(), "X"); // Insert X at index 0
    
    // Remove element
    vec.erase(vec.begin()); // Remove first element
    vec.erase(vec.begin() + 1); // Remove at index 1
    
    // Access by index
    cout << "First: " << vec[0] << endl;
    cout << "Last: " << vec[vec.size() - 1] << endl;
    
    // Search
    auto it = find(vec.begin(), vec.end(), "B");
    if (it != vec.end()) {
        cout << "Found at index: " << distance(vec.begin(), it) << endl;
    }
    
    // Get size and capacity
    cout << "Size: " << vec.size() << endl;
    cout << "Capacity: " << vec.capacity() << endl;
    
    // Display
    for (const auto& element : vec) {
        cout << element << " ";
    }
    cout << endl;
    
    return 0;
}
```

#### Custom Dynamic Array Implementation:

```cpp
#include <iostream>
using namespace std;

template <typename T>
class DynamicArray {
private:
    T* array;
    int size;
    int capacity;
    
    void grow() {
        int newCapacity = capacity * 2;
        T* newArray = new T[newCapacity];
        
        for (int i = 0; i < size; i++) {
            newArray[i] = array[i];
        }
        
        delete[] array;
        array = newArray;
        capacity = newCapacity;
    }
    
    void shrink() {
        int newCapacity = capacity / 2;
        T* newArray = new T[newCapacity];
        
        for (int i = 0; i < size; i++) {
            newArray[i] = array[i];
        }
        
        delete[] array;
        array = newArray;
        capacity = newCapacity;
    }
    
public:
    DynamicArray(int initialCapacity = 10) 
        : capacity(initialCapacity), size(0) {
        array = new T[capacity];
    }
    
    // Add element
    void add(T data) {
        if (size >= capacity) {
            grow();
        }
        array[size] = data;
        size++;
    }
    
    // Insert at specific index
    void insert(int index, T data) {
        if (size >= capacity) {
            grow();
        }
        
        for (int i = size - 1; i >= index; i--) {
            array[i + 1] = array[i];
        }
        
        array[index] = data;
        size++;
    }
    
    // Delete element
    void deleteElement(T data) {
        for (int i = 0; i < size; i++) {
            if (array[i] == data) {
                for (int j = i; j < size - 1; j++) {
                    array[j] = array[j + 1];
                }
                size--;
                
                if (size <= capacity / 3) {
                    shrink();
                }
                break;
            }
        }
    }
    
    // Get element at index
    T get(int index) {
        if (index >= 0 && index < size) {
            return array[index];
        }
        throw out_of_range("Index out of bounds");
    }
    
    // Search for element
    int search(T data) {
        for (int i = 0; i < size; i++) {
            if (array[i] == data) {
                return i;
            }
        }
        return -1;
    }
    
    // Check if empty
    bool isEmpty() {
        return size == 0;
    }
    
    // Get size
    int getSize() {
        return size;
    }
    
    // Get capacity
    int getCapacity() {
        return capacity;
    }
    
    // Display
    void display() {
        cout << "[";
        for (int i = 0; i < size; i++) {
            cout << array[i];
            if (i < size - 1) cout << ", ";
        }
        cout << "]" << endl;
    }
    
    // Destructor
    ~DynamicArray() {
        delete[] array;
    }
};

int main() {
    DynamicArray<int> arr;
    
    arr.add(10);
    arr.add(20);
    arr.add(30);
    arr.add(40);
    
    arr.display(); // [10, 20, 30, 40]
    
    arr.insert(2, 25);
    arr.display(); // [10, 20, 25, 30, 40]
    
    cout << "Search 25: " << arr.search(25) << endl; // 2
    
    arr.deleteElement(25);
    arr.display(); // [10, 20, 30, 40]
    
    return 0;
}
```

#### Operations Time Complexity:
| Operation | Time Complexity |
|-----------|-----------------| 
| Random access (by index) | O(1) |
| Search | O(n) |
| Insert at end | O(1) - amortized |
| Insert at beginning | O(n) - requires shifting |
| Delete | O(n) - requires shifting |

---

## Algorithms

### Big O Notation

**Definition:** A notation that describes the performance of an algorithm as the amount of data increases.

#### Common Big O Complexities (Best to Worst):
| Complexity | Name | Example |
|-----------|------|---------| 
| O(1) | Constant | Accessing array element by index |
| O(log n) | Logarithmic | Binary search |
| O(n) | Linear | Loop through array |
| O(n log n) | Quasi-linear | Quick sort, merge sort |
| O(n²) | Quadratic | Bubble sort, nested loops |
| O(2ⁿ) | Exponential | Recursive fibonacci |
| O(n!) | Factorial | Permutations |

---

## Search Algorithms

### Linear Search

**Definition:** An algorithm that checks each element sequentially until the target is found.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

int linearSearch(const vector<int>& array, int value) {
    for (int i = 0; i < array.size(); i++) {
        if (array[i] == value) {
            return i; // Element found
        }
    }
    return -1; // Element not found
}

int main() {
    vector<int> array = {5, 2, 8, 1, 9, 3, 7};
    
    int index = linearSearch(array, 1);
    
    if (index != -1) {
        cout << "Element found at index: " << index << endl;
    } else {
        cout << "Element not found" << endl;
    }
    
    return 0;
}
```

#### Characteristics:
- Time Complexity: **O(n)**
- Works with **unsorted data**
- Simple to implement

---

### Binary Search

**Definition:** An algorithm that eliminates half of the remaining elements with each comparis Only works on **sorted data**.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

int binarySearch(const vector<int>& array, int target) {
    int low = 0;
    int high = array.size() - 1;
    
    while (low <= high) {
        int middle = low + (high - low) / 2;
        int value = array[middle];
        
        if (value == target) {
            return middle; // Found
        } else if (value < target) {
            low = middle + 1; // Search right
        } else {
            high = middle - 1; // Search left
        }
    }
    
    return -1; // Not found
}

// Recursive implementation
int binarySearchRecursive(const vector<int>& array, int target, int low, int high) {
    if (low > high) {
        return -1; // Not found
    }
    
    int middle = low + (high - low) / 2;
    
    if (array[middle] == target) {
        return middle;
    } else if (array[middle] < target) {
        return binarySearchRecursive(array, target, middle + 1, high);
    } else {
        return binarySearchRecursive(array, target, low, middle - 1);
    }
}

int main() {
    vector<int> array = {1, 3, 5, 7, 9, 11, 13, 15, 17, 19};
    
    int index = binarySearch(array, 7);
    
    if (index != -1) {
        cout << "Element found at index: " << index << endl;
    } else {
        cout << "Element not found" << endl;
    }
    
    return 0;
}
```

#### Characteristics:
- Time Complexity: **O(log n)**
- **MUST be sorted**
- **Much faster** for large datasets

---

## Sorting Algorithms

### Bubble Sort

**Definition:** A sorting algorithm that repeatedly compares adjacent elements and swaps them if they're in the wrong order.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

void bubbleSort(vector<int>& array) {
    for (int i = 0; i < array.size() - 1; i++) {
        for (int j = 0; j < array.size() - i - 1; j++) {
            if (array[j] > array[j + 1]) {
                // Swap
                int temp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = temp;
            }
        }
    }
}

// For descending order
void bubbleSortDescending(vector<int>& array) {
    for (int i = 0; i < array.size() - 1; i++) {
        for (int j = 0; j < array.size() - i - 1; j++) {
            if (array[j] < array[j + 1]) { // Changed operator
                // Swap
                int temp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = temp;
            }
        }
    }
}

void display(const vector<int>& array) {
    for (int element : array) {
        cout << element << " ";
    }
    cout << endl;
}

int main() {
    vector<int> array = {5, 2, 8, 1, 9};
    
    bubbleSort(array);
    
    cout << "Sorted: ";
    display(array); // 1 2 5 8 9
    
    return 0;
}
```

#### Characteristics:
- Time Complexity: **O(n²)**
- Space Complexity: **O(1)** - In-place
- **Simple but inefficient** for large datasets

---

### Selection Sort

**Definition:** A sorting algorithm that repeatedly finds the minimum element and places it at the beginning.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

void selectionSort(vector<int>& array) {
    for (int i = 0; i < array.size() - 1; i++) {
        int minIndex = i;
        
        // Find minimum in remaining array
        for (int j = i + 1; j < array.size(); j++) {
            if (array[j] < array[minIndex]) {
                minIndex = j;
            }
        }
        
        // Swap if needed
        if (minIndex != i) {
            int temp = array[i];
            array[i] = array[minIndex];
            array[minIndex] = temp;
        }
    }
}

void display(const vector<int>& array) {
    for (int element : array) {
        cout << element << " ";
    }
    cout << endl;
}

int main() {
    vector<int> array = {9, 1, 8, 2, 7, 3, 6, 4, 5};
    
    selectionSort(array);
    
    cout << "Sorted: ";
    display(array); // 1 2 3 4 5 6 7 8 9
    
    return 0;
}
```

#### Characteristics:
- Time Complexity: **O(n²)**
- Space Complexity: **O(1)** - In-place
- Minimal number of swaps

---

### Quick Sort

**Definition:** A divide-and-conquer sorting algorithm that partitions the array and recursively sorts sub-arrays.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

int partition(vector<int>& array, int low, int high) {
    int pivot = array[high];
    int i = low - 1;
    
    for (int j = low; j < high; j++) {
        if (array[j] < pivot) {
            i++;
            // Swap
            int temp = array[i];
            array[i] = array[j];
            array[j] = temp;
        }
    }
    
    // Swap pivot to correct position
    int temp = array[i + 1];
    array[i + 1] = array[high];
    array[high] = temp;
    
    return i + 1;
}

void quickSort(vector<int>& array, int low, int high) {
    if (low < high) {
        int pi = partition(array, low, high);
        
        quickSort(array, low, pi - 1);   // Sort left partition
        quickSort(array, pi + 1, high);  // Sort right partition
    }
}

void display(const vector<int>& array) {
    for (int element : array) {
        cout << element << " ";
    }
    cout << endl;
}

int main() {
    vector<int> array = {5, 2, 8, 1, 9, 3, 7};
    
    quickSort(array, 0, array.size() - 1);
    
    cout << "Sorted: ";
    display(array); // 1 2 3 5 7 8 9
    
    return 0;
}
```

#### Characteristics:
- Average Time Complexity: **O(n log n)**
- Worst Case: **O(n²)**
- Space Complexity: **O(log n)** (recursion stack)
- **Very efficient** in practice

---

### Merge Sort

**Definition:** A divide-and-conquer sorting algorithm that divides array in half and recursively merges sorted sub-arrays.

#### Implementation:

```cpp
#include <iostream>
#include <vector>

using namespace std;

void merge(vector<int>& array, int left, int mid, int right) {
    int leftSize = mid - left + 1;
    int rightSize = right - mid;
    
    vector<int> leftArray(leftSize);
    vector<int> rightArray(rightSize);
    
    // Copy data to temp arrays
    for (int i = 0; i < leftSize; i++) {
        leftArray[i] = array[left + i];
    }
    for (int i = 0; i < rightSize; i++) {
        rightArray[i] = array[mid + 1 + i];
    }
    
    // Merge the arrays
    int i = 0, j = 0, k = left;
    
    while (i < leftSize && j < rightSize) {
        if (leftArray[i] <= rightArray[j]) {
            array[k] = leftArray[i];
            i++;
        } else {
            array[k] = rightArray[j];
            j++;
        }
        k++;
    }
    
    // Copy remaining elements
    while (i < leftSize) {
        array[k] = leftArray[i];
        i++;
        k++;
    }
    while (j < rightSize) {
        array[k] = rightArray[j];
        j++;
        k++;
    }
}

void mergeSort(vector<int>& array, int left, int right) {
    if (left < right) {
        int mid = left + (right - left) / 2;
        
        mergeSort(array, left, mid);      // Sort left half
        mergeSort(array, mid + 1, right); // Sort right half
        merge(array, left, mid, right);   // Merge
    }
}

void display(const vector<int>& array) {
    for (int element : array) {
        cout << element << " ";
    }
    cout << endl;
}

int main() {
    vector<int> array = {5, 2, 8, 1, 9, 3, 7};
    
    mergeSort(array, 0, array.size() - 1);
    
    cout << "Sorted: ";
    display(array); // 1 2 3 5 7 8 9
    
    return 0;
}
```

#### Characteristics:
- Time Complexity: **O(n log n)** - Always
- Space Complexity: **O(n)** - Requires extra space
- **Guaranteed** good performance
- **Stable sort**

---

## Advanced Data Structures

### Graph

A **graph** is a collection of nodes (vertices) connected by edges (links).

#### Adjacency List Implementation:

```cpp
#include <iostream>
#include <vector>
#include <queue>

using namespace std;

class Graph {
private:
    int vertices;
    vector<vector<int>> adjacencyList;
    
public:
    Graph(int vertices) {
        this->vertices = vertices;
        adjacencyList.resize(vertices);
    }
    
    // Add edge (undirected)
    void addEdge(int u, int v) {
        adjacencyList[u].push_back(v);
        adjacencyList[v].push_back(u); // For undirected graph
    }
    
    // Add edge (directed)
    void addDirectedEdge(int u, int v) {
        adjacencyList[u].push_back(v);
    }
    
    // Check if edge exists
    bool hasEdge(int u, int v) {
        for (int neighbor : adjacencyList[u]) {
            if (neighbor == v) return true;
        }
        return false;
    }
    
    // Display graph
    void display() {
        for (int i = 0; i < vertices; i++) {
            cout << i << " -> ";
            for (int neighbor : adjacencyList[i]) {
                cout << neighbor << " ";
            }
            cout << endl;
        }
    }
    
    // Depth-First Search
    void dfs(int startVertex) {
        vector<bool> visited(vertices, false);
        dfsHelper(startVertex, visited);
    }
    
private:
    void dfsHelper(int vertex, vector<bool>& visited) {
        if (visited[vertex]) return;
        
        visited[vertex] = true;
        cout << vertex << " ";
        
        for (int neighbor : adjacencyList[vertex]) {
            if (!visited[neighbor]) {
                dfsHelper(neighbor, visited);
            }
        }
    }
    
public:
    // Breadth-First Search
    void bfs(int startVertex) {
        vector<bool> visited(vertices, false);
        queue<int> q;
        
        q.push(startVertex);
        visited[startVertex] = true;
        
        while (!q.empty()) {
            int vertex = q.front();
            q.pop();
            
            cout << vertex << " ";
            
            for (int neighbor : adjacencyList[vertex]) {
                if (!visited[neighbor]) {
                    q.push(neighbor);
                    visited[neighbor] = true;
                }
            }
        }
    }
};

int main() {
    Graph graph(5);
    
    graph.addDirectedEdge(0, 1);
    graph.addDirectedEdge(0, 2);
    graph.addDirectedEdge(1, 3);
    graph.addDirectedEdge(2, 3);
    graph.addDirectedEdge(3, 4);
    
    cout << "Graph:" << endl;
    graph.display();
    
    cout << "\nDFS from 0: ";
    graph.dfs(0);
    cout << endl;
    
    cout << "BFS from 0: ";
    graph.bfs(0);
    cout << endl;
    
    return 0;
}
```

---

### Binary Search Tree (BST)

A **Binary Search Tree** is a binary tree where each node has at most two children, and values follow the BST property.

#### Implementation:

```cpp
#include <iostream>
#include <queue>

using namespace std;

struct Node {
    int data;
    Node* left;
    Node* right;
    
    Node(int value) : data(value), left(nullptr), right(nullptr) {}
};

class BST {
private:
    Node* root;
    
    Node* insertHelper(Node* root, int data) {
        if (root == nullptr) {
            return new Node(data);
        }
        
        if (data < root->data) {
            root->left = insertHelper(root->left, data);
        } else if (data > root->data) {
            root->right = insertHelper(root->right, data);
        }
        
        return root;
    }
    
    bool searchHelper(Node* root, int data) {
        if (root == nullptr) return false;
        
        if (root->data == data) {
            return true;
        } else if (data < root->data) {
            return searchHelper(root->left, data);
        } else {
            return searchHelper(root->right, data);
        }
    }
    
    void inOrderHelper(Node* root) {
        if (root == nullptr) return;
        
        inOrderHelper(root->left);
        cout << root->data << " ";
        inOrderHelper(root->right);
    }
    
    void preOrderHelper(Node* root) {
        if (root == nullptr) return;
        
        cout << root->data << " ";
        preOrderHelper(root->left);
        preOrderHelper(root->right);
    }
    
    void postOrderHelper(Node* root) {
        if (root == nullptr) return;
        
        postOrderHelper(root->left);
        postOrderHelper(root->right);
        cout << root->data << " ";
    }
    
    int findMinHelper(Node* root) {
        while (root->left != nullptr) {
            root = root->left;
        }
        return root->data;
    }
    
    int findMaxHelper(Node* root) {
        while (root->right != nullptr) {
            root = root->right;
        }
        return root->data;
    }
    
    Node* removeHelper(Node* root, int data) {
        if (root == nullptr) return nullptr;
        
        if (data < root->data) {
            root->left = removeHelper(root->left, data);
        } else if (data > root->data) {
            root->right = removeHelper(root->right, data);
        } else {
            // Case 1: Leaf node
            if (root->left == nullptr && root->right == nullptr) {
                delete root;
                return nullptr;
            }
            
            // Case 2: Node has right child
            if (root->right != nullptr) {
                int successor = findMinHelper(root->right);
                root->data = successor;
                root->right = removeHelper(root->right, successor);
            }
            // Case 3: Node has only left child
            else {
                int predecessor = findMaxHelper(root->left);
                root->data = predecessor;
                root->left = removeHelper(root->left, predecessor);
            }
        }
        
        return root;
    }
    
    void deleteTreeHelper(Node* root) {
        if (root == nullptr) return;
        
        deleteTreeHelper(root->left);
        deleteTreeHelper(root->right);
        delete root;
    }
    
public:
    BST() : root(nullptr) {}
    
    void insert(int data) {
        root = insertHelper(root, data);
    }
    
    bool search(int data) {
        return searchHelper(root, data);
    }
    
    void inOrder() {
        inOrderHelper(root);
        cout << endl;
    }
    
    void preOrder() {
        preOrderHelper(root);
        cout << endl;
    }
    
    void postOrder() {
        postOrderHelper(root);
        cout << endl;
    }
    
    int findMin() {
        if (root == nullptr) throw runtime_error("Tree is empty");
        return findMinHelper(root);
    }
    
    int findMax() {
        if (root == nullptr) throw runtime_error("Tree is empty");
        return findMaxHelper(root);
    }
    
    void remove(int data) {
        if (!search(data)) {
            cout << data << " could not be found" << endl;
            return;
        }
        root = removeHelper(root, data);
    }
    
    ~BST() {
        deleteTreeHelper(root);
    }
};

int main() {
    BST bst;
    
    bst.insert(50);
    bst.insert(30);
    bst.insert(70);
    bst.insert(20);
    bst.insert(40);
    bst.insert(60);
    bst.insert(80);
    
    cout << "In-Order (sorted): ";
    bst.inOrder();
    
    cout << "Pre-Order: ";
    bst.preOrder();
    
    cout << "Post-Order: ";
    bst.postOrder();
    
    cout << "Min: " << bst.findMin() << endl;
    cout << "Max: " << bst.findMax() << endl;
    
    cout << "Search 40: " << (bst.search(40) ? "Found" : "Not found") << endl;
    
    bst.remove(20);
    cout << "After removing 20 - In-Order: ";
    bst.inOrder();
    
    return 0;
}
```

#### BST Time Complexities:
| Operation | Average | Worst Case |
|-----------|---------|-----------| 
| Search | O(log n) | O(n) |
| Insert | O(log n) | O(n) |
| Delete | O(log n) | O(n) |
| Traversal | O(n) | O(n) |

---

## Conclusion

This comprehensive C++ guide covers fundamental data structures and algorithms equivalent to the Java version.

**Data Structures Covered:**
- Stack (LIFO)
- Queue (FIFO)
- Priority Queue
- Linked List
- Dynamic Array/Vector
- Graph (Adjacency List)
- Binary Search Tree

**Algorithms Covered:**
- Linear Search - O(n)
- Binary Search - O(log n)
- Bubble Sort - O(n²)
- Selection Sort - O(n²)
- Quick Sort - O(n log n)
- Merge Sort - O(n log n)
- Depth-First Search - O(V + E)
- Breadth-First Search - O(V + E)

**Key Takeaways:** Choose the right data structure for your use case Understand time and space complexity Consider whether data needs to be sorted Know when to use each algorithm Practice implementing from scratch to understand deeply

Remember: The best data structure/algorithm depends on your specific problem requirements!

---

## Quick Reference: Time Complexities

### Data Structures Access Patterns:

| Operation | Array | Linked List | BST | Hash Table |
|-----------|-------|-------------|-----|-----------| 
| Access | O(1) | O(n) | O(log n) | O(1) avg |
| Search | O(n) | O(n) | O(log n) | O(1) avg |
| Insert | O(n) | O(1) | O(log n) | O(1) avg |
| Delete | O(n) | O(1) | O(log n) | O(1) avg |

### Sorting Algorithms Comparison:

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------| 
| Bubble | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Selection | O(n²) | O(n²) | O(n²) | O(1) | No |
| Quick | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| Merge | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |

---

# Advanced Data Structures and Algorithms in C++

---

## Hash Table / Unordered Map / Unordered Set

### Concepts

**Hash Table** uses a hash function to map keys to array indices, enabling O(1) average-case lookup.

#### Key Terminology:
- **Hash Function:** Converts key to array index
- **Collision:** Two keys hash to same index
- **Load Factor:** Elements / Array size
- **Rehashing:** Resizing table when load factor exceeds threshold

### C++ STL Implementation (Recommended)

```cpp
#include <iostream>
#include <unordered_map>
#include <unordered_set>
#include <vector>

using namespace std;

int main() {
    // ===== UNORDERED_MAP =====
    unordered_map<string, int> frequencyMap;
    
    // Insert elements
    frequencyMap["apple"] = 3;
    frequencyMap["banana"] = 2;
    frequencyMap["cherry"] = 1;
    
    // Access elements
    cout << "Apple: " << frequencyMap["apple"] << endl;
    
    // Check if key exists
    if (frequencyMap.find("apple") != frequencyMap.end()) {
        cout << "Apple found!" << endl;
    }
    
    // Iterate
    for (auto& pair : frequencyMap) {
        cout << pair.first << ": " << pair.second << endl;
    }
    
    // Count frequency of characters
    string text = "hello world";
    unordered_map<char, int> charFreq;
    for (char c : text) {
        if (c != ' ') {
            charFreq[c]++;
        }
    }
    
    cout << "\nCharacter Frequencies:" << endl;
    for (auto& p : charFreq) {
        cout << p.first << ": " << p.second << endl;
    }
    
    // ===== UNORDERED_SET =====
    unordered_set<int> uniqueNumbers;
    
    vector<int> numbers = {5, 2, 8, 2, 5, 1, 8, 3};
    
    // Insert unique elements
    for (int num : numbers) {
        uniqueNumbers.insert(num);
    }
    
    cout << "\nUnique numbers: ";
    for (int num : uniqueNumbers) {
        cout << num << " ";
    }
    cout << endl;
    
    // Check membership
    cout << "5 exists: " << (uniqueNumbers.count(5) ? "Yes" : "No") << endl;
    
    return 0;
}
```

### Custom Hash Table Implementation

```cpp
#include <iostream>
#include <vector>
#include <list>
#include <utility>

using namespace std;

template <typename K, typename V>
class HashTable {
private:
    static const int TABLE_SIZE = 10;
    vector<list<pair<K, V>>> table;
    
    int hash(K key) {
        return key % TABLE_SIZE;
    }
    
public:
    HashTable() {
        table.resize(TABLE_SIZE);
    }
    
    void insert(K key, V value) {
        int index = hash(key);
        
        // Check if key already exists and update
        for (auto& p : table[index]) {
            if (p.first == key) {
                p.second = value;
                return;
            }
        }
        
        // Insert new key-value pair
        table[index].push_back({key, value});
    }
    
    V get(K key) {
        int index = hash(key);
        
        for (auto& p : table[index]) {
            if (p.first == key) {
                return p.second;
            }
        }
        
        throw runtime_error("Key not found");
    }
    
    bool contains(K key) {
        int index = hash(key);
        
        for (auto& p : table[index]) {
            if (p.first == key) {
                return true;
            }
        }
        
        return false;
    }
    
    void remove(K key) {
        int index = hash(key);
        
        for (auto it = table[index].begin(); it != table[index].end(); ++it) {
            if (it->first == key) {
                table[index].erase(it);
                return;
            }
        }
    }
    
    void display() {
        for (int i = 0; i < TABLE_SIZE; i++) {
            cout << "Index " << i << ": ";
            for (auto& p : table[i]) {
                cout << "[" << p.first << ": " << p.second << "] ";
            }
            cout << endl;
        }
    }
};

int main() {
    HashTable<int, string> hashtable;
    
    hashtable.insert(1, "One");
    hashtable.insert(11, "Eleven");
    hashtable.insert(21, "Twenty-one");
    hashtable.insert(2, "Two");
    
    hashtable.display();
    
    cout << "\nGet key 1: " << hashtable.get(1) << endl;
    
    cout << "Contains 11: " << (hashtable.contains(11) ? "Yes" : "No") << endl;
    
    hashtable.remove(11);
    cout << "\nAfter removing 11:" << endl;
    hashtable.display();
    
    return 0;
}
```

### Common Interview Problems

```cpp
// Problem 1: Find duplicates in array
vector<int> findDuplicates(vector<int>& nums) {
    unordered_set<int> seen, duplicates;
    vector<int> result;
    
    for (int num : nums) {
        if (seen.count(num)) {
            if (!duplicates.count(num)) {
                duplicates.insert(num);
                result.push_back(num);
            }
        } else {
            seen.insert(num);
        }
    }
    
    return result;
}

// Problem 2: Two Sum
vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int, int> map; // value -> index
    
    for (int i = 0; i < nums.size(); i++) {
        int complement = target - nums[i];
        
        if (map.find(complement) != map.end()) {
            return {map[complement], i};
        }
        
        map[nums[i]] = i;
    }
    
    return {};
}

// Problem 3: Valid Anagram
bool isAnagram(string s, string t) {
    if (s.length() != t.length()) return false;
    
    unordered_map<char, int> freq;
    
    for (char c : s) {
        freq[c]++;
    }
    
    for (char c : t) {
        if (freq[c] == 0) return false;
        freq[c]--;
    }
    
    return true;
}

// Problem 4: First Unique Character
int firstUniqChar(string s) {
    unordered_map<char, int> freq;
    
    for (char c : s) {
        freq[c]++;
    }
    
    for (int i = 0; i < s.length(); i++) {
        if (freq[s[i]] == 1) {
            return i;
        }
    }
    
    return -1;
}
```

### Time Complexities (Hash Tables)

| Operation | Average | Worst Case |
|-----------|---------|------------|
| Search | O(1) | O(n) |
| Insert | O(1) | O(n) |
| Delete | O(1) | O(n) |
| Space | O(n) | O(n) |

---

## Heaps (Min Heap & Max Heap)

### Heap Properties

A **heap** is a complete binary tree where:
- **Max Heap:** Parent ≥ Children
- **Min Heap:** Parent ≤ Children

#### Key Operations:
- **Heapify:** Maintain heap property
- **Push:** Add element and restore heap
- **Pop:** Remove root and restore heap
- **Build Heap:** O(n) heap construction

### Min Heap Implementation

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

class MinHeap {
private:
    vector<int> heap;
    
    int parent(int i) { return (i - 1) / 2; }
    int leftChild(int i) { return 2 * i + 1; }
    int rightChild(int i) { return 2 * i + 2; }
    
    void swap(int& a, int& b) {
        int temp = a;
        a = b;
        b = temp;
    }
    
    void heapifyDown(int i) {
        int smallest = i;
        int left = leftChild(i);
        int right = rightChild(i);
        
        if (left < heap.size() && heap[left] < heap[smallest]) {
            smallest = left;
        }
        
        if (right < heap.size() && heap[right] < heap[smallest]) {
            smallest = right;
        }
        
        if (smallest != i) {
            swap(heap[i], heap[smallest]);
            heapifyDown(smallest);
        }
    }
    
    void heapifyUp(int i) {
        if (i > 0 && heap[parent(i)] > heap[i]) {
            swap(heap[parent(i)], heap[i]);
            heapifyUp(parent(i));
        }
    }
    
public:
    void push(int value) {
        heap.push_back(value);
        heapifyUp(heap.size() - 1);
    }
    
    int pop() {
        if (heap.empty()) throw runtime_error("Heap is empty");
        
        int root = heap[0];
        heap[0] = heap[heap.size() - 1];
        heap.pop_back();
        
        if (!heap.empty()) {
            heapifyDown(0);
        }
        
        return root;
    }
    
    int peek() {
        if (heap.empty()) throw runtime_error("Heap is empty");
        return heap[0];
    }
    
    bool isEmpty() {
        return heap.empty();
    }
    
    // Build heap from array in O(n)
    void buildHeap(vector<int>& arr) {
        heap = arr;
        for (int i = heap.size() / 2 - 1; i >= 0; i--) {
            heapifyDown(i);
        }
    }
    
    void display() {
        for (int val : heap) {
            cout << val << " ";
        }
        cout << endl;
    }
};

int main() {
    MinHeap minHeap;
    
    minHeap.push(10);
    minHeap.push(5);
    minHeap.push(20);
    minHeap.push(3);
    minHeap.push(8);
    
    cout << "Min Heap: ";
    minHeap.display();
    
    cout << "Peek (min): " << minHeap.peek() << endl;
    
    cout << "Pop order: ";
    while (!minHeap.isEmpty()) {
        cout << minHeap.pop() << " ";
    }
    cout << endl;
    
    // Build heap from array
    vector<int> arr = {10, 5, 20, 3, 8, 15};
    MinHeap heap2;
    heap2.buildHeap(arr);
    cout << "Built heap: ";
    heap2.display();
    
    return 0;
}
```

### Max Heap Implementation

```cpp
class MaxHeap {
private:
    vector<int> heap;
    
    int parent(int i) { return (i - 1) / 2; }
    int leftChild(int i) { return 2 * i + 1; }
    int rightChild(int i) { return 2 * i + 2; }
    
    void swap(int& a, int& b) {
        int temp = a;
        a = b;
        b = temp;
    }
    
    void heapifyDown(int i) {
        int largest = i;
        int left = leftChild(i);
        int right = rightChild(i);
        
        if (left < heap.size() && heap[left] > heap[largest]) {
            largest = left;
        }
        
        if (right < heap.size() && heap[right] > heap[largest]) {
            largest = right;
        }
        
        if (largest != i) {
            swap(heap[i], heap[largest]);
            heapifyDown(largest);
        }
    }
    
    void heapifyUp(int i) {
        if (i > 0 && heap[parent(i)] < heap[i]) {
            swap(heap[parent(i)], heap[i]);
            heapifyUp(parent(i));
        }
    }
    
public:
    void push(int value) {
        heap.push_back(value);
        heapifyUp(heap.size() - 1);
    }
    
    int pop() {
        if (heap.empty()) throw runtime_error("Heap is empty");
        
        int root = heap[0];
        heap[0] = heap[heap.size() - 1];
        heap.pop_back();
        
        if (!heap.empty()) {
            heapifyDown(0);
        }
        
        return root;
    }
    
    int peek() {
        if (heap.empty()) throw runtime_error("Heap is empty");
        return heap[0];
    }
    
    bool isEmpty() {
        return heap.empty();
    }
};

// Kth largest element
int findKthLargest(vector<int>& nums, int k) {
    MinHeap minHeap;
    
    for (int num : nums) {
        minHeap.push(num);
        if (minHeap.heap.size() > k) {
            minHeap.pop();
        }
    }
    
    return minHeap.peek();
}
```

---

## Balanced Trees (AVL & Red-Black Trees)

### AVL Tree Concepts

An **AVL Tree** is a self-balancing BST where:
- Height difference (balance factor) ≤ 1
- Rebalances automatically with rotations

#### Balance Factor:
```
balance_factor = height(left_subtree) - height(right_subtree)
Valid: -1, 0, 1
```

#### Rotations: 
- **Left Rotation:** Right-heavy case 
- **Right Rotation:** Left-heavy case 
- **Left-Right Rotation:** Left child is right-heavy 
- **Right-Left Rotation:** Right child is left-heavy

### AVL Tree Implementation

```cpp
#include <iostream>
#include <algorithm>

using namespace std;

struct AVLNode {
    int data;
    AVLNode* left;
    AVLNode* right;
    int height;
    
    AVLNode(int value) 
        : data(value), left(nullptr), right(nullptr), height(1) {}
};

class AVLTree {
private:
    AVLNode* root;
    
    int getHeight(AVLNode* node) {
        return node ? node->height : 0;
    }
    
    int getBalance(AVLNode* node) {
        return node ? getHeight(node->left) - getHeight(node->right) : 0;
    }
    
    void updateHeight(AVLNode* node) {
        if (node) {
            node->height = 1 + max(getHeight(node->left), getHeight(node->right));
        }
    }
    
    // Left rotation
    AVLNode* rotateLeft(AVLNode* x) {
        AVLNode* y = x->right;
        AVLNode* T2 = y->left;
        
        y->left = x;
        x->right = T2;
        
        updateHeight(x);
        updateHeight(y);
        
        return y;
    }
    
    // Right rotation
    AVLNode* rotateRight(AVLNode* y) {
        AVLNode* x = y->left;
        AVLNode* T2 = x->right;
        
        x->right = y;
        y->left = T2;
        
        updateHeight(y);
        updateHeight(x);
        
        return x;
    }
    
    AVLNode* insertHelper(AVLNode* node, int data) {
        if (node == nullptr) {
            return new AVLNode(data);
        }
        
        if (data < node->data) {
            node->left = insertHelper(node->left, data);
        } else if (data > node->data) {
            node->right = insertHelper(node->right, data);
        } else {
            return node; // Duplicate
        }
        
        updateHeight(node);
        int balance = getBalance(node);
        
        // Left-Left case
        if (balance > 1 && data < node->left->data) {
            return rotateRight(node);
        }
        
        // Right-Right case
        if (balance < -1 && data > node->right->data) {
            return rotateLeft(node);
        }
        
        // Left-Right case
        if (balance > 1 && data > node->left->data) {
            node->left = rotateLeft(node->left);
            return rotateRight(node);
        }
        
        // Right-Left case
        if (balance < -1 && data < node->right->data) {
            node->right = rotateRight(node->right);
            return rotateLeft(node);
        }
        
        return node;
    }
    
    bool searchHelper(AVLNode* node, int data) {
        if (node == nullptr) return false;
        
        if (data == node->data) return true;
        if (data < node->data) return searchHelper(node->left, data);
        return searchHelper(node->right, data);
    }
    
    void inOrderHelper(AVLNode* node) {
        if (node == nullptr) return;
        
        inOrderHelper(node->left);
        cout << node->data << " ";
        inOrderHelper(node->right);
    }
    
public:
    AVLTree() : root(nullptr) {}
    
    void insert(int data) {
        root = insertHelper(root, data);
    }
    
    bool search(int data) {
        return searchHelper(root, data);
    }
    
    void inOrder() {
        inOrderHelper(root);
        cout << endl;
    }
};

int main() {
    AVLTree avl;
    
    avl.insert(10);
    avl.insert(20);
    avl.insert(30);
    avl.insert(40);
    avl.insert(50);
    avl.insert(25);
    
    cout << "AVL Tree (In-Order): ";
    avl.inOrder();
    
    cout << "Search 25: " << (avl.search(25) ? "Found" : "Not found") << endl;
    
    return 0;
}
```

### Red-Black Tree Concepts

**Red-Black Trees** are easier to implement than AVL with relaxed balance conditions:
- Every node is RED or BLACK
- Root is BLACK
- Leaves are BLACK
- RED nodes have BLACK children
- All paths have same BLACK node count

**In C++:** Use `std::set` and `std::map` (implemented as Red-Black Trees)

```cpp
#include <set>
#include <map>

int main() {
    // Internally implemented as Red-Black Tree
    set<int> rbtSet;
    rbtSet.insert(50);
    rbtSet.insert(30);
    rbtSet.insert(70);
    rbtSet.insert(20);
    
    // Guaranteed O(log n) operations
    cout << "Set contains 30: " << (rbtSet.find(30) != rbtSet.end()) << endl;
    
    // Map (also Red-Black Tree)
    map<string, int> rbtMap;
    rbtMap["apple"] = 3;
    rbtMap["banana"] = 2;
    
    return 0;
}
```

---

## Trie (Prefix Tree)

A **Trie** is a tree-based data structure for efficient string searching and prefix matching.

### Trie Node Structure

```cpp
#include <iostream>
#include <unordered_map>
#include <vector>

using namespace std;

struct TrieNode {
    unordered_map<char, TrieNode*> children;
    bool isEndOfWord = false;
};

class Trie {
private:
    TrieNode* root;
    
public:
    Trie() {
        root = new TrieNode();
    }
    
    // Insert word into trie
    void insert(string word) {
        TrieNode* node = root;
        
        for (char c : word) {
            if (node->children.find(c) == node->children.end()) {
                node->children[c] = new TrieNode();
            }
            node = node->children[c];
        }
        
        node->isEndOfWord = true;
    }
    
    // Search for exact word
    bool search(string word) {
        TrieNode* node = root;
        
        for (char c : word) {
            if (node->children.find(c) == node->children.end()) {
                return false;
            }
            node = node->children[c];
        }
        
        return node->isEndOfWord;
    }
    
    // Search for prefix
    bool startsWith(string prefix) {
        TrieNode* node = root;
        
        for (char c : prefix) {
            if (node->children.find(c) == node->children.end()) {
                return false;
            }
            node = node->children[c];
        }
        
        return true;
    }
    
    // Get all words with given prefix
    void getAllWordsWithPrefix(string prefix, vector<string>& result) {
        TrieNode* node = root;
        
        for (char c : prefix) {
            if (node->children.find(c) == node->children.end()) {
                return; // Prefix not found
            }
            node = node->children[c];
        }
        
        dfsHelper(node, prefix, result);
    }
    
private:
    void dfsHelper(TrieNode* node, string word, vector<string>& result) {
        if (node->isEndOfWord) {
            result.push_back(word);
        }
        
        for (auto& p : node->children) {
            dfsHelper(p.second, word + p.first, result);
        }
    }
};

int main() {
    Trie trie;
    
    // Insert words
    trie.insert("apple");
    trie.insert("app");
    trie.insert("application");
    trie.insert("apply");
    trie.insert("banana");
    
    // Search
    cout << "Search 'apple': " << (trie.search("apple") ? "Found" : "Not found") << endl;
    cout << "Search 'app': " << (trie.search("app") ? "Found" : "Not found") << endl;
    cout << "Search 'appl': " << (trie.search("appl") ? "Found" : "Not found") << endl;
    
    // Prefix search
    cout << "Starts with 'app': " << (trie.startsWith("app") ? "Yes" : "No") << endl;
    cout << "Starts with 'ban': " << (trie.startsWith("ban") ? "Yes" : "No") << endl;
    
    // Autocomplete
    vector<string> suggestions;
    trie.getAllWordsWithPrefix("app", suggestions);
    cout << "Words starting with 'app': ";
    for (string& word : suggestions) {
        cout << word << " ";
    }
    cout << endl;
    
    return 0;
}
```

### Common Trie Problems

```cpp
// Problem 1: Longest Common Prefix
string longestCommonPrefix(vector<string>& strs) {
    if (strs.empty()) return "";
    
    Trie trie;
    for (string& s : strs) {
        trie.insert(s);
    }
    
    string prefix = "";
    for (int i = 0; i < strs[0].length(); i++) {
        prefix += strs[0][i];
        if (!trie.startsWith(prefix)) {
            prefix.pop_back();
            break;
        }
    }
    
    return prefix;
}

// Problem 2: Word Dictionary
class WordDictionary {
private:
    TrieNode* root;
    
    bool searchHelper(TrieNode* node, string& word, int index) {
        if (index == word.length()) {
            return node->isEndOfWord;
        }
        
        if (word[index] == '.') {
            for (auto& p : node->children) {
                if (searchHelper(p.second, word, index + 1)) {
                    return true;
                }
            }
            return false;
        } else {
            if (node->children.find(word[index]) == node->children.end()) {
                return false;
            }
            return searchHelper(node->children[word[index]], word, index + 1);
        }
    }
    
public:
    WordDictionary() {
        root = new TrieNode();
    }
    
    void addWord(string word) {
        TrieNode* node = root;
        for (char c : word) {
            if (node->children.find(c) == node->children.end()) {
                node->children[c] = new TrieNode();
            }
            node = node->children[c];
        }
        node->isEndOfWord = true;
    }
    
    bool search(string word) {
        return searchHelper(root, word, 0);
    }
};
```

---

## Disjoint Set Union (Union-Find / DSU)

**DSU** efficiently handles set union and membership queries using path compression and union by rank.

### Union-Find Implementation

```cpp
#include <iostream>
#include <vector>

using namespace std;

class DSU {
private:
    vector<int> parent;
    vector<int> rank;
    
public:
    DSU(int n) {
        parent.resize(n);
        rank.resize(n, 0);
        
        // Initially, each element is its own parent
        for (int i = 0; i < n; i++) {
            parent[i] = i;
        }
    }
    
    // Find with path compression
    int find(int x) {
        if (parent[x] != x) {
            parent[x] = find(parent[x]); // Path compression
        }
        return parent[x];
    }
    
    // Union by rank
    bool unite(int x, int y) {
        int rootX = find(x);
        int rootY = find(y);
        
        if (rootX == rootY) {
            return false; // Already in same set
        }
        
        // Union by rank
        if (rank[rootX] < rank[rootY]) {
            parent[rootX] = rootY;
        } else if (rank[rootX] > rank[rootY]) {
            parent[rootY] = rootX;
        } else {
            parent[rootY] = rootX;
            rank[rootX]++;
        }
        
        return true;
    }
    
    // Check if connected
    bool connected(int x, int y) {
        return find(x) == find(y);
    }
};

int main() {
    DSU dsu(10);
    
    dsu.unite(0, 1);
    dsu.unite(1, 2);
    dsu.unite(3, 4);
    
    cout << "0 and 2 connected: " << (dsu.connected(0, 2) ? "Yes" : "No") << endl; // Yes
    cout << "0 and 4 connected: " << (dsu.connected(0, 4) ? "Yes" : "No") << endl; // No
    
    dsu.unite(2, 4);
    cout << "0 and 4 connected: " << (dsu.connected(0, 4) ? "Yes" : "No") << endl; // Yes
    
    return 0;
}
```

### DSU Applications

```cpp
// Problem 1: Detect cycle in undirected graph
bool hasCycle(int n, vector<pair<int, int>>& edges) {
    DSU dsu(n);
    
    for (auto& edge : edges) {
        int u = edge.first;
        int v = edge.second;
        
        if (dsu.connected(u, v)) {
            return true; // Cycle detected
        }
        
        dsu.unite(u, v);
    }
    
    return false;
}

// Problem 2: Number of connected components
int countComponents(int n, vector<pair<int, int>>& edges) {
    DSU dsu(n);
    
    for (auto& edge : edges) {
        dsu.unite(edge.first, edge.second);
    }
    
    set<int> roots;
    for (int i = 0; i < n; i++) {
        roots.insert(dsu.find(i));
    }
    
    return roots.size();
}

// Problem 3: Kruskal's Algorithm for MST
class Edge {
public:
    int u, v, weight;
    
    bool operator<(const Edge& other) const {
        return weight < other.weight;
    }
};

int kruskalMST(int n, vector<Edge>& edges) {
    sort(edges.begin(), edges.end());
    DSU dsu(n);
    
    int mstWeight = 0;
    int edgesUsed = 0;
    
    for (auto& edge : edges) {
        if (dsu.unite(edge.u, edge.v)) {
            mstWeight += edge.weight;
            edgesUsed++;
            if (edgesUsed == n - 1) break;
        }
    }
    
    return mstWeight;
}
```

---

## Heap Sort

**Heap Sort** uses a heap to sort elements in O(n log n) time.

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

void heapify(vector<int>& arr, int n, int i) {
    int largest = i;
    int left = 2 * i + 1;
    int right = 2 * i + 2;
    
    if (left < n && arr[left] > arr[largest]) {
        largest = left;
    }
    
    if (right < n && arr[right] > arr[largest]) {
        largest = right;
    }
    
    if (largest != i) {
        swap(arr[i], arr[largest]);
        heapify(arr, n, largest);
    }
}

void heapSort(vector<int>& arr) {
    int n = arr.size();
    
    // Build max heap
    for (int i = n / 2 - 1; i >= 0; i--) {
        heapify(arr, n, i);
    }
    
    // Extract elements from heap
    for (int i = n - 1; i > 0; i--) {
        swap(arr[0], arr[i]);
        heapify(arr, i, 0);
    }
}

void display(const vector<int>& arr) {
    for (int val : arr) {
        cout << val << " ";
    }
    cout << endl;
}

int main() {
    vector<int> arr = {12, 11, 13, 5, 6, 7};
    
    cout << "Original: ";
    display(arr);
    
    heapSort(arr);
    
    cout << "Sorted: ";
    display(arr);
    
    return 0;
}
```

### Time Complexities (Heap Sort)
- **Best:** O(n log n)
- **Average:** O(n log n)
- **Worst:** O(n log n)
- **Space:** O(1)

---

## Two-Pointer Techniques

Two pointers solve array/string problems efficiently by maintaining pointers at strategic positions.

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

// Problem 1: Two Sum II (Sorted array)
vector<int> twoSum(vector<int>& numbers, int target) {
    int left = 0, right = numbers.size() - 1;
    
    while (left < right) {
        int sum = numbers[left] + numbers[right];
        
        if (sum == target) {
            return {left + 1, right + 1}; // 1-indexed
        } else if (sum < target) {
            left++;
        } else {
            right--;
        }
    }
    
    return {};
}

// Problem 2: Valid Palindrome
bool isPalindrome(string s) {
    int left = 0, right = s.length() - 1;
    
    while (left < right) {
        while (left < right && !isalnum(s[left])) left++;
        while (left < right && !isalnum(s[right])) right--;
        
        if (tolower(s[left]) != tolower(s[right])) {
            return false;
        }
        
        left++;
        right--;
    }
    
    return true;
}

// Problem 3: Container with Most Water
int maxArea(vector<int>& height) {
    int left = 0, right = height.size() - 1;
    int maxWater = 0;
    
    while (left < right) {
        int width = right - left;
        int h = min(height[left], height[right]);
        maxWater = max(maxWater, width * h);
        
        if (height[left] < height[right]) {
            left++;
        } else {
            right--;
        }
    }
    
    return maxWater;
}

// Problem 4: Remove Duplicates (In-place)
int removeDuplicates(vector<int>& nums) {
    int pointer = 0;
    
    for (int i = 1; i < nums.size(); i++) {
        if (nums[i] != nums[pointer]) {
            pointer++;
            nums[pointer] = nums[i];
        }
    }
    
    return pointer + 1;
}

// Problem 5: Sort Colors (3-way partition)
void sortColors(vector<int>& nums) {
    int left = 0, mid = 0, right = nums.size() - 1;
    
    while (mid <= right) {
        if (nums[mid] == 0) {
            swap(nums[left], nums[mid]);
            left++;
            mid++;
        } else if (nums[mid] == 1) {
            mid++;
        } else {
            swap(nums[mid], nums[right]);
            right--;
        }
    }
}

int main() {
    // Test Two Sum II
    vector<int> nums = {2, 7, 11, 15};
    vector<int> result = twoSum(nums, 9);
    cout << "Two Sum: [" << result[0] << ", " << result[1] << "]" << endl;
    
    // Test Palindrome
    cout << "Is 'a man, a plan, a canal: Panama' a palindrome? "
         << (isPalindrome("a man, a plan, a canal: Panama") ? "Yes" : "No") << endl;
    
    // Test Container
    vector<int> heights = {1, 8, 6, 2, 5, 4, 8, 3, 7};
    cout << "Max water area: " << maxArea(heights) << endl;
    
    return 0;
}
```

---

## Sliding Window

Sliding window maintains a window of elements and slides it across the data structure.

```cpp
#include <iostream>
#include <vector>
#include <unordered_map>
#include <algorithm>

using namespace std;

// Problem 1: Longest Substring Without Repeating Characters
int lengthOfLongestSubstring(string s) {
    unordered_map<char, int> lastIndex;
    int left = 0, maxLen = 0;
    
    for (int right = 0; right < s.length(); right++) {
        if (lastIndex.find(s[right]) != lastIndex.end()) {
            left = max(left, lastIndex[s[right]] + 1);
        }
        
        lastIndex[s[right]] = right;
        maxLen = max(maxLen, right - left + 1);
    }
    
    return maxLen;
}

// Problem 2: Minimum Window Substring
string minWindow(string s, string t) {
    unordered_map<char, int> required, windowCounts;
    
    for (char c : t) {
        required[c]++;
    }
    
    int left = 0, formed = 0;
    int minLen = INT_MAX, minStart = 0;
    
    for (int right = 0; right < s.length(); right++) {
        char c = s[right];
        windowCounts[c]++;
        
        if (windowCounts[c] == required[c]) {
            formed++;
        }
        
        while (formed == required.size()) {
            if (right - left + 1 < minLen) {
                minLen = right - left + 1;
                minStart = left;
            }
            
            char leftChar = s[left];
            windowCounts[leftChar]--;
            if (windowCounts[leftChar] < required[leftChar]) {
                formed--;
            }
            left++;
        }
    }
    
    return minLen == INT_MAX ? "" : s.substr(minStart, minLen);
}

// Problem 3: Maximum Average Subarray
double findMaxAverage(vector<int>& nums, int k) {
    double maxSum = 0, currentSum = 0;
    
    for (int i = 0; i < k; i++) {
        currentSum += nums[i];
    }
    maxSum = currentSum;
    
    for (int i = k; i < nums.size(); i++) {
        currentSum += nums[i] - nums[i - k];
        maxSum = max(maxSum, currentSum);
    }
    
    return maxSum / k;
}

// Problem 4: Sliding Window Maximum
vector<int> maxSlidingWindow(vector<int>& nums, int k) {
    vector<int> result;
    deque<int> indices; // Store indices of useful elements
    
    for (int i = 0; i < nums.size(); i++) {
        // Remove elements outside window
        if (!indices.empty() && indices.front() < i - k + 1) {
            indices.pop_front();
        }
        
        // Remove elements smaller than current
        while (!indices.empty() && nums[indices.back()] < nums[i]) {
            indices.pop_back();
        }
        
        indices.push_back(i);
        
        // Add to result when window is complete
        if (i >= k - 1) {
            result.push_back(nums[indices.front()]);
        }
    }
    
    return result;
}

int main() {
    // Test 1
    cout << "Longest substring without repeating: "
         << lengthOfLongestSubstring("abcabcbb") << endl; // 3 (abc)
    
    // Test 2
    cout << "Min window: " << minWindow("ADOBECODEBANC", "ABC") << endl; // "BANC"
    
    // Test 3
    vector<int> nums = {1, 3, -1, -3, 5, 3, 4, 3, 6};
    cout << "Max average with k=3: " << findMaxAverage(nums, 3) << endl;
    
    // Test 4
    vector<int> result = maxSlidingWindow(nums, 3);
    cout << "Sliding window max: ";
    for (int val : result) {
        cout << val << " ";
    }
    cout << endl;
    
    return 0;
}
```

---

## Backtracking

Backtracking explores all possible solutions by building incrementally and abandoning paths that fail.

```cpp
#include <iostream>
#include <vector>
#include <string>

using namespace std;

// Problem 1: Generate Permutations
void permuteHelper(vector<int>& nums, vector<vector<int>>& result, 
                   int start, int end) {
    if (start == end) {
        result.push_back(nums);
        return;
    }
    
    for (int i = start; i <= end; i++) {
        swap(nums[start], nums[i]);
        permuteHelper(nums, result, start + 1, end);
        swap(nums[start], nums[i]); // Backtrack
    }
}

vector<vector<int>> permute(vector<int> nums) {
    vector<vector<int>> result;
    permuteHelper(nums, result, 0, nums.size() - 1);
    return result;
}

// Problem 2: Combinations
void combineHelper(int n, int k, int start, vector<int>& current,
                   vector<vector<int>>& result) {
    if (current.size() == k) {
        result.push_back(current);
        return;
    }
    
    for (int i = start; i <= n; i++) {
        current.push_back(i);
        combineHelper(n, k, i + 1, current, result);
        current.pop_back(); // Backtrack
    }
}

vector<vector<int>> combine(int n, int k) {
    vector<vector<int>> result;
    vector<int> current;
    combineHelper(n, k, 1, current, result);
    return result;
}

// Problem 3: N-Queens
bool isSafe(vector<string>& board, int row, int col, int n) {
    // Check column
    for (int i = 0; i < row; i++) {
        if (board[i][col] == 'Q') return false;
    }
    
    // Check diagonal (top-left)
    for (int i = row - 1, j = col - 1; i >= 0 && j >= 0; i--, j--) {
        if (board[i][j] == 'Q') return false;
    }
    
    // Check diagonal (top-right)
    for (int i = row - 1, j = col + 1; i >= 0 && j < n; i--, j++) {
        if (board[i][j] == 'Q') return false;
    }
    
    return true;
}

void nQueensHelper(vector<string>& board, int row, int n,
                   vector<vector<string>>& result) {
    if (row == n) {
        result.push_back(board);
        return;
    }
    
    for (int col = 0; col < n; col++) {
        if (isSafe(board, row, col, n)) {
            board[row][col] = 'Q';
            nQueensHelper(board, row + 1, n, result);
            board[row][col] = '.'; // Backtrack
        }
    }
}

vector<vector<string>> solveNQueens(int n) {
    vector<vector<string>> result;
    vector<string> board(n, string(n, '.'));
    nQueensHelper(board, 0, n, result);
    return result;
}

// Problem 4: Word Search
bool wordSearchHelper(vector<vector<char>>& board, string& word, int idx,
                     int row, int col, vector<vector<bool>>& visited) {
    if (idx == word.length()) return true;
    
    if (row < 0 || row >= board.size() || col < 0 || col >= board[0].size()
        || visited[row][col] || board[row][col] != word[idx]) {
        return false;
    }
    
    visited[row][col] = true;
    
    bool found = wordSearchHelper(board, word, idx + 1, row + 1, col, visited) ||
                 wordSearchHelper(board, word, idx + 1, row - 1, col, visited) ||
                 wordSearchHelper(board, word, idx + 1, row, col + 1, visited) ||
                 wordSearchHelper(board, word, idx + 1, row, col - 1, visited);
    
    visited[row][col] = false; // Backtrack
    return found;
}

bool wordSearch(vector<vector<char>>& board, string word) {
    int m = board.size(), n = board[0].size();
    vector<vector<bool>> visited(m, vector<bool>(n, false));
    
    for (int i = 0; i < m; i++) {
        for (int j = 0; j < n; j++) {
            if (wordSearchHelper(board, word, 0, i, j, visited)) {
                return true;
            }
        }
    }
    
    return false;
}

int main() {
    // Test Permutations
    vector<int> nums = {1, 2, 3};
    auto perms = permute(nums);
    cout << "Permutations of {1,2,3}: " << perms.size() << " permutations" << endl;
    
    // Test Combinations
    auto combs = combine(4, 2);
    cout << "Combinations C(4,2): " << combs.size() << " combinations" << endl;
    
    return 0;
}
```

---

## Dynamic Programming

DP solves problems by breaking them into subproblems and storing results.

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <unordered_map>

using namespace std;

// Problem 1: Fibonacci
int fib(int n, vector<int>& memo) {
    if (n <= 1) return n;
    if (memo[n] != -1) return memo[n];
    
    return memo[n] = fib(n - 1, memo) + fib(n - 2, memo);
}

// Problem 2: 0/1 Knapsack
int knapsack(vector<int>& weights, vector<int>& values, int capacity) {
    int n = weights.size();
    vector<vector<int>> dp(n + 1, vector<int>(capacity + 1, 0));
    
    for (int i = 1; i <= n; i++) {
        for (int w = 1; w <= capacity; w++) {
            if (weights[i - 1] <= w) {
                dp[i][w] = max(dp[i - 1][w],
                              dp[i - 1][w - weights[i - 1]] + values[i - 1]);
            } else {
                dp[i][w] = dp[i - 1][w];
            }
        }
    }
    
    return dp[n][capacity];
}

// Problem 3: Longest Increasing Subsequence (LIS)
int lengthOfLIS(vector<int>& nums) {
    int n = nums.size();
    vector<int> dp(n, 1);
    
    for (int i = 1; i < n; i++) {
        for (int j = 0; j < i; j++) {
            if (nums[j] < nums[i]) {
                dp[i] = max(dp[i], dp[j] + 1);
            }
        }
    }
    
    return *max_element(dp.begin(), dp.end());
}

// Problem 4: Coin Change
int coinChange(vector<int>& coins, int amount) {
    vector<int> dp(amount + 1, INT_MAX);
    dp[0] = 0;
    
    for (int i = 1; i <= amount; i++) {
        for (int coin : coins) {
            if (coin <= i && dp[i - coin] != INT_MAX) {
                dp[i] = min(dp[i], dp[i - coin] + 1);
            }
        }
    }
    
    return dp[amount] == INT_MAX ? -1 : dp[amount];
}

// Problem 5: Edit Distance (Levenshtein Distance)
int editDistance(string word1, string word2) {
    int m = word1.length(), n = word2.length();
    vector<vector<int>> dp(m + 1, vector<int>(n + 1));
    
    for (int i = 0; i <= m; i++) {
        dp[i][0] = i;
    }
    for (int j = 0; j <= n; j++) {
        dp[0][j] = j;
    }
    
    for (int i = 1; i <= m; i++) {
        for (int j = 1; j <= n; j++) {
            if (word1[i - 1] == word2[j - 1]) {
                dp[i][j] = dp[i - 1][j - 1];
            } else {
                dp[i][j] = 1 + min({dp[i - 1][j],      // Delete
                                    dp[i][j - 1],      // Insert
                                    dp[i - 1][j - 1]   // Replace
                                   });
            }
        }
    }
    
    return dp[m][n];
}

// Problem 6: Longest Common Subsequence (LCS)
int longestCommonSubsequence(string text1, string text2) {
    int m = text1.length(), n = text2.length();
    vector<vector<int>> dp(m + 1, vector<int>(n + 1, 0));
    
    for (int i = 1; i <= m; i++) {
        for (int j = 1; j <= n; j++) {
            if (text1[i - 1] == text2[j - 1]) {
                dp[i][j] = dp[i - 1][j - 1] + 1;
            } else {
                dp[i][j] = max(dp[i - 1][j], dp[i][j - 1]);
            }
        }
    }
    
    return dp[m][n];
}

// Problem 7: Maximum Subarray (Kadane's Algorithm)
int maxSubArray(vector<int>& nums) {
    int maxSum = nums[0];
    int currentSum = nums[0];
    
    for (int i = 1; i < nums.size(); i++) {
        currentSum = max(nums[i], currentSum + nums[i]);
        maxSum = max(maxSum, currentSum);
    }
    
    return maxSum;
}

// Problem 8: Unique Paths
int uniquePaths(int m, int n) {
    vector<vector<int>> dp(m, vector<int>(n, 1));
    
    for (int i = 1; i < m; i++) {
        for (int j = 1; j < n; j++) {
            dp[i][j] = dp[i - 1][j] + dp[i][j - 1];
        }
    }
    
    return dp[m - 1][n - 1];
}

int main() {
    // Test Fibonacci
    vector<int> memo(10, -1);
    cout << "Fib(9): " << fib(9, memo) << endl;
    
    // Test Knapsack
    vector<int> weights = {2, 3, 4, 5};
    vector<int> values = {3, 4, 5, 6};
    cout << "Knapsack(capacity=8): " << knapsack(weights, values, 8) << endl;
    
    // Test LIS
    vector<int> lis_arr = {10, 9, 2, 5, 3, 7, 101, 18};
    cout << "LIS length: " << lengthOfLIS(lis_arr) << endl;
    
    // Test Coin Change
    vector<int> coins = {1, 2, 5};
    cout << "Coin change for 5: " << coinChange(coins, 5) << endl;
    
    // Test Edit Distance
    cout << "Edit distance ('horse', 'ros'): "
         << editDistance("horse", "ros") << endl;
    
    return 0;
}
```

---

## Advanced Graph Algorithms

### Dijkstra's Algorithm

```cpp
#include <iostream>
#include <vector>
#include <queue>
#include <climits>

using namespace std;

vector<int> dijkstra(int n, vector<vector<pair<int, int>>>& graph, int start) {
    vector<int> dist(n, INT_MAX);
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;
    
    dist[start] = 0;
    pq.push({0, start});
    
    while (!pq.empty()) {
        auto [d, u] = pq.top();
        pq.pop();
        
        if (d > dist[u]) continue;
        
        for (auto [v, weight] : graph[u]) {
            if (dist[u] + weight < dist[v]) {
                dist[v] = dist[u] + weight;
                pq.push({dist[v], v});
            }
        }
    }
    
    return dist;
}

int main() {
    int n = 5;
    vector<vector<pair<int, int>>> graph(n);
    
    graph[0].push_back({1, 4});
    graph[0].push_back({2, 1});
    graph[1].push_back({3, 1});
    graph[2].push_back({1, 2});
    graph[2].push_back({3, 5});
    graph[3].push_back({4, 3});
    
    vector<int> dist = dijkstra(n, graph, 0);
    
    cout << "Distances from 0: ";
    for (int d : dist) {
        cout << (d == INT_MAX ? -1 : d) << " ";
    }
    cout << endl;
    
    return 0;
}
```

### Prim's Algorithm (MST)

```cpp
int primMST(int n, vector<vector<pair<int, int>>>& graph) {
    vector<bool> visited(n, false);
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;
    
    pq.push({0, 0});
    int mstWeight = 0;
    
    while (!pq.empty()) {
        auto [weight, u] = pq.top();
        pq.pop();
        
        if (visited[u]) continue;
        
        visited[u] = true;
        mstWeight += weight;
        
        for (auto [v, w] : graph[u]) {
            if (!visited[v]) {
                pq.push({w, v});
            }
        }
    }
    
    return mstWeight;
}
```

### Topological Sort (Kahn's Algorithm)

```cpp
vector<int> topologicalSort(int n, vector<vector<int>>& graph) {
    vector<int> inDegree(n, 0);
    queue<int> q;
    vector<int> result;
    
    for (int u = 0; u < n; u++) {
        for (int v : graph[u]) {
            inDegree[v]++;
        }
    }
    
    for (int i = 0; i < n; i++) {
        if (inDegree[i] == 0) {
            q.push(i);
        }
    }
    
    while (!q.empty()) {
        int u = q.front();
        q.pop();
        result.push_back(u);
        
        for (int v : graph[u]) {
            inDegree[v]--;
            if (inDegree[v] == 0) {
                q.push(v);
            }
        }
    }
    
    return result.size() == n ? result : vector<int>();
}
```

### Floyd-Warshall Algorithm

```cpp
void floydWarshall(int n, vector<vector<int>>& dist) {
    for (int k = 0; k < n; k++) {
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                if (dist[i][k] != INT_MAX && dist[k][j] != INT_MAX) {
                    dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j]);
                }
            }
        }
    }
}
```

---

## Segment Tree

A **Segment Tree** efficiently handles range queries and updates.

```cpp
#include <iostream>
#include <vector>

using namespace std;

class SegmentTree {
private:
    vector<int> tree;
    int n;
    
    void build(vector<int>& arr, int node, int start, int end) {
        if (start == end) {
            tree[node] = arr[start];
        } else {
            int mid = (start + end) / 2;
            build(arr, 2 * node, start, mid);
            build(arr, 2 * node + 1, mid + 1, end);
            tree[node] = tree[2 * node] + tree[2 * node + 1];
        }
    }
    
    void updateHelper(int node, int start, int end, int idx, int val) {
        if (start == end) {
            tree[node] = val;
        } else {
            int mid = (start + end) / 2;
            if (idx <= mid) {
                updateHelper(2 * node, start, mid, idx, val);
            } else {
                updateHelper(2 * node + 1, mid + 1, end, idx, val);
            }
            tree[node] = tree[2 * node] + tree[2 * node + 1];
        }
    }
    
    int queryHelper(int node, int start, int end, int l, int r) {
        if (r < start || end < l) return 0; // No overlap
        if (l <= start && end <= r) return tree[node]; // Complete overlap
        
        int mid = (start + end) / 2;
        return queryHelper(2 * node, start, mid, l, r) +
               queryHelper(2 * node + 1, mid + 1, end, l, r);
    }
    
public:
    SegmentTree(vector<int>& arr) {
        n = arr.size();
        tree.resize(4 * n);
        build(arr, 1, 0, n - 1);
    }
    
    void update(int idx, int val) {
        updateHelper(1, 0, n - 1, idx, val);
    }
    
    int query(int l, int r) {
        return queryHelper(1, 0, n - 1, l, r);
    }
};

int main() {
    vector<int> arr = {1, 3, 5, 7, 9, 11};
    SegmentTree st(arr);
    
    cout << "Sum(1, 3): " << st.query(1, 3) << endl; // 3+5+7 = 15
    
    st.update(1, 10);
    cout << "After update(1, 10), Sum(1, 3): " << st.query(1, 3) << endl; // 10+5+7 = 22
    
    return 0;
}
```

---

## Time Complexity Summary Table

| Data Structure / Algorithm | Best | Average | Worst | Space |
|----------------------------|------|---------|-------|-------|
| Hash Table (insert/delete/search) | O(1) | O(1) | O(n) | O(n) |
| Heap (insert/delete) | O(1) | O(log n) | O(log n) | O(n) |
| AVL Tree (insert/delete) | - | O(log n) | O(log n) | O(n) |
| Trie (insert/search) | - | O(m) | O(m) | O(ALPHABET_SIZE * n * m) |
| DSU (union/find) | - | O(α(n)) | O(α(n)) | O(n) |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) |
| Dijkstra | O(E log V) | O(E log V) | O(E log V) | O(V) |
| Segment Tree (query/update) | - | O(log n) | O(log n) | O(n) |

---

## Key Interview Takeaways

**When to use each:**

- **Hash Table:** Frequency counting, duplicate detection, cache
- **Heap:** Priority queue, Kth largest/smallest, heap sort
- **AVL/RB Tree:** Ordered data with guaranteed O(log n) operations
- **Trie:** String prefix search, autocomplete, dictionary
- **DSU:** Connected components, cycle detection, MST
- **Two-Pointer:** Sorted arrays, palindromes, window problems
- **Sliding Window:** Substring/subarray problems, optimization
- **Backtracking:** Permutations, combinations, puzzle solving
- **DP:** Optimization problems, overlapping subproblems
- **Dijkstra:** Shortest path in weighted graphs
- **Segment Tree:** Range queries and updates efficiently

**Pro Tips:**
- Always analyze time/space complexity
- Think about edge cases (empty input, single element)
- Choose the right data structure for the problem
- DP is about identifying subproblems and recurrence relation
- Backtracking requires careful constraint checking

This comprehensive guide covers ~95% of interview DSA questions!

---
End-of-File

The [KintsugiStack](https://github.com/kintsugi-programmer/KintsugiStack) repository, authored by Kintsugi-Programmer, is less a comprehensive resource and more an Artifact of Continuous Research and Deep Inquiry into Computer Science and Software Engineering. It serves as a transparent ledger of the author's relentless pursuit of mastery, from the foundational algorithms to modern full-stack implementation.

> Made with 💚 [Kintsugi-Programmer](https://github.com/kintsugi-programmer)
