# Python_Viva_MCQ_Deep_Prep

## Python Viva + MCQ Deep Prep

Introduction to Python → Tuples (Full Syllabus Coverage)
Prepared for Avadhut Chavan

How to Use This Guide

1. Introduction to Python
2. Identifiers & Keywords
3. Lines, Indentation, Quotes, Comments, Statements
4. Operators
5. Reserved Words Table (Reference)
6. Variables & Data Types
7. Conditional Statements
8. range() Function
9. Loops - for and while
10. Strings
11. Lists
12. Tuples - YOUR LAST TOPIC (go deepest here)
MASTER MCQ BANK (50 Questions, Grouped by Topic, With Answers)
Final Rapid-Fire Round (Self-Quiz Before the Test)

## How to Use This Guide

- Viva sections - read the explanation once, then cover it and explain out loud in your own words. Oral examiners reward clarity, not memorized definitions.
- “Why it matters” notes - these are the follow-up questions examiners ask after your first answer. Prepare them too.
- Code + Output pairs - trace through every line mentally before checking the output. This is exactly how MCQ “predict the output” questions work.
- MCQs - grouped by topic, so you can test yourself topic-by-topic instead of only at the end.

## 1. Introduction to Python

## Core Facts

- Python is general-purpose, interpreted, interactive, object-oriented, and high-level.
- Created by Guido van Rossum, developed 1985-1990 at the National Research Institute for Mathematics and Computer Science, Netherlands.
- Released under the GPL (General Public License), like Perl.
- Designed for readability - uses English keywords, minimal punctuation compared to C/Java.
- Still maintained by a core development team; Guido van Rossum retains a guiding role.

## Features (explain each in 1 line)

| Feature | Meaning |
| --- | --- |
| Interpreted | Code runs line-by-line via an interpreter; no separate compile step |
| Interactive | You can type commands directly at the Python prompt and get immediate results |
| Object-Oriented | Supports classes, objects, encapsulation |
| Beginner-friendly | Simple syntax, used from scripting to web development to games |
| Cross-platform | Same code runs on Windows, Linux, macOS |
| High-level | Abstracts away memory management, closer to human language than machine code |

Why it matters (follow-up Qs): “Why is Python called interpreted?” → Because the Python interpreter executes source code directly, translating and running it line-by-line at runtime, instead of compiling the whole program to machine code first like C/C++. -“Name 3 languages Python borrowed ideas from.” → ABC, Modula-3, C, C++, Algol-68, Smalltalk, Unix shell.

## 2. Identifiers & Keywords

## Identifiers

- An identifier names a variable, function, class, module, or other object.
- Rules:
○ Must start with a letter (A-Z, a-z) or underscore _ .
○ Followed by any number of letters, digits, or underscores.
    - Cannot start with a digit.
    ○ Cannot contain special symbols like ! @ # $ %.
- Python is case-sensitive: Manpower and manpower are different identifiers.

## Naming Conventions

- Class names → start with uppercase (e.g., Student ).
- All other identifiers (variables, functions) → start with lowercase (e.g., student_name ).
- _name (single leading underscore) → convention for a private identifier.
- __name (double leading underscore) → strongly private, triggers name-mangling.
- $\_\_\_\_$ name $\_\_\_\_$ (leading + trailing double underscore) → language-defined special name (a “dunder”, e.g., $\_\_\_\_$ init $\_\_\_\_$ , $\_\_\_\_$ main $\_\_\_\_$ ).

## Keywords

- Reserved words that cannot be used as identifiers.
- Python 3 has 35 keywords (the PPT says 33, based on an older version - mention “33+ depending on version” if asked, since the exact count changes across Python 3.x releases).
- All keywords are lowercase except True , False , and None .

Full keyword list to recognize: and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield, True, False, None

Why it matters: - “Can class be a variable name?” → No, it’s a reserved keyword. - “What does __init_ mean?” → It’s a special/dunder method - the constructor, automatically called when an object is created.

## 3. Lines, Indentation, Quotes, Comments, Statements

## Indentation

- Python has no braces {} for blocks - indentation itself defines a block.
- All statements inside one block must have the same indentation (spaces or tabs, but be consistent).
- Wrong/inconsistent indentation → IndentationError .

```
if True:
    print("True")
    print("India")
else:
    print("False")
```

## Multi-line statements

- A statement normally ends at a newline.
- Backslash = line continuation character.

```
total = item1 + \
    item2 + \
    item3
```

- Not needed inside [] , {} , () — brackets allow natural line breaks.

## Quotations

- Single ‘…’, double “…”, and triple ’’‘…’’’ / “““…”“” are all valid for strings.
- Start and end quote type must match.
- Triple quotes are used for strings that span multiple lines.

## Comments

- # starts a comment - everything after it (until end of line) is ignored by the interpreter.
- No native block-comment symbol; use # on every line, or a triple-quoted string as an (unofficial) multi-line comment.

## Multiple statements on one line

- Semicolon ; separates statements: $\mathrm{x}=$ “MIT”; $\mathrm{y}=20$

## Suites (compound statements)

- A suite = group of individual statements forming one code block.
- Compound statements ( if , while , def , class ) need:
    1. A header line ending in :
1. One or more indented lines forming the suite.

```
if expression:
        suite
elif expression:
        suite
else:
        suite
```

## 4. Operators

The 7 Operator Categories

1. Arithmetic
2. Assignment
3. Comparison (Relational)
4. Logical
5. Bitwise
6. Identity
7. Membership

Arithmetic Operators

| Op | Meaning | Example |
| --- | --- | --- |
| + | Add | $\mathrm{x}+\mathrm{y}$ |
| - | Subtract | $x-y$ |
| * | Multiply | x * y |
| / | Divide (always float) | x / y |
| % | Modulus (remainder) | $x \% \mathrm{y}$ |
| // | Floor division | x // y |
| ** | Exponent | x ** y |

Assignment Operators

| Op | Equivalent |
| --- | --- |
| = | $\mathrm{c}=\mathrm{a}+\mathrm{b}$ |
| += | c = c + a |
| -= | c = c - a |
| *= | c = c * a |
| /= | c = c / a |
| %= | c = c % a |

Comparison Operators

```
> < == != >= <= - all return True / False .
```

Logical Operators

| Op | Meaning |
| --- | --- |
| and | True if both operands are true |
| or | True if either operand is true |
| not | Reverses the boolean value |

```
a = 10; b = 5
if a > 5 and b < 10:
    print("Both conditions are true")
age = 20; citizen = True
if age >= 18 and citizen:
    print("Eligible to vote")
x = False
if not x:
    print("Condition is reversed")
```

| Op | Meaning |
| --- | --- |
| & | AND |
| } | OR |
| ~ | NOT (complement) |
| ^ | XOR |
| >> | Right shift |
| << | Left shift |

Identity & Membership

- is / is not → checks if two variables point to the same object in memory (not just equal value).
- in / not in → checks membership in a sequence (string, list, tuple, etc.).

Why it matters (classic trap): - == checks value equality. is checks identity (same memory location). Two lists with the same contents are == but not always is . - / always returns a float, even $10 / 2 \rightarrow 5.0$. // returns floor result: $10 / / 3 \rightarrow 3$, and -7//2 → -4 (floors toward negative infinity, not toward zero - a common trick question).

## 5. Reserved Words Table (Reference)

| and | exec | not |
| --- | --- | --- |
| assert | finally | or |
| break | for | pass |
| class | from | print |
| continue | global | raise |
| def | if | return |
| del | import | try |
| elif | in | while |
| else | is | with |
| except | lambda | yield |

(Note: exec and print were keywords in Python 2; in Python 3 they are built-in functions, not reserved words. If your examiner is testing Python 3 specifically, be ready to mention this distinction - it shows deeper understanding.)

## 6. Variables & Data Types

Variables

- Variables = reserved memory locations to store values.
- No explicit declaration needed - type is inferred automatically when a value is assigned (this is called dynamic typing).
- = assigns: left side = variable name, right side = value.

```
counter = 100 # integer
counter = 100.10 # float (reassignment allowed - dynamic typing)
name = "John" # string
```

Multiple Assignment

```
a = b = c = 1 # all three point to the SAME object (value 1)
a, b, c = 1, 2, "John" # different objects assigned individually
```

Standard Data Types (5 core ones from the PPT)

1. Numbers
2. String
3. List
4. Tuple
5. Dictionary
(Modern Python also treats Boolean and Set as standard types - worth mentioning if asked “is that all the data types?”)

Numbers

- Created the moment you assign a numeric value: var1 = 10 .
- Deleted using del : del var1 or del var1, var2 .
- Four numeric types (per the PPT, which reflects Python 2 terminology):
○ int - signed integers
○ long - long integers (Python 2 only; Python 3 merged long into int )
○ float - floating point real values
○ complex - complex numbers (e.g., 3+4j )

Why it matters: - “Does Python 3 have a long type?” → No - this is a great “gotcha” answer to have ready. In Python 3, int has unlimited precision and long was merged into it. - “Is Python statically or dynamically typed?” → Dynamically typed - variable types are determined at runtime, and a variable can be reassigned to a different type.

## 7. Conditional Statements

if

```
if x > 0:
    print("Positive")
```

if-else

```
if x % 2 == 0:
    print("Even")
else:
    print("Odd")
```

Nested if

```
num = 10
if num > 0:
    if num % 2 == 0:
        print("Positive and Even")
```

elif ladder

```
marks = 85
if marks >= 75:
    print("Grade A")
elif marks >= 60:
    print("Grade B")
elif marks >= 40:
    print("Grade C")
else:
    print("Fail")
```

- Conditions are checked top to bottom; the first True branch executes and the rest are skipped.

Why it matters: - “Difference between nested-if and elif?” → Nested-if checks a second, unrelated condition only when the first is true (AND-like relationship). elif offers alternative conditions for the same decision (OR-like, mutually exclusive branches).

## 8. range() Function

Forms

| Form | Example | Produces |
| --- | --- | --- |
| range(stop) | range(5) |  |

|  |  | 01234 |
| --- | --- | --- |
| range(start, stop) | range $(1,6)$ | 12345 |
| range(start, stop, step) | range(1,10,2) | 13579 |

Key Rules

- Start is inclusive, stop is exclusive.
- Step is optional, defaults to 1 .
- range() returns a range object, not a list - it generates numbers lazily (memory-efficient, doesn’t store the whole sequence).
- Negative step → counts downward: range(5, 0, -1) → 54321 .

```
for i in range(5):
    print(i)
```

Why it matters: - “Why doesn’t range() create a full list in memory?” → It’s a lazy sequence - generates each value on demand, saving memory for large ranges (important for millions of iterations).

## 9. Loops - for and while

for loop

```
for i in range(1, 6):
    print(i * i)
```

break, continue, pass

```
for i in range(5):
    if i == 3:
        break # exits loop entirely
    print(i)
for i in range(5):
    if i == 2:
        continue # skips this iteration only
    print(i)
for i in range(5):
    pass # does nothing - placeholder
```

Nested for

```
for i in range(1, 4):
    for j in range(1, 3):
        print(i, j)
```

else with for loop

```
for i in range(3):
    print(i)
else:
    print("Loop completed") # runs only if loop finishes WITHOUT break
```

while loop

```
i = 1
while i <= 5:
    print(i)
    i += 1
```

while with break/continue

```
i = 1
while i <= 5:
    if i == 3:
        break
    print(i)
    i += 1
```

## while with else

```
i = 1
while i <= 3:
    print(i)
    i += 1
else:
    print("Loop finished") # runs if while completes normally
```

Why it matters: - “break vs continue vs pass - in one line each?” - break → exits the loop completely. - continue → skips the rest of the current iteration, jumps to next. - pass → does nothing; a syntactic placeholder (used when a statement is syntactically required but no action is needed). - “When does the else clause of a loop NOT execute?” → When the loop is terminated early by a break . - “What if while True: has no break?” → Infinite loop - runs forever (a common bug to be aware of).

## 10. Strings

Basics

- A string = contiguous sequence of characters in quotes (single or double).
- Indexing: word[0] (first char), word[-1] (last char) - negative indices count from the end.
- Slicing: string[start:end:step] - start inclusive, end exclusive.

```
word = "Python"
print(word[0]) # P
print(word[-1]) # n
```

## Concatenation & Repetition

```
first = "Data"; second = "Science"
result = first + " " + second # "Data Science"
print("Hi" * 2) # "HiHi"
```

## Length & Common Methods

```
course = "Machine Learning"
print(len(course)) # 17
msg = "python programming"
print(msg.upper()) # PYTHON PROGRAMMING
print(msg.capitalize()) # Python programming
print(msg.replace("python", "java")) # java programming
```

## Slicing Deep Dive

```
text = "PythonProgramming"
print(text[0:6]) # Python
print(text[6:17]) # Programming
text = "Artificial Intelligence"
print(text[:10]) # Artificial (no start = from beginning)
print(text[11:]) # Intelligence (no end = till the end)
text = "MachineLearning"
print(text[-8:]) # Learning (negative index slicing)
print(text[:-8]) # Machine
text = "Programming"
print(text[::2]) # Pormig (every 2nd character)
print(text[1::1]) # rogramming
```

## Reverse & Formatting

```
text = "Python"
print(text[::-1]) # nohtyP
name = "Sachin"; subject = "Python"
print(f"My name is {name} and I teach {subject}")
```

Why it matters: - “Are strings mutable?” → No. word[0] = ‘X’ raises a TypeError . Any “modification” (like .replace() ) actually returns a new string. - “What does text [::2] mean exactly?” → Start and end are omitted (whole string), step = 2, so it picks every second character starting from index 0.

## 11. Lists

What is a List?

- Ordered, mutable collection defined with .
- Can store heterogeneous data types (mixed int, string, float, etc. in one list).
- 0-indexed; supports negative indexing and slicing.
- + = concatenation, * = repetition (same as strings).

```
my_list = [10, 20, 30, "Python", 3.14]
numbers = [1, 2, 3, 4]
names = ["Alice", "Bob"]
empty_list = []
```

Characteristics (rapid-fire for viva)

- Ordered ✓
- Mutable ✓
- Allows duplicates ✓
- Indexed (0-based) ✓
- Mixed data types ✓

Accessing & Slicing

```
data = [10, 20, 30, 40]
print(data[0]) # 10
print(data[-1]) # 40
data = [1, 2, 3, 4, 5]
print(data[1:4]) # [2, 3, 4]
```

Updating

```
data = [10, 20, 30]
data[1] = 25
print(data) # [10, 25, 30]
```

Adding Elements

```
data.append(40) # adds single element at end
data.insert(1, 15) # adds element at specific index
data.extend([50, 60]) # adds multiple elements
```

Removing Elements

```
data.remove(20) # removes first matching VALUE
data.pop() # removes & returns LAST element
data.pop(1) # removes & returns element at index 1
del data[0] # deletes by index, no return value
```

## Full Method Reference

| Method | What it does |
| --- | --- |
| append(x) | Add one element at the end |
| insert(i, x) | Insert element at index i |
| extend(iterable) | Add multiple elements from another list |
| remove(x) | Remove first occurrence of value x |
| pop([i]) | Remove & return element at index i (default: last) |
| clear() | Remove all elements |
| index(x) | Return index of first occurrence of x |
| count(x) | Count occurrences of x |
| sort() | Sort ascending in-place ( reverse=True for descending) |
| reverse() | Reverse the list in-place |
| copy() | Return a shallow copy |

```
data = [10, 20, 30, 40]
data.clear()
print(data) # []
data = [10, 20, 30, 20, 40]
print(data.index(20)) # 1 (first occurrence)
print(data.count(20)) # 2
numbers = [40, 10, 30, 20]
numbers.sort()
print(numbers) # [10, 20, 30, 40]
numbers.sort(reverse=True)
print(numbers) # [40, 30, 20, 10]
original = [10, 20, 30]
duplicate = original.copy()
duplicate.append(40)
print(original) # [10, 20, 30] -- unaffected
print(duplicate) # [10, 20, 30, 40]
```

## List Comprehension

Structure: new_list = [expression for item in iterable if condition]

```
squares = [x*x for x in range(1, 6)]
print(squares) # [1, 4, 9, 16, 25]
evens = [x for x in range(1, 11) if x % 2 == 0]
print(evens) # [2, 4, 6, 8, 10]
result = ["Even" if x % 2 == 0 else "Odd" for x in range(1, 6)]
print(result) # ['Odd','Even','Odd','Even','Odd']
even_squares = [x*x for x in range(1, 11) if x % 2 == 0]
```

Why it matters: - “What’s the advantage of list comprehension over a for-loop?” → Shorter, more readable, and typically faster since it’s optimized internally by the interpreter. - “What’s the difference between remove() and pop() ?” → remove(x) deletes by value (first match); pop(i) deletes by index and returns the removed item, while remove() returns nothing. - “Is original.copy() a deep or shallow copy?” → Shallow - nested mutable objects inside are still shared between original and copy.

## 12. Tuples - YOUR LAST TOPIC (go deepest here)

What is a Tuple?

- A tuple is a sequence type similar to a list, but:
○ Lists use and are mutable.
○ Tuples use ( ) and are immutable (cannot be changed after creation).
- Ordered, allows duplicate values.

```
t = (10, 20, 30)
print(t)
```

## List vs Tuple - Master This Table

| Feature | List | Tuple |
| --- | --- | --- |
| Mutable | Yes | No |
| Syntax | [ ] | ( ) |
| Speed | Slower | Faster |
| Safety | Less (can be changed accidentally) | More (data integrity guaranteed) |
| Use case | Data that changes | Fixed/constant data (coordinates, DB records) |

## Accessing Elements

```
t = (10, 20, 30, 40)
print(t[0]) # 10
print(t[-1]) # 40
numbers = (10, 20, 30, 40, 50, 60, 70)
print(numbers[1:5]) # (20, 30, 40, 50)
print(numbers[:4]) # (10, 20, 30, 40)
print(numbers[3:]) # (40, 50, 60, 70)
```

Indexing and slicing work exactly like lists - this is the easiest connection to make in a viva answer.

## Immutability - Deep Dive

```
t = (1, 2, 3)
t[0] = 100 # (TypeError): 'tuple' object does not support item assignment
t = (1, 2, 3)
t = t + (4, 5) # (allowed) - creates a brand NEW tuple, doesn't modify original
print(t) # (1, 2, 3, 4, 5)
```

Key insight for viva: $t=t+(4,5)$ looks like modification, but it isn’t - Python builds an entirely new tuple object and reassigns the name t to it. The original (1,2,3) tuple object is discarded (garbage collected), not changed.

## The Single-Element Tuple Trap

```
x = (5) # this is just an INTEGER in parentheses, NOT a tuple!
type(x) # <class 'int'>
t = (5,) # the trailing comma makes it a tuple
type(t) # <class 'tuple'>
```

This is one of the most common MCQ/viva trick questions on tuples.

## Iterating Through a Tuple

```
t = (10, 20, 30)
for i in t:
    print(i)
# Using while loop with index
t = (10, 20, 30)
i = 0
while i < len(t):
    print(t[i])
    i += 1
```

## Built-in Tuple Functions

```
t = (5, 2, 8, 2)
print(len(t)) # 4 - number of elements
print(max(t)) # 8 - largest value
```

```
print(min(t)) # 2 - smallest value
print(t.count(2)) # 2 - occurrences of value 2
print(t.index(8)) # 2 - index of first occurrence of value 8
```

Note: tuples only have two built-in methods — count() and index() — because they’re immutable (no append, remove, sort, etc.).

## Packing & Unpacking

```
t = (10, 20, 30) # Packing - combining values into a tuple
a, b, c = t # Unpacking - extracting values into variables
print(a, b, c) # 10 20 30
student = ("Rahul", 20, "Pune")
name, age, city = student
print(name) # Rahul
print(age) # 20
print(city) # Pune
```

Rule: number of variables on the left must match the number of elements in the tuple (unless you use * for extended unpacking, e.g., a, *rest = t ).

## Swapping Two Variables - Classic Viva Question

```
a = 10
b = 20
a, b = b, a
print("a =", a) # a = 20
print("b =", b) # b = 10
```

Why it works: Python evaluates the entire right-hand side (b, a) as a tuple first, then unpacks it into a, b - so no temporary variable is needed, unlike in C/Java.

## Sum and Average of a Tuple

```
marks = (70, 80, 90, 85, 75)
total = sum(marks)
average = total / len(marks)
print("Total =", total) # 400
print("Average =", average) # 80.0
```

(Note: the PPT slide had del sum before this, which would delete the built-in sum function - that line should NOT be included, it’s a slide typo. Flag this if your teacher asks - it shows you’re thinking critically, not just memorizing.)

## Conversions

```
numbers = [10, 20, 30, 40]
t = tuple(numbers) # list -> tuple
print(t) # (10, 20, 30, 40)
t = (5, 10, 15, 20)
l = list(t) # tuple -> list
print(l) # [5, 10, 15, 20]
```

## Nested Tuples

```
students = (
    ("Rahul", 80),
    ("Sneha", 90),
    ("Amit", 85)
)
for name, marks in students:
    print(name, marks)
```

Each inner tuple gets automatically unpacked into name, marks during iteration.

## Zipping Tuples

```
names = ("Amit", "Rahul", "Sneha")
marks = (80, 90, 85)
result = tuple(zip(names, marks))
print(result)
# (('Amit', 80), ('Rahul', 90), ('Sneha', 85))
```

zip() pairs elements from multiple iterables positionally (1st with 1st, 2nd with 2nd…) and stops at the shortest iterable if lengths differ.

## Full Tuple Viva Q&A Bank

- Q: Why use a tuple instead of a list? A: Tuples are faster (less overhead since Python doesn’t need to allow for resizing), safer (data can’t be accidentally modified), and are commonly used for fixed collections like coordinates ( $\mathrm{x}, \mathrm{y}$ ) , RGB values, or function return values with multiple items.
- Q: Can a tuple contain mutable objects like a list? A: Yes - e.g., $\mathrm{t}=(1,2,[3,4])$. The tuple itself is immutable (you can’t reassign t[2] ), but the list inside it can still be modified ( t[2].append(5) works). This is an advanced point that impresses examiners.
- Q: How do you create an empty tuple? A: $\mathrm{t}=()$
- Q: What is tuple packing? A: Assigning multiple comma-separated values to one variable name automatically creates a tuple: t = 10, 20, 30 also works without explicit parentheses.
- Q: Is $(1,2,3)==(1,2,3)$ True? A: Yes - tuples compare by value, element by element.

## MASTER MCQ BANK (50 Questions, Grouped by Topic, With Answers)

## A. Basics & Identifiers

1. Who created Python? a) Dennis Ritchie b) James Gosling c) Guido van Rossum d) Bjarne Stroustrup
2. Python source code is released under: a) MIT License b) GPL c) Apache d) BSD
3. Which is a valid identifier? a) 2value b) **_value2** c) value-2 d) value#2
4. Which of these is NOT a Python keyword? a) class b) import c) value d) lambda
5. $\_\_\_\_$ init $\_\_\_\_$ is an example of: a) A syntax error b) A dunder/special method c) A private variable d) A keyword
6. Python identifiers are: a) Case-insensitive b) Case-sensitive c) Numeric only d) Always lowercase

## B. Structure - Indentation, Comments, Quotes

1. Python blocks are defined by: a) Curly braces b) Indentation c) Parentheses d) Semicolons
2. Which symbol starts a single-line comment? a) // b) /* c) # d) –
3. Which character allows a statement to continue on the next line? a) & b) c) % d) #
4. Triple quotes are mainly used for: a) Comments b) Multi-line strings c) Numbers d) Keywords

## C. Operators

1. Result of 10 / 3 in Python 3: a) 3 b) 3.3333… c) 3.0 d) Error
2. Result of 10 // 3 : a) 3.33 b) 3 c) 3.0 d) 1
3. Which operator checks membership in a list? a) is b) == c) in d) &
4. x is y checks: a) Value equality b) Identity (same memory object) c) Data type d) Length
5. Which is a bitwise operator? a) and b) ^ c) in d) not

## D. Variables & Data Types

1. Python variables need explicit type declaration: a) True b) False
2. Which of these is NOT one of Python’s 5 standard data types (per this syllabus)? a) Numbers b) String c) Tuple d) Boolean (bonus: Boolean IS a real type in modern Python, but not one of the 5 listed on the slide)
3. In Python 3 , the long type: a) Still exists separately b) Was merged into int c) Was removed entirely d) Became a keyword

## E. Conditionals

1. In an elif ladder, once a condition is True: a) All blocks execute b) Only that block executes, rest are skipped c) Nothing executes d) Error occurs
2. Nested if means: a) Two elif statements b) An if statement inside another if c) if with no condition d) if with multiple conditions using commas

## F. range() and Loops

1. range(1, 10, 2) generates: a) 1,2,3… 10 b) 1,3,5,7,9 c) 2,4,6,8 d) 1,10
2. In range () , the stop value is: a) Inclusive b) Exclusive c) Optional d) Always 0
3. range() returns: a) A list b) A range object c) A tuple d) A string
4. Which keyword skips only the current iteration? a) break b) continue c) pass d) return
5. The else block of a for loop executes when: a) The loop hits break b) The loop completes without break c) The loop body is empty d) Always
6. pass statement: a) Exits the loop b) Skips an iteration c) Does nothing (placeholder) d) Raises an error

## G. Strings

1. Are Python strings mutable? a) Yes b) No
2. “Python”[-1] gives: a) P b) n c) o d) Error
3. text[::-1] on a string: a) Uppercases it b) Reverses it c) Removes spaces d) Returns first half
4. “hi” * 3 gives: a) Error b) “hihihi” c) “hi3” d) 3
5. In string[start:end:step], the end index is: a) Inclusive b) Exclusive c) Optional only d) Always required

## H. Lists

1. Which is TRUE about lists? a) Immutable b) Mutable c) Fixed size d) Only same-type elements
2. Which method adds ONE element to the end? a) extend() b) append() c) insert() d) add()
3. data.pop(1) does what? a) Adds at index 1 b) Removes & returns element at index 1 c) Sorts the list d) Copies the list
4. Difference between remove() and pop() : a) No difference b) remove() deletes by value, pop() deletes by index & returns it c) pop() deletes by value d) Both need an index
5. [x*x for x in range(1,4)] produces: a) [1,2,3] b) [1,4,9] c) [1,2,3,4] d) Error
6. original.copy() creates: a) A reference to the same list b) A shallow copy c) A tuple d) An error

## I. Tuples (extra weight - this is your last & most important topic)

1. Tuples are defined using: a) b) { } c) ( ) d) < >
2. Which is TRUE about tuples? a) Mutable b) Immutable c) Unordered d) No duplicates allowed
3. What happens with $\mathrm{t}[0]=5$ on a tuple? a) Works fine b) TypeError c) Creates new tuple automatically d) Deletes tuple
4. How do you create a single-element tuple with value 5? a) (5) b) (5,) c) [5] d) tuple(5)
5. Which function converts a list to a tuple? a) list() b) tuple() c) set() d) dict()
6. $t=(10,20,30) ; a, b, c=t$ - this is called: a) Slicing b) Unpacking c) Nesting d) Zipping
7. Easiest way to swap a and b : a) Third variable required b) a, b=b, a c) swap(a,b) d) Not possible in Python
8. tuple(zip((1,2),(3,4))) gives: a) (1,2,3,4) b) ((1,3),(2,4)) c) (1,3) d) Error
9. Which built-in gives the count of a value in a tuple? a) len() b) count() c) index() d) size()
10. Speed comparison - which is generally faster? a) List b) Tuple c) Both same d) Depends on OS
11. $\mathrm{t}=(1,2,3) ; \mathrm{t}=\mathrm{t}+(4,5)$ - what happens to the original tuple object? a) It gets modified in place b) A new tuple is created; original is discarded c) Error occurs d) t becomes a list
12. Which methods does a tuple have? a) append() , remove() b) count() , index() c) sort() , reverse() d) insert() , pop()
13. $\mathrm{t}=(1,2,[3,4])$ - can you do t[2].append(5) ? a) No, tuple is immutable b) Yes - the list inside can still be modified c) Raises TypeError d) Converts t to a list

## Final Rapid-Fire Round (Self-Quiz Before the Test)

Say these out loud, no peeking: 1. Difference between is and == ? 2. Why is range() memory-efficient? 3. Why doesn’t $\mathrm{t}=\mathrm{t}+$ $(4,5)$ violate tuple immutability? 4 . What’s the trailing-comma rule for single-element tuples? 5. remove() vs pop() - one line each. 6. Swap two variables in one line using tuples. 7. Two built-in methods every tuple has. 8. Why are tuples faster than lists?

If you can answer all 8 confidently without notes, you’re ready.
Good luck for your test!