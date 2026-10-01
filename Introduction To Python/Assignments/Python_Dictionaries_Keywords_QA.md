# Python_Dictionaries_Keywords_QA

# Python Dictionaries, Keywords & Identifiers

Question & Answer Reference Notes

## 1. What is a dictionary in Python? Explain its structure.

A dictionary is Python’s built-in data structure for storing data as key-value pairs, written using curly braces. Each key maps to a specific value, and the key acts as a unique identifier used to retrieve that value quickly, similar to a real-world dictionary mapping words to meanings. Dictionaries are mutable, allowing keys and values to be added, updated, or removed after creation, and since Python 3.7 they maintain insertion order. Values can be of any data type and can repeat, but keys must be unique and immutable, making dictionaries ideal for fast lookups.

```
student = {'name': 'Rahul', 'age': 21, 'branch': 'CS'}
# keys: 'name', 'age', 'branch'
# values: 'Rahul', 21, 'CS'
```

## 2. Explain key-value pairs and rules for dictionary keys.

A key-value pair links a unique key to an associated piece of data called its value, written as key: value inside a dictionary. Keys must be unique within a dictionary; assigning a value to an existing key simply overwrites the previous value. Keys must also be immutable and hashable, so strings, numbers, and tuples are valid, but lists, sets, and dictionaries cannot be used as keys since they’re mutable and unhashable. Values, on the other hand, have no such restriction and can be of any data type, including lists, other dictionaries, or duplicate values across different keys.

```
valid = {'a': 1, 1: 'x', (1,2): 'tuple key'} # OK
# invalid = {[1,2]: 'y'} # TypeError: unhashable type: 'list'
```

## 3. Explain dictionary creation, accessing, and modification.

Dictionaries are created using curly braces with key-value pairs, e.g. {‘a’:1,‘b’:2}, or via the dict() constructor. Values are accessed using square-bracket notation with the key, such as d[‘a’], which raises a KeyError if the key doesn’t exist, or more safely through the get() method. Modification is done by assigning a value to a key: if the key already exists its value is updated, and if it doesn’t exist a new key-value pair is added automatically. This makes dictionaries flexible for both retrieving and dynamically updating structured data.

```
d = {'a': 1, 'b': 2}
d['a'] # 1 (access)
d['c'] = 3 # adds new key -> {'a':1,'b':2,'c':3}
d['a'] = 100 # updates existing key -> {'a':100,...}
```

## 4. Explain dictionary methods: keys(), values(), and items().

keys() returns a view object containing all the keys currently in the dictionary, which can be looped over or converted to a list. values() similarly returns a view of all the values stored in the dictionary, without their associated keys. items() returns a view of key-value pairs as tuples, making it the most common choice for iterating over a dictionary when both the key and value are needed together. All three return dynamic ‘view objects’ that automatically reflect any later changes made to the original dictionary.

```
d = {'a': 1, 'b': 2, 'c': 3}
d.keys() # dict_keys(['a', 'b', 'c'])
d.values() # dict_values([1, 2, 3])
d.items() # dict_items([('a',1), ('b',2), ('c',3)])
for k, v in d.items():
    print(k, v)
```

## 5. Explain get() and update() methods of dictionary.

get(key, default) retrieves the value for a given key without raising an error if the key is missing; instead it returns None, or a specified default value, making it a safer alternative to square-bracket access. update() merges another dictionary or iterable of key-value pairs into the current dictionary, adding new keys and overwriting the values of any keys that already exist. update() modifies the dictionary in place and returns None. Together, these methods allow safe reading and efficient bulk-modification of dictionary data without manual looping.

```
d = {'a': 1, 'b': 2}
d.get('a') # 1
d.get('z', 0) # 0 (default, no KeyError)
d.update({'b': 20, 'c': 3}) # {'a':1,'b':20,'c':3}
```

## 6. Differentiate between pop() and del in dictionary.

pop(key, default) removes the specified key from the dictionary and returns its value, allowing an optional default to avoid a KeyError if the key is absent, which makes it useful when you need the removed value for further use. del d[key] is a statement, not a method, that deletes a key-value pair directly but returns nothing, and it raises a KeyError if the key isn’t found unless checked beforehand. Essentially, pop() is expression-based and safer with defaults, while del is a direct, value-discarding deletion statement.

```
d = {'a': 1, 'b': 2}
val = d.pop('a') # val = 1, d = {'b': 2}
d.pop('z', 'none') # 'none' (no error)
del d['b'] # removes 'b', returns nothing
```

## 7. Explain clear() and copy() dictionary methods.

clear() removes all key-value pairs from the dictionary, leaving it as an empty dictionary {} while keeping the same object in memory rather than creating a new one. copy() returns a new, shallow copy of the dictionary,
meaning changes to the copy’s top-level keys and values won’t affect the original, though nested mutable objects inside are still shared between both. This distinction matters when working with dictionaries containing nested lists or dictionaries, where a deep copy from the copy module may be needed instead.

```
d = {'a': 1, 'b': 2}
d2 = d.copy() # {'a': 1, 'b': 2}, independent top-level copy
d.clear() # d becomes {}
print(d2) # {'a': 1, 'b': 2} (unaffected)
```

## 8. What are Python keywords? List any ten keywords.

Keywords are reserved words in Python that have a predefined meaning and special purpose in the language’s syntax, so they cannot be used as identifiers such as variable, function, or class names. Python has 35 keywords in total, and they are case-sensitive, always written in lowercase except True, False, and None. They control the language’s structure, including conditionals, loops, function definitions, exception handling, and logical operations, forming the essential grammar of every Python program.

```
import keyword
print(keyword.kwlist) # lists all keywords
# Ten examples:
# if, else, elif, for, while, def, return, import, class, try
```

## 9. Explain valid and invalid identifiers with examples.

An identifier is the name given to variables, functions, classes, or other objects in Python. Valid identifiers must start with a letter (a-z, A-Z) or an underscore, followed by any combination of letters, digits, or underscores, and cannot be a reserved keyword. They are case-sensitive, so age and Age are treated as different identifiers. Invalid identifiers include names starting with a digit, containing spaces or special characters like @ or -, or matching a Python keyword such as class or for.

```
# Valid identifiers
age = 21
_name = 'Rahul'
student1 = 'CS'
# Invalid identifiers
# 1name = 'x' -> starts with a digit
# my-name = 'x' -> contains a hyphen
# class = 'x' -> 'class' is a reserved keyword
```

## 10. Explain Python indentation and its role in program execution.

Indentation is the whitespace at the start of a line, and in Python it is not optional styling but a core part of the syntax that defines the boundaries of code blocks such as loops, conditionals, functions, and classes. Unlike languages that use curly braces to group statements, Python relies entirely on consistent indentation to determine which statements belong to which block during execution. Incorrect or mismatched indentation
causes an IndentationError and prevents the program from running at all. The standard convention is four spaces per indentation level, ensuring both readability and correct program logic.

```
def greet(name):
    if name:
        print('Hello,', name)
    else:
        print('Hello, stranger')
```

## 11. How does tuple packing and unpacking work in Python? Explain with an example.

Tuple packing is the process of combining multiple comma-separated values into a single tuple, with or without enclosing parentheses, such as point $=3,4$. Unpacking reverses this by assigning each element of a tuple to a separate variable in one statement, matching them by position, such as $\mathrm{x}, \mathrm{y}=$ point. Extended unpacking with an asterisk allows one variable to collect multiple remaining values as a list. This mechanism is widely used for returning multiple values from functions and for swapping variable values without a temporary variable.

```
point = 3, 4 # packing
x, y = point # unpacking -> x=3, y=4
a, b = 5, 10
a, b = b, a # swap using packing/unpacking -> a=10, b=5
```

1. Write a Python program to count the frequency of each word in a given sentence using a dictionary.

The program splits the input sentence into individual words using split(), which separates on whitespace by default. It then iterates through each word, using a dictionary to store words as keys and their occurrence counts as values. The get() method checks if a word already exists in the dictionary and increments its count, or initializes it to one if seen for the first time. This approach efficiently tallies word frequency in a single pass through the sentence using a dictionary’s fast key-based lookups.

```
sentence = input('Enter a sentence: ')
words = sentence.lower().split()
freq = {}
for word in words:
    freq[word] = freq.get(word, 0) + 1
for word, count in freq.items():
    print(f'{word}: {count}')
```

1. Write a Python function that takes a tuple of integers as input and returns a new tuple containing only the unique elements. Explain how tuples differ from lists in terms of memory usage and performance.

The function converts the input tuple into a set to automatically eliminate duplicate values, since sets only store unique elements, and then converts the result back into a tuple to preserve the required return type. Regarding memory and performance, tuples generally consume less memory than lists because their immutability lets Python store them more compactly and avoid overallocation for future growth, which lists reserve. Tuples are also faster to create and iterate over since the interpreter can make optimizations knowing their contents won’t change, making them preferable for fixed collections of data.

```
def unique_elements(t):
    return tuple(set(t))
nums = (1, 2, 2, 3, 4, 4, 5)
print(unique_elements(nums)) # e.g. (1, 2, 3, 4, 5)
# Note: set() does not preserve original order
```

## 14. What are dictionaries in Python? How do they differ from lists?

A dictionary is a mutable, unordered-by-key-lookup collection that stores data as key-value pairs, allowing values to be retrieved quickly using their unique key rather than a numeric position. A list, by contrast, is an ordered collection where elements are accessed purely by their integer index, with no inherent key-based mapping. Dictionaries require unique, hashable keys, while lists simply store a sequence of values that can include duplicates. Dictionaries are best suited for labeled or structured data needing fast lookups, such as records, whereas lists suit simple ordered sequences.

```
# Dictionary: key-based access
person = {'name': 'Alice', 'age': 25}
person['name'] # 'Alice'
# List: index-based access
person_list = ['Alice', 25]
person_list[0] # 'Alice'
```