# Explained

---

## PART 1: THE ABSOLUTE BASICS

### 1.1 What is a Linked List?

A **linked list** is a linear data structure where elements (called **nodes**) are not stored in contiguous memory. Instead, each node stores:

1. **Data** — the actual value
2. **Link/Pointer** — the address of the next node

```
[5|•]→[10|•]→[20|•]→[1|NULL]
 ↑
HEAD
```

- `HEAD` is a pointer that always points to the first node.
- The last node's pointer is `NULL` — this marks the end.
- If `HEAD == NULL`, the list is empty.

**Why does this matter?** Arrays need a contiguous block of memory decided in advance. Linked lists grab memory node-by-node, wherever it's free, and "link" them together. This is the single idea everything else builds on.

### 1.2 Array vs Linked List (know this cold — very common exam question)

| Feature | Array | Linked List |
| --- | --- | --- |
| Size | Fixed, resizing is expensive | Dynamic — grows/shrinks as needed |
| Insert/Delete | Expensive — elements shift | Cheap — just change pointers, no shifting |
| Access | Random access, O(1) via index | No random access — must traverse, O(n) |
| Memory waste | Wasted if array not full | No waste — allocated exactly as needed |
| Sequential access | Fast (contiguous memory → cache-friendly) | Slower (nodes scattered in memory) |
| Extra memory | None | Needs extra space for pointers |

**Rule of thumb:** Choose arrays when you need fast lookups by index. Choose linked lists when you're inserting/deleting a lot, especially at the front or middle.

### 1.3 The Four Types of Linked Lists

1. **Singly Linked List (SLL)** — each node points only to the next node.
2. **Doubly Linked List (DLL)** — each node points to both next and previous.
3. **Singly Circular Linked List (SCLL)** — last node points back to the first (a loop).
4. **Doubly Circular Linked List (DCLL)** — circular + bidirectional.

---

## PART 2: SINGLY LINKED LIST (SLL) — DEEP DIVE

### 2.1 Node Structure in C

```c
struct node {
    int data;
    struct node *next;
};
typedef struct node * nodeptr;
nodeptr list = NULL;   // empty list to start
```

- `struct node *next` is the pointer that "links" this node to the next one.
- `typedef` just lets us write `nodeptr` instead of `struct node *` everywhere — cleaner code.

### 2.2 The Five Basic Operations

Every linked list problem is built from these five operations. Master these and you can solve almost anything.

#### (a) Create / Build the list

```c
nodeptr create(nodeptr list) {
    int n, i;
    nodeptr newnode, curr;
    printf("How many elements:");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("Enter number : ");
        scanf("%d", &newnode->data);
        newnode->next = NULL;
        if (list == NULL) {
            list = curr = newnode;      // first node ever
        } else {
            curr->next = newnode;       // attach new node at the end
            curr = newnode;             // move curr forward
        }
    }
    return list;
}
```

**Line-by-line logic:**

- `malloc` grabs memory for one new node on the heap.
- `newnode->next = NULL` — always terminate the new node first, before linking it in.
- `curr` is a "tail pointer" — it always tracks the last node so we can attach quickly instead of re-traversing every time.

#### (b) Display / Traverse

```c
void display(nodeptr list) {
    nodeptr curr;
    for (curr = list; curr != NULL; curr = curr->next) {
        printf("%d\n", curr->data);
    }
}
```

This is the **traversal pattern** — you'll reuse `for(curr=list; curr!=NULL; curr=curr->next)` in almost every SLL function. Memorize this skeleton.

#### (c) Search

```c
void search(nodeptr list) {
    nodeptr curr;
    int i, r;
    printf("Enter element to search:");
    scanf("%d", &r);
    for (i = 1, curr = list; curr != NULL; curr = curr->next, i++) {
        if (curr->data == r) {
            printf("%d found at %d position!!!", r, i);
            return;
        }
    }
    printf("%d not found!!!", r);
}
```

Standard linear search — O(n), since we can't jump to an index like an array.

#### (d) Insert — 3 cases, this is where most people get confused

**Case 1: Insert at the beginning**

- Make `newnode->next` point to the current first node (old head).
- Make `list` (head pointer) point to `newnode`.
- **Order matters**: always link the new node first, *then* move the head — otherwise you lose the rest of the list.

**Case 2: Insert at the end**

- Traverse to the last node (the one whose `next == NULL`).
- Set `lastnode->next = newnode`, and `newnode->next = NULL`.

**Case 3: Insert at any position (general case)**

- Traverse to the node *just before* the target position (`curr`).
- `newnode->next = curr->next;`
- `curr->next = newnode;`
- Again — connect the new node forward **before** you break the old link, or you'll lose the tail of the list.

```c
nodeptr add(nodeptr list) {
    nodeptr newnode, curr = list;
    int i, pos;
    printf("Enter position:");
    scanf("%d", &pos);
    newnode = (struct node *)malloc(sizeof(struct node));
    printf("Enter number : ");
    scanf("%d", &newnode->data);
    newnode->next = NULL;

    if (list == NULL) {           // empty list — new node becomes the list
        list = newnode;
        return list;
    }
    if (pos == 1) {                // insert at beginning
        newnode->next = curr;
        list = newnode;
        return list;
    }
    // walk to the node just before 'pos'
    for (i = 1, curr = list; i < pos - 1 && curr->next != NULL; i++, curr = curr->next);
    newnode->next = curr->next;
    curr->next = newnode;
    return list;
}
```

**Why `i < pos - 1`?** Because we want `curr` to stop at the node *before* the insertion point, not at the point itself. This off-by-one detail is the #1 source of bugs — always trace it on paper with a small example (say pos = 3) before trusting the code.

#### (e) Delete — 3 cases (mirror image of insert)

**Case 1: Delete the first node**

- Move `list` to `curr->next` (the second node becomes the new head).
- Free the old first node.

**Case 2: Delete the last node**

- Traverse until `curr->next->next == NULL` (i.e., `curr` is the second-last node).
- Set `curr->next = NULL`, free the old last node.

**Case 3: Delete an intermediate node**

- Traverse to the node *before* the one you want to delete.
- "Skip over" it: `curr->next = curr->next->next;`
- Free the skipped node.

```c
nodeptr del(nodeptr list) {
    nodeptr curr = list, curr1;
    int i, pos;
    printf("Enter position to delete:");
    scanf("%d", &pos);
    if (list == NULL) { printf("List is empty"); return list; }

    if (pos == 1) {
        list = curr->next;
        free(curr);
        return list;
    }
    for (i = 1, curr = list; i < pos - 1 && curr->next != NULL; i++, curr = curr->next);
    if (curr->next == NULL) { printf("Position out of range"); return list; }
    curr1 = curr->next;
    curr->next = curr1->next;   // bypass the node to delete
    free(curr1);                // then free it
    return list;
}
```

**Golden rule for delete:** Always re-link the pointers *before* you `free()` the node. If you free first, you lose the address needed to fix the link — this causes memory corruption.

### 2.3 SLL Advantages / Disadvantages (exam-favorite)

**Advantages:**

- Easy insertion/deletion, no shifting of elements
- No wasted space — allocated exactly as needed
- Dynamic size — grows/shrinks freely
- Doesn't need contiguous memory

**Disadvantages:**

- Extra memory used for storing pointers
- No random access — must traverse from the head every time
- Can only traverse forward, never backward
- Sorting is harder than with arrays

---

## PART 3: DOUBLY LINKED LIST (DLL)

### 3.1 Structure

```c
struct node {
    int data;
    struct node *next;
    struct node *prev;   // NEW: points backward too
};
```

```
NULL ← [prev|5|next] ⇄ [prev|10|next] ⇄ [prev|20|next] → NULL
```

Each node now has **two pointers** — `next` and `prev`. This is the entire difference from SLL; every operation just needs one extra line to also fix the `prev` pointer.

### 3.2 Create

Same as SLL, but add:

```c
newnode->next = newnode->prev = NULL;
...
curr->next = newnode;
newnode->prev = curr;   // the new backward link
curr = newnode;
```

### 3.3 Insert at position (general case)

```c
newnode->next = curr->next;
newnode->prev = curr;
curr->next->prev = newnode;   // fix the backward link of the node ahead
curr->next = newnode;
```

**Pattern to remember:** In a DLL, every insert/delete touches **4 pointers** instead of 2 (SLL). Draw it out: newnode's next & prev, and the neighbors' next/prev that now point to newnode.

### 3.4 Delete at position

```c
curr1 = curr->next;
curr->next = curr1->next;
curr1->next->prev = curr;    // fix backward link of the node after the deleted one
free(curr1);
```

### 3.5 DLL Advantages / Disadvantages

**Advantages:**

- Traverse both directions (forward and backward)
- Deletion is easier — you don't need a separate "curr" trailing pointer since `prev` already gives you the previous node
- Easy to reverse (just swap next/prev at every node)

**Disadvantages:**

- Extra memory for the `prev` pointer
- More pointers to update → slower operations, more chances of bugs

---

## PART 4: CIRCULAR LINKED LISTS

### 4.1 The Core Idea

Instead of the last node pointing to `NULL`, it points back to the **first node** — forming a circle. Two flavors:

1. **Singly Circular (SCLL):** last node's `next` → first node.
2. **Doubly Circular (DCLL):** SCLL + backward links too.

```
   →[10]→[20]→[40]→[55]→[70]→
   ↑____________________________|
```

### 4.2 Key Code Differences from SLL

The traversal condition changes from `curr != NULL` to `curr->next != list` (because there's no NULL to stop at):

```c
void display(nodeptr list) {
    nodeptr curr;
    for (curr = list; curr->next != list; curr = curr->next) {
        printf("%d\n", curr->data);
    }
    printf("%d\n", curr->data);  // print the last node too — loop stops one short
}
```

Notice the extra `printf` after the loop — since the loop condition excludes the last node (to avoid infinite looping), you print it separately.

**Creating the circle:** whenever a new node is added, its `next` must be set to `list` (the head), not `NULL`:

```c
newnode->next = list;
```

**Deleting the first node** is the trickiest part of SCLL — you must first find the *last* node (since it's the one pointing to the first) and re-point it to the new head:

```c
for (curr = list; curr->next != list; curr = curr->next);  // find last node
curr->next = curr1->next;   // last node now points to new head
list = curr1->next;
free(curr1);
```

### 4.3 Circular List — Advantages / Disadvantages

**Advantages:**

- From any node, you can reach any other node (SLL can't go backward at all)
- Jumping from the last node back to the first is instant — O(1), no traversal needed

**Disadvantages:**

- Harder to reverse
- Risk of **infinite loops** if you're not careful with your stopping condition
- Going "backward" one step still means looping through the *entire* list (unless it's also doubly linked)

---

## PART 5: COMPLEXITY CHEAT SHEET

| Operation | Array | SLL | DLL |
| --- | --- | --- | --- |
| Access by index | O(1) | O(n) | O(n) |
| Search | O(n) | O(n) | O(n) |
| Insert at beginning | O(n) (shift) | O(1) | O(1) |
| Insert at end (no tail ptr) | O(1) | O(n) | O(1) if tail ptr kept |
| Insert at middle | O(n) | O(n) to find + O(1) to link | O(n) to find + O(1) to link |
| Delete at beginning | O(n) (shift) | O(1) | O(1) |
| Delete at end | O(1) | O(n) | O(1) if tail ptr kept |

**Key exam insight:** the *insertion/deletion at a known position* is O(1) — it's *finding* that position that costs O(n). This distinction trips people up constantly.

---

## PART 6: PRO-LEVEL — BEYOND THE SLIDES

These are the patterns that separate "I can write the slide's code" from "I can solve any linked list problem" — common in interviews and lab vivas.

### 6.1 Reverse a Singly Linked List (iterative) — the single most-asked LL question

```c
nodeptr reverse(nodeptr list) {
    nodeptr prev = NULL, curr = list, next;
    while (curr != NULL) {
        next = curr->next;   // save the next node before we overwrite it
        curr->next = prev;   // reverse the pointer
        prev = curr;         // move prev forward
        curr = next;         // move curr forward
    }
    return prev;   // prev is now the new head
}
```

**Trace it by hand** on `1→2→3→NULL` with 3 nodes — this single dry run makes the logic click permanently. Time: O(n), Space: O(1).

### 6.2 Find the Middle Node (Slow/Fast Pointer / "Tortoise and Hare")

```c
nodeptr findMiddle(nodeptr list) {
    nodeptr slow = list, fast = list;
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;        // moves 1 step
        fast = fast->next->next;  // moves 2 steps
    }
    return slow;   // when fast reaches the end, slow is at the middle
}
```

This "two-pointer" trick is used everywhere — cycle detection, middle node, nth-from-end, palindrome check.

### 6.3 Detect a Cycle (Floyd's Cycle Detection Algorithm)

```c
int hasCycle(nodeptr list) {
    nodeptr slow = list, fast = list;
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->next;
        if (slow == fast) return 1;   // they met → cycle exists
    }
    return 0;   // fast hit NULL → no cycle
}
```

**Why it works:** if there's a loop, the fast pointer (2 steps) will eventually "lap" the slow pointer (1 step) inside the loop — like two runners on a circular track.

### 6.4 Find nth Node from the End (one-pass, no length counting)

```c
nodeptr nthFromEnd(nodeptr list, int n) {
    nodeptr first = list, second = list;
    for (int i = 0; i < n; i++) first = first->next;   // move first n steps ahead
    while (first != NULL) {
        first = first->next;
        second = second->next;
    }
    return second;   // second is now n nodes from the end
}
```

### 6.5 Merge Two Sorted Linked Lists

```c
nodeptr merge(nodeptr a, nodeptr b) {
    nodeptr dummy = (nodeptr)malloc(sizeof(struct node));
    nodeptr tail = dummy;
    while (a != NULL && b != NULL) {
        if (a->data <= b->data) { tail->next = a; a = a->next; }
        else                    { tail->next = b; b = b->next; }
        tail = tail->next;
    }
    tail->next = (a != NULL) ? a : b;   // attach whatever's left
    nodeptr result = dummy->next;
    free(dummy);
    return result;
}
```

**The "dummy node" trick** is a pro technique: instead of special-casing "is this the first node I'm adding?", you start with a throwaway dummy node and just return `dummy->next` at the end. This eliminates a whole class of edge-case bugs — use it whenever you're *building* a list node by node.

### 6.6 Detect and Remove Duplicates (unsorted SLL)

```c
void removeDuplicates(nodeptr list) {
    nodeptr curr = list, runner, temp;
    while (curr != NULL) {
        runner = curr;
        while (runner->next != NULL) {
            if (runner->next->data == curr->data) {
                temp = runner->next;
                runner->next = runner->next->next;
                free(temp);
            } else {
                runner = runner->next;
            }
        }
        curr = curr->next;
    }
}
```

This is O(n²) with two pointers, no extra space. (A hash-set approach gets it to O(n) time but O(n) space — good to mention if asked "can you optimize this?")

### 6.7 Common Viva / Interview Questions to Be Ready For

1. Why can't you binary search a linked list? *(No O(1) random access — you can't jump to the middle index directly.)*
2. How do you find if a linked list has a loop, and then find where the loop **starts**? *(Floyd's algorithm — after slow/fast meet, reset one pointer to head, move both one step at a time; they meet at the loop's start. Good to know this exists even if not asked to code it.)*
3. Why use a **dummy/sentinel node**? *(Removes special-casing for "empty list" or "inserting at head".)*
4. SLL vs DLL vs Array — when would you pick each? *(Array: frequent lookups by index. SLL: frequent inserts/deletes at the front, memory-constrained. DLL: need to traverse both directions or delete a node without knowing its predecessor.)*
5. What happens if you `free()` a node before updating the pointers around it? *(You lose the address needed to relink → memory leak / dangling pointer / crash.)*

---

## PART 7: HOW TO ACTUALLY GET GOOD AT THIS (practical study plan)

1. **Don't memorize code — memorize the pattern.** Every SLL function is built from the same skeleton: declare `curr`, loop with `curr->next` checks, handle the "empty list" edge case first.
2. **Draw boxes and arrows on paper** for every operation before coding it. Linked list bugs are almost always "I updated pointers in the wrong order" — drawing catches this instantly.
3. **Always ask: "empty list? first node? last node?"** before writing any insert/delete function. These are the 3 edge cases that break naive code.
4. **Trace your own code by hand** with a 3-node example before running it — this is faster than debugging after the fact.
5. **Once SLL insert/delete/reverse feel automatic**, move to DLL (just "SLL + one more pointer to maintain"), then circular (just "change the stopping condition").

You now have everything from your slides *plus* the interview/pro-level patterns (reverse, cycle detection, dummy nodes, two-pointer technique) that go beyond what's typically taught in a first DSA course. Practice writing these five from memory — SLL insert/delete, reverse, cycle detection, merge — and you'll be ahead of most of your batch.