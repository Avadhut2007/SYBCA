# Introduction to Data Structures

### Topics Covered:

- Self Referential Structure
    
    **Structure — Basics (prerequisite):**
    
    - The use of structures helps organize complicated data, particularly in large programs, by treating a group of related variables as a unit rather than separate entities.
    - **Structure**: a composition of variables (possibly of different data types) grouped together under a single name.
    - Each variable inside the structure is called a **member**. The name given to the structure is called a **structure tag**.
    
    ```c
    struct tag
    {
        data_type member1, member2, ...;
    } instance;
    ```
    
    **Example:**
    
    ```c
    struct student
    {
        int rno, age;
        char name[20];
    } s;
    
    struct student s1;
    ```
    
    **Initialization:**
    
    ```c
    struct student
    {
        int rno, age;
        char name[20];
    } s = {1, 21, "Akash"};
    
    struct student s1 = {2, 21, "Sonali"};
    ```
    
    **Accessing Structure Members:**
    
    - Members are accessed using the **dot operator (.)** between the structure variable and member name.
    - Syntax: `structure_variable.member;`
    - Example: `s.rno; s.age; s.name;`
    
    **Size of a Structure:**
    
    - Size = sum of sizes required for its individual members.
    - Example: `char name[20]; int rno, age;` → size = 20 + 2 + 2 = **24 bytes**
    
    **Array of Structures:**
    
    - An array of structures can be declared just like any other array — each element is an individual structure.
    - All array elements occupy consecutive memory locations.
    
    ```c
    struct student
    {
        ...
    } s[size];
    // OR
    struct student s[size];
    ```
    
    **Pointer to Structures:**
    
    - The address of a structure variable is obtained using the `&` operator, and assigned to a pointer declared as a pointer to that structure type.
    
    ```c
    struct student
    {
        int rno, age;
    } s;
    struct student *p;
    p = &s;
    ```
    
    **Accessing Structure Variables Using Pointer:**
    
    - Use the **arrow operator (->)** to access members through a pointer.
    
    ```c
    p->rno;
    p->age;
    ```
    
    ---
    
    **Self-Referential Structure:**
    
    - A self-referential structure is a structure that can have members which point to a structure variable of the same type.
    - They can have one or more pointers pointing to the same type of structure as their member.
    - Widely used in dynamic data structures such as linked lists, trees, etc.
    
    **Syntax:**
    
    ```c
    struct structure_name
    {
        data_type member1;
        struct structure_name *pointer_name;
    } instance;
    ```
    
    **Diagram (from slide) — Linked list built using self-referential structure:**
    
    ```
    Head
      |
      v
    [ 5 | * ] --> [ 10 | * ] --> [ 20 | * ] --> [ 1 | * ] --> Null
    ```
    
    Each box has a data field and a pointer field. The pointer field of each node points to the next node of the *same struct type*, and the last node's pointer is Null. `Head` points to the first node.
    
- Data Structures: Overview and Classification
    
    **Key Definitions:**
    
    - **Data** – A collection of numbers, alphabets, and symbols combined to represent information.
    - **Data Type** – Term describing the type of information a language supports (int, char, float, double, etc.)
    - **Data Object** – A set of elements (D), finite or infinite. e.g. D={0,+1,-1,+2,-2…} or D={'A'…'Z'}
    - **Structure** – Way of organizing data so it's easier to use.
    - **Data Structure** – A particular way of organizing data in a computer so it can be used efficiently; a scheme for organizing related pieces of information.
    
    **Advantages of Data Structures:**
    
    - Easier to access and manipulate information vs raw/unstructured data
    - Variety of operations can be performed on structured data
    - Related data stored together in required format
    - Better algorithms can be applied → improves program efficiency
    
    **Operations on Data Structures:**
    
    - Create
    - Add an element
    - Delete an element
    - Traverse / Display
    - Sort the list of elements
    - Search for a data element
    
    **Classification (hierarchy):**
    
    ```
    Data Structure
    |-- Primitive Data Structure (Integer, Float, Character, Pointer)
    `-- Non-Primitive Data Structure
        |-- Linear Data Structure (Array, Linked List, Stack, Queue)
        `-- Non-Linear Data Structure (Tree, Graph, Files)
    ```
    
- Primitive and Non Primitive Data Structures
    
    **Primitive Data Structure:**
    
    - Used to represent standard data types of a computer language
    - Examples: integer, character, float, pointer
    
    **Non-Primitive Data Structure:**
    
    - Constructed using one or more primitive data structures
    - Has a specific functionality; can be designed by the user
    - Classified into: Linear and Non-Linear Data Structures
- Linear and Nonlinear Structures
    
    **Linear Data Structures:**
    
    - A linear data structure traverses the data elements sequentially, in which only one data element can directly be reached.
    - Examples: Arrays, Linked Lists
    
    **Non-Linear Data Structures:**
    
    - Every data item is attached to several other data items in a way that is specific for reflecting relationships. The data items are not arranged in a sequential structure.
    - Examples: Trees, Graphs
    
    **Types Overview:**
    
    | Type | Description |
    | --- | --- |
    | Array | Contiguous memory block; each location stores one fixed-length item |
    | Stack | Insert/remove from same end → LIFO (Last In First Out) |
    | Queue | Insert from one end, remove from other → FIFO (First In First Out) |
    | Linked List | Dynamic structure; space allocated/freed as needed |
    | Tree | Non-linear; represents hierarchical relationships. Binary Tree = each node has max 2 children (left/right) |
    | Graph | Set of vertices (V) connected by edges (E); G = (V, E). Trees are a special kind of graph |
    
    ---
    
    **Array** — a contiguous block of memory locations where each memory location stores one fixed-length data item.
    
    ```c
    int a[10];      // Array of Integers
    char b[10];     // Array of Character
    ```
    
    **Diagram (Array of Integers / Array of Characters):**
    
    ```
    Index:   0  1  2  3  4  5  6  7  8  9
    Int a:   5  6  4  3  7  8  9  2  1  2
    
    Index:   0  1  2  3  4  5  6  7  8  9
    Char b:  M  I  T  W  P  U  P  U  N  E
    ```
    
    **Stack** — items can be inserted only from one end and removed from the same end. The last item inserted is the first item taken out → **LIFO (Last In First Out)**.
    
    **Diagram (stack, top to bottom = last-in at top):**
    
    ```
     Top of Stack
    +--------+
    |   20   |  <- last pushed, first to pop
    +--------+
    |   10   |
    +--------+
    |    5   |  <- first pushed, last to pop
    +--------+
    ```
    
    **Queue** — a two-ended data structure where items are inserted from one end and taken out from the other end. The first item inserted is the first item taken out → **FIFO (First In First Out)**.
    
    **Diagram (people queueing into a building):**
    
    ```
    Rear (new people join) --> [ ][ ][ ][ ][ ][ ][ ][ ][ ] --> Front (first person served/exits)
    ```
    
    **Linked List** — space to store items is created as needed and destroyed when no longer required. Hence it's a **dynamic data structure**; space is acquired only when needed.
    
    **Diagram:**
    
    ```
    [17|*] --> [23|*] --> [55|*] --> [72|*] --> [14|*] --> [62|*] --> (end)
    ```
    
    **Tree** — a non-linear data structure mainly used to represent data containing a hierarchical relationship between elements.
    
    **Binary Tree** — a tree such that every node has at most 2 children, each labeled as either the left or right child.
    
    **Diagram (General Tree vs Binary Tree):**
    
    ```
    General Tree                       Binary Tree
            Root                              Root
          /  |  \                            /    \
     Parent Node ...                     Parent    Node
      / | \   / \                         /  \        \
    Child . Leaf .                     Child  Leaf     Leaf
    
    (a node can have many children)     (each node has at most 2 children)
    ```
    
    **Graph** — a set of items connected by edges. Each item is called a vertex or node. Trees are just a special kind of graph. Graphs are usually represented as **G = (V, E)**, where V is the set of vertices and E is the set of edges.
    
    **Diagram (undirected graph with diagonal, and directed graph):**
    
    ```
    Undirected (4 vertices, one diagonal edge):
      A---B
      | \ |
      D---C          edges: A-B, B-C, C-D, D-A, A-C
    
    Directed graph (4 nodes with directed edges):
      A          B
       \        /
        v      v
           C
        ^      ^
       /        \
      D -------->  (back up to B)
    ```
    
- Algorithm Analysis
    
    **Algorithm — Definition:**
    
    - A finite set of instructions in a specific sequence, which if followed, accomplishes a particular task.
    
    **Steps in Algorithm Development:**
    
    1. Identification of input
    2. Identification of output
    3. Identification of processing operations
    4. Processing Definiteness (no ambiguity)
    5. Processing Finiteness (must terminate)
    6. Possessing Effectiveness (steps must be practically executable)
    
    **Characteristics of a Good Algorithm:**
    
    - Finiteness – terminates after finite steps
    - Definiteness – each instruction clear & unambiguous
    - Effectiveness – primitive, convertible to program statements
    - Input – accepts zero or more external inputs
    - Output – produces at least one output
    
    **Advantages:**
    
    - Language/hardware independent
    - Makes program logic easy to understand
    - Errors easier to identify
    - Program can be written directly from it
    - Written in simple English → understandable by all
    
    **Disadvantages:**
    
    - Time-consuming to write
    - Difficult to show branching/repetition
    - Unclear how much detail to include
    - Can get lengthy/complicated for big tasks
    
    **Algorithm Analysis Basics:**
    
    - Efficiency measured in terms of **time** and **space**
    - **Space Complexity** – memory needed = fixed part (constants) + variable part
    - **Time Complexity** – time taken for execution
    - **Frequency Count** – total number of times a statement executes
    
    **Best / Average / Worst Case:**
    
    - **Best case** – minimum steps executed
    - **Worst case** – maximum steps executed (slowest)
    - **Average case** – average steps executed
    - Example: Searching in an array of n elements → Best = 1, Worst = n, Average = n/2
- Big O Notation
    
    **Asymptotic Notations Overview:**
    
    - The time and space complexity of an algorithm can be expressed in several ways: the algorithm never takes more than some function of n operations; its running time is always less than some function of n; its running time is order of some function of n.
    - Expressed using Asymptotic Notations **(O, Ω, Ɵ)**. They're called "asymptotic" because they apply for large values of n.
    
    **O Notation (Big O) — Upper Bound:**
    
    - Denotes the **worst case** of an algorithm.
    - Expressed as O(g(n)).
    - Definition: f(n) = O(g(n)) iff there exist positive constants c and n₀ such that f(n) ≤ c·g(n) for all n ≥ n₀, c > 0, n₀ ≥ 1
    - **Diagram (upper bound):** f(n) stays below the curve c·g(n) for all n once n ≥ n₀ — cg(n) forms a ceiling above f(n) from n₀ onward.
    
    ![175911.jpg](Introduction%20to%20Data%20Structures/175911.jpg)
    
    **Ω Notation (Big Omega) — Lower Bound:**
    
    - Denotes the **best case** of an algorithm.
    - Expressed as Ω(g(n)).
    - Definition: f(n) = Ω(g(n)) iff there exist positive constants c and n₀ such that f(n) ≥ c·g(n) for all n ≥ n₀, c > 0, n₀ ≥ 1
    - **Diagram (lower bound):** f(n) stays above the curve c·g(n) for all n once n ≥ n₀ — cg(n) forms a floor below f(n) from n₀ onward.
    
    ![175912.jpg](Introduction%20to%20Data%20Structures/175912.jpg)
    
    **Ɵ Notation (Big Theta) — Tight Bound:**
    
    - Denotes **both** upper and lower bounds — the **average case**.
    - Expressed as Ɵ(g(n)).
    - Definition: f(n) = Ɵ(g(n)) iff there exist positive constants c₁, c₂, n₀ such that c₁·g(n) ≤ f(n) ≤ c₂·g(n) for all n ≥ n₀, c₁, c₂ > 0, n₀ ≥ 1
    - **Diagram (tight bound):** f(n) is sandwiched between c₁·g(n) (lower) and c₂·g(n) (upper) for all n once n ≥ n₀.
    
    ![175913.jpg](Introduction%20to%20Data%20Structures/175913.jpg)
    
    **Relations between O, Ω, Ɵ:**
    
    - All three notations describe how f(n) behaves relative to some reference function g(n), just from different sides:
        - **O(g(n))** → f(n) is bounded *above* (worst case)
        - **Ω(g(n))** → f(n) is bounded *below* (best case)
        - **Ɵ(g(n))** → f(n) is bounded *both above and below* (average/tight case — combines O and Ω)
    - Visually: the O graph shades the region above f(n) up to cg(n); the Ω graph shades the region below f(n) down to cg(n); the Ɵ graph shades the narrow band between c₁g(n) and c₂g(n) that contains f(n) — showing Ɵ as the intersection of O and Ω.