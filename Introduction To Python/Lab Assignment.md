# Lab Assignment

- Lab(14/07)
    - Q1. Sum of 2 numbers
        
        ```python
        a = int(input("Enter first number: "))
        b = int(input("Enter second number: "))
        print("Sum =", a + b)
        
        ```
        
    - Q2. Sub of 2 numbers
        
        ```python
        a = float(input("Enter first number: "))
        b = float(input("Enter second number: "))
        print("Sub =", a - b)
        
        ```
        
    - Q3. Product (int and float value)
        
        ```python
        a = int(input("Enter an integer: "))
        b = float(input("Enter a float: "))
        print("Product =", a * b)
        
        ```
        
    - Q4. Division of 2 numbers
        
        ```python
        a = int(input("enter first number: "))
        b = int(input("enter second number: "))
        print("quotient =",a / b)
        
        ```
        
    - Q5. Area of  a circle
        
        ```python
        r =float(input("enter radius: "))
        area=3.14 * r * r
        print("area of circle =",area)
        
        ```
        
    - Q6. Area of a triangle
        
        ```python
        base=float(input("enter base: "))
        height=float(input("enter height: "))
        area= 0.5*base*height
        print("area of triangle =",area)
        ```
        
    - Q7. Simple Interest
        
        ```python
        p=float(input("enter principle amount: "))
        r=float(input("enter rate of interest in %: "))
        t=float(input("enter time period in years : "))
        SI= (p*r*t)/100
        print("Simple Interest=",SI)
        ```
        
    - Q8. Max of 2 numbers
        
        ```python
        a=int(input("enter number 1: "))
        b=int(input("enter number 2: "))
        if a>b:
            print("number 1 greater")
        else: 
            print("number 2 greater")
        ```
        
    - Q9. Even or Odd
        
        ```python
        **a=int(input("enter number: "))
        if a%2==0:
            print("Even")
        else:
            print("odd")**
        ```
        
    - Q10. Min of 3 numbers
        
        ```python
        a=int(input("enter number 1: "))
        b=int(input("enter number 2: "))
        c=int(input("enter number 3: "))
        if a<b and a<c:
            print("num 1 is min")
        elif b<a and b<c:
            print("num 2 is min")
        else: 
            print("num 3 is min")
        ```
        
    - Q11. Voting age
        
        ```python
        age=int(input("enter age: "))
        if age>=18:
            print("eligible to vote")
        else:
            print("not eligible")
        ```
        
    - Q12. Number is positive, negative or zero
        
        ```python
        a=int(input("enter number: "))
        if a>0:
            print("positive")
        elif a<0:
            print("negative")
        else:
            print("zero")
        ```
        
- Lab(21/07)
    - Q1. Day of the Week, Write a Python program to read a number (1–7) from the user and display the corresponding day of the week using if...elif...else. If the entered number is not between 1 and 7, display "Invalid Input".
        
        ```python
        n=int(input("enter day number(1-7): "))
        if n==1:
            print("Monday")
        elif n==2:
            print("Tuesday")
        elif n==3: 
            print("Wednesday")
        elif n==4:
            print("Thursday")
        elif n==5:
            print("Friday")
        elif n==6:
            print("Saturday")
        elif n==7:
            print("Sunday")
        else:
            print("Invalid Input")
            
        ```
        
    - Q2. Simple Calculator, Write a Python program to read two numbers and an operator (+, -, *, /) from the user. Perform the corresponding arithmetic operation using if...elif...else. Display an appropriate message for an invalid operator.
        
        ```python
        a= float(input("enter first number: "))
        b= float(input("enter second number: "))
        o= input("enter operator (+,-,*,/): ")
        
        if o=="+":
            print("result =",a+b)
        elif o=="-":
            print("result =",a-b)
        elif o=="*":
            print("result =",a*b)
        elif o=="/":
            print("result =",a/b)
            if b!=0:
                print("result=", a/b)
            else: 
                print("division by 0 is not possible")
        else:
            print("Invalid operator")
        ```
        
    - **Q3** Write a program to check whether a given number is **prime**.
        
        ```python
        n = int(input("enter number: "))
        is_prime = True
        
        if n<2:
            is_prime = False
        else:
            for i in range(2,n):
                if n%i==0:
                    is_prime = False
                    break
        
        if is_prime:
            print("Prime")
        else:
            print("Not Prime")
        ```
        
    - **Q4**  Write a program to print all **even numbers** between 1 and N.
        
        ```python
        n=int(input("enter N: "))
        for i in range(1,n+1):
            if i%2==0:
                print(i)
        ```
        
    - **Q5. Print Numbers Using for Loop,** Write a program to print numbers from **1 to N** using a **for loop**
        
        ```python
        n = int(input("enter N: "))
        for i in range(1,n+1):
            print(i)
        ```
        
    - **Q6. Print Numbers Using while Loop,** Write a program to print numbers from **N to 1** using a **while loop**.
        
        ```python
        n = int(input("enter N: "))
        while n>=1:
            print(n)
            n= n-1
        ```
        
    - **Q7. Sum of First N Natural Numbers,** Write a program to find the **sum of first N natural numbers** using a loop.
        
        ```python
        n = int(input("Enter the value of N: "))
        sum = 0
        for i in range(1, n + 1):
            sum = sum + i
        print("Sum =", sum)
        ```
        
- Lab(28/07)
    - Q1. Write a program in python to count vowels and consonants from a string
        
        ```python
        def count_vowels_consonants(s):
            vowels = "aeiouAEIOU"
            v_count = 0
            c_count = 0
            for ch in s:
                if ch.isalpha():
                    if ch in vowels:
                        v_count += 1
                    else:
                        c_count += 1
            return v_count, c_count
        
        s = input("Enter a string: ")
        print(count_vowels_consonants(s))
        ```
        
    - Q2. Write a program to count digits and special characters in a string
        
        ```python
        def count_digits_special(s):
            d_count = 0
            sp_count = 0
            for ch in s:
                if ch.isdigit():
                    d_count += 1
                elif not ch.isalnum() and not ch.isspace():
                    sp_count += 1
            return d_count, sp_count
        
        s = input("Enter a string: ")
        print(count_digits_special(s))
        ```
        
    - Q3. Write a program to check whether two strings are anagrams
        
        ```python
        def is_anagram(s1, s2):
            s1 = s1.replace(" ", "").lower()
            s2 = s2.replace(" ", "").lower()
            return sorted(s1) == sorted(s2)
        
        s1 = input("Enter first string: ")
        s2 = input("Enter second string: ")
        print(is_anagram(s1, s2))
        ```
        
    - Q4. Write a program to find occurrence of each character in a string
        
        ```python
        def char_occurrence(s):
            freq = {}
            for ch in s:
                if ch in freq:
                    freq[ch] += 1
                else:
                    freq[ch] = 1
            return freq
        
        s = input("Enter a string: ")
        print(char_occurrence(s))
        ```
        
    - Q5. Write a program to reverse every word of a sentence
        
        ```python
        def reverse_each_word(sentence):
            words = sentence.split()
            reversed_words = []
            for word in words:
                reversed_words.append(word[::-1])
            return " ".join(reversed_words)
        
        sentence = input("Enter a sentence: ")
        print(reverse_each_word(sentence))
        ```
        
    - Q6. Write a program to find the longest word in a sentence
        
        ```python
        def longest_word(sentence):
            words = sentence.split()
            longest = ""
            for word in words:
                if len(word) > len(longest):
                    longest = word
            return longest
        
        sentence = input("Enter a sentence: ")
        print(longest_word(sentence))
        ```
        
    - Q7. Write a program to remove duplicate characters from a string
        
        ```python
        def remove_duplicates(s):
            seen = set()
            result = ""
            for ch in s:
                if ch not in seen:
                    seen.add(ch)
                    result += ch
            return result
        
        s = input("Enter a string: ")
        print(remove_duplicates(s))
        ```
        
    - Q8. Write a program to check whether string is palindrome
        
        ```python
        def is_palindrome(s):
            s = s.lower().replace(" ", "")
            return s == s[::-1]
        
        s = input("Enter a string: ")
        print(is_palindrome(s))
        ```
        
    - Q9. Write a program to count occurrence of each word in a sentence
        
        ```python
        def word_occurrence(sentence):
            words = sentence.split()
            freq = {}
            for word in words:
                if word in freq:
                    freq[word] += 1
                else:
                    freq[word] = 1
            return freq
        
        sentence = input("Enter a sentence: ")
        print(word_occurrence(sentence))
        ```
        
    - Q10. Write a program to count duplicate words in a sentence
        
        ```python
        def count_duplicate_words(sentence):
            words = sentence.split()
            freq = {}
            for word in words:
                if word in freq:
                    freq[word] += 1
                else:
                    freq[word] = 1
            duplicates = {}
            for word, count in freq.items():
                if count > 1:
                    duplicates[word] = count
            return duplicates
        
        sentence = input("Enter a sentence: ")
        print(count_duplicate_words(sentence))
        ```
        
    - Q11. Write a program to replace multiple spaces with a single space
        
        ```python
        def remove_multiple_spaces(sentence):
            words = sentence.split()
            return " ".join(words)
        
        sentence = input("Enter a sentence with extra spaces: ")
        print(remove_multiple_spaces(sentence))
        ```
        
    - Q12. Write a program to convert sentence into title case without title method
        
        ```python
        def to_title_case(sentence):
            words = sentence.split()
            result = []
            for word in words:
                new_word = word[0].upper() + word[1:].lower()
                result.append(new_word)
            return " ".join(result)
        
        sentence = input("Enter a sentence: ")
        print(to_title_case(sentence))
        ```
        
- Lab(04/08)
    - Q1. Write a Python program to create a list of numbers and find the sum of all elements using a for loop.
        
        ```python
        numbers = [10, 20, 30, 40, 50]
        total = 0
        
        for num in numbers:
            total += num
        
        print("List:", numbers)
        print("Sum of all elements:", total)
        ```
        
    - Q2. Write a Python program to count the number of even and odd elements in a given list.
        
        ```python
        numbers = [12, 7, 18, 5, 24, 9, 2]
        even_count = 0
        odd_count = 0
        
        for num in numbers:
            if num % 2 == 0:
                even_count += 1
            else:
                odd_count += 1
        
        print("List:", numbers)
        print("Even numbers count:", even_count)
        print("Odd numbers count:", odd_count)
        ```
        
    - Q3. Write a Python program to search an element in a list and terminate the loop using break when the element is found.
        
        ```python
        n = int(input("Enter number of elements: "))
        numbers = []
        
        for i in range(n):
            num = int(input(f"Enter element {i+1}: "))
            numbers.append(num)
        
        target = int(input("Enter number to search: "))
        
        for num in numbers:
            if num == target:
                print(f"{target} found in the list!")
                break
        else:
            print(f"{target} not found in the list.")
        ```
        
    - Q4. Write a Python program to print only odd elements from a list using continue.
        
        ```python
        n = int(input("Enter number of elements: "))
        numbers = []
        
        for i in range(n):
            num = int(input(f"Enter element {i+1}: "))
            numbers.append(num)
        
        print("Odd numbers:")
        for num in numbers:
            if num % 2 == 0:
                continue
            print(num)
        ```
        
    - Q5. Write a Python program to demonstrate the use of append(), insert(), and remove() methods on a list.
        
        ```python
        fruits = []
        
        n = int(input("How many fruits? "))
        for i in range(n):
            fruits.append(input("Enter fruit: "))
        
        print("Original list:", fruits)
        
        fruits.append(input("Enter fruit to append: "))
        print("After append:", fruits)
        
        fruits.insert(1, input("Enter fruit to insert at position 1: "))
        print("After insert:", fruits)
        
        fruits.remove(input("Enter fruit to remove: "))
        print("After remove:", fruits)
        ```
        
    - Q6. Write a Python program to find the largest and smallest elements in a list using if conditions.
        
        ```python
        numbers = []
        
        n = int(input("How many numbers? "))
        for i in range(n):
            num = int(input("Enter number: "))
            numbers.append(num)
        
        largest = numbers[0]
        smallest = numbers[0]
        
        for num in numbers:
            if num > largest:
                largest = num
            if num < smallest:
                smallest = num
        
        print("Largest:", largest)
        print("Smallest:", smallest)
        ```
        
    - Q7. Write a Python program to display all elements of a tuple using a for loop.
        
        ```python
        fruits = ("apple", "banana", "mango", "grape")
        
        print("Tuple elements:")
        for item in fruits:
            print(item)
        ```
        
- Lab(11/08)
    - Q1. Write a Python program to find the count and index of a given element in a tuple using count() and index() methods.
        
        ```python
        t = (10, 20, 30, 20, 40, 20)
        element = 20
        print("Count of", element, ":", t.count(element))
        print("Index of", element, ":", t.index(element))
        ```
        
    - Q2. Write a Python program to convert a list into a tuple and a tuple into a list.
        
        ```python
        lst = [1, 2, 3, 4]
        tup = tuple(lst)
        print("List to Tuple:", tup)
        
        tup2 = (5, 6, 7, 8)
        lst2 = list(tup2)
        print("Tuple to List:", lst2)
        ```
        
    - Q3. Write a Python program to copy elements from a list into a tuple using a loop.
        
        ```python
        lst = [1, 2, 3, 4, 5]
        temp = []
        for item in lst:
            temp.append(item)
        tup = tuple(temp)
        print("Tuple after copying:", tup)
        ```
        
    - Q4. Write a Python program to reverse a list using a while loop (without using built-in reverse functions).
        
        ```python
        lst = [1, 2, 3, 4, 5]
        i = 0
        j = len(lst) - 1
        while i < j:
            lst[i], lst[j] = lst[j], lst[i]
            i += 1
            j -= 1
        print("Reversed list:", lst)
        ```
        
    - Q5. Write a Python program to demonstrate tuple packing and unpacking with appropriate examples.
        
        ```python
        person = ("Avadhut", 18, "Pune")
        name, age, city = person
        print("Packed tuple:", person)
        print("Unpacked -> Name:", name, "Age:", age, "City:", city)
        ```
        
    - Q6. Write a Python program to create a new list containing only even numbers from an existing list using list comprehension.
        
        ```python
        numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        even_nums = [n for n in numbers if n % 2 == 0]
        print("Even numbers:", even_nums)
        ```
        
    - Q7. Write a Python program to generate a list of squares of numbers from 1 to 10 using list comprehension.
        
        ```python
        squares = [n**2 for n in range(1, 11)]
        print("Squares:", squares)
        ```
        
- Lab(18/08)
    - Q1. Create a dictionary with five student names and their marks. Display all the student names using the keys() function.
        
        ```python
        students = {"Amit": 85, "Priya": 90, "Rahul": 78, "Sneha": 88, "Karan": 92}
        print("Student Names:")
        for name in students.keys():
            print(name)
        ```
        
        Output:
        
        ```
        Student Names:
        Amit
        Priya
        Rahul
        Sneha
        Karan
        ```
        
    - Q2. Create a dictionary of five fruits and their prices. Display all the prices using the values() function.
        
        ```python
        fruits = {"Apple": 120, "Banana": 40, "Mango": 100, "Grapes": 80, "Orange": 60}
        print("Fruit Prices:")
        for price in fruits.values():
            print(price)
        ```
        
        Output:
        
        ```
        Fruit Prices:
        120
        40
        100
        80
        60
        ```
        
    - Q3. Create a dictionary of five countries and their capitals. Display each country and its capital using the items() function and a for loop.
        
        ```python
        countries = {"India": "New Delhi", "USA": "Washington DC", "Japan": "Tokyo", "France": "Paris", "Germany": "Berlin"}
        for country, capital in countries.items():
            print(country, "->", capital)
        ```
        
        Output:
        
        ```
        India -> New Delhi
        USA -> Washington DC
        Japan -> Tokyo
        France -> Paris
        Germany -> Berlin
        ```
        
    - Q4. Create a dictionary of four subjects and their marks. Find the total of all marks using a for loop.
        
        ```python
        marks = {"Maths": 85, "Physics": 78, "Python": 92, "DBMS": 88}
        total = 0
        for subject in marks:
            total += marks[subject]
        print("Total Marks =", total)
        ```
        
        Output:
        
        ```
        Total Marks = 343
        ```
        
    - Q5. Create a dictionary of employee names and their salaries. Add a new employee using the update() function and display the updated dictionary.
        
        ```python
        employees = {"Ravi": 45000, "Sneha": 50000, "Amit": 42000}
        employees.update({"Pooja": 48000})
        print("Updated Dictionary:", employees)
        ```
        
        Output:
        
        ```
        Updated Dictionary: {'Ravi': 45000, 'Sneha': 50000, 'Amit': 42000, 'Pooja': 48000}
        ```
        
    - Q6. Create a dictionary of five products and their prices. Ask the user to enter a product name and display its price using the get() function. If the product is not found, display "Product not found".
        
        ```python
        products = {"Pen": 10, "Notebook": 40, "Bag": 500, "Bottle": 150, "Pencil": 5}
        name = input("Enter product name: ")
        print(products.get(name, "Product not found"))
        ```
        
        Output (sample runs):
        
        ```
        Enter product name: Bag
        500
        
        Enter product name: Eraser
        Product not found
        ```
        
    - Q7. Create a dictionary of five items and their quantities. Remove one item using the pop() function and display the remaining dictionary.
        
        ```python
        items = {"Rice": 10, "Wheat": 15, "Sugar": 5, "Salt": 2, "Oil": 8}
        items.pop("Salt")
        print("Remaining Dictionary:", items)
        ```
        
        Output:
        
        ```
        Remaining Dictionary: {'Rice': 10, 'Wheat': 15, 'Sugar': 5, 'Oil': 8}
        ```
        
    - Q8. Create a dictionary containing five numbers as values. Using a for loop and an if statement, count how many values are even and how many are odd.
        
        ```python
        numbers = {"a": 12, "b": 7, "c": 18, "d": 5, "e": 24}
        even_count = 0
        odd_count = 0
        for value in numbers.values():
            if value % 2 == 0:
                even_count += 1
            else:
                odd_count += 1
        print("Even count:", even_count)
        print("Odd count:", odd_count)
        ```
        
        Output:
        
        ```
        Even count: 3
        Odd count: 2
        ```
        
- Lab (25/08)
    - Q1. Remove Duplicates, Write a Python program to remove duplicate elements from a list using a set.
        
        ```python
        numbers = [1, 2, 2, 3, 4, 4, 5]
        unique_numbers = list(set(numbers))
        print("Original:", numbers)
        print("After removing duplicates:", unique_numbers)
        ```
        
        Output:
        
        ```jsx
        Original: [1, 2, 2, 3, 4, 4, 5]
        After removing duplicates: [1, 2, 3, 4, 5]
        ```
        
    - Q2. Union and Intersection, Write a program to find the union and intersection of two given sets.
        
        ```python
        A = {1, 2, 3, 4, 5}
        B = {4, 5, 6, 7, 8}
        print("Set A:", A)
        print("Set B:", B)
        print("Union:", A | B)
        print("Intersection:", A & B)
        ```
        
        Output:
        
        ```jsx
        Set A: {1, 2, 3, 4, 5}
        Set B: {4, 5, 6, 7, 8}
        Union: {1, 2, 3, 4, 5, 6, 7, 8}
        Intersection: {4, 5}
        ```
        
    - Q3. Subset Check, Write a Python program to check whether one set is a subset of another set.
        
        ```python
        A = {1, 2, 3}
        B = {1, 2, 3, 4, 5}
        print("A:", A)
        print("B:", B)
        print("Is A a subset of B?", A.issubset(B))
        ```
        
        Output:
        
        ```jsx
        A: {1, 2, 3}
        B: {1, 2, 3, 4, 5}
        Is A a subset of B? True
        ```
        
    - Q4. Symmetric Difference, Write a program to find the symmetric difference between two sets.
        
        ```python
        A = {1, 2, 3, 4}
        B = {3, 4, 5, 6}
        print("A:", A)
        print("B:", B)
        print("Symmetric Difference:", A ^ B)
        ```
        
        Output:
        
        ```jsx
        A: {1, 2, 3, 4}
        B: {3, 4, 5, 6}
        Symmetric Difference: {1, 2, 5, 6}
        ```
        
    - Q5. Common Elements in Three Sets, Write a Python program to find common elements among bthree sets.
        
        ```python
        A = {1, 2, 3, 4}
        B = {2, 3, 4, 5}
        C = {3, 4, 5, 6}
        common = A & B & C
        print("A:", A)
        print("B:", B)
        print("C:", C)
        print("Common elements:", common)
        ```
        
        Output:
        
        ```jsx
        A: {1, 2, 3, 4}
        B: {2, 3, 4, 5}
        C: {3, 4, 5, 6}
        Common elements: {3, 4}
        ```
        
    - Q6. Function Without Arguments (Print Inside Function), Write a function that prints "Welcome to Python Programming" when called.
        
        ```python
        def welcome():
            print("Welcome to Python Programming")
        
        welcome()
        ```
        
        Output:
        
        ```jsx
        Welcome to Python Programming
        ```
        
    - Q7. Function With Arguments (Print Inside Function), Write a function that takes a name as an argument and prints a greeting message.
        
        ```python
        def greet(name):
            print("Hello,", name, "! Welcome!")
        
        greet("Avadhut")
        ```
        
        Output:
        
        ```jsx
        Hello, Avadhut ! Welcome!
        ```
        
    - Q8. Function With Arguments (Return Result)
        
        ```python
        def add(a, b):
            return a + b
        
        result = add(5, 10)
        print("Sum =", result)
        ```
        
        Output:
        
        ```jsx
        Sum = 15
        ```
        
    - Q9. Write a function that takes two numbers as arguments and returns their sum. Print the result using a function call.
        
        ```python
        def add_numbers(a, b):
            return a + b
        
        print("Sum =", add_numbers(7, 12))
        ```
        
        Output:
        
        ```jsx
        Sum = 19
        ```
        
    - Q10. Function Without Arguments (Return Result), Write a function that returns the current year. Print the returned value.
        
        ```python
        from datetime import datetime
        
        def get_current_year():
            return datetime.now().year
        
        year = get_current_year()
        print("Current Year:", year)
        ```
        
        Output:
        
        ```jsx
        Current Year: 2026
        ```
        
    - Q11. Function With Arguments (Even/Odd Check), Write a function that takes a number as argument and prints whether it is even or odd.
        
        ```python
        def check_even_odd(n):
            if n % 2 == 0:
                print(n, "is Even")
            else:
                print(n, "is Odd")
        
        check_even_odd(7)
        ```
        
        Output:
        
        ```jsx
        7 is Odd
        ```
        
    - Q12. Function With Arguments (Return Boolean), Write a function that takes a number and returns True if it is prime, otherwise False. Print the result.
        
        ```python
        def is_prime(n):
            if n < 2:
                return False
            for i in range(2, n):
                if n % i == 0:
                    return False
            return True
        
        print("Is 13 prime?", is_prime(13))
        ```
        
        Output:
        
        ```jsx
        Is 13 prime? True
        ```
        
    - Q13. Function With Default Argument, Write a function to calculate simple interest where rate has a default value of 5%. Return the result and print it.
        
        ```python
        def simple_interest(p, t, r=5):
            return (p * r * t) / 100
        
        result = simple_interest(1000, 2)
        print("Simple Interest =", result)
        ```
        
        Output:
        
        ```jsx
        Simple Interest = 100.0
        ```
        
    - Q14. Function With Multiple Arguments, Write a function that takes three numbers and returns the largest number.
        
        ```python
        def largest(a, b, c):
            if a >= b and a >= c:
                return a
            elif b >= a and b >= c:
                return b
            else:
                return c
        
        print("Largest =", largest(10, 25, 15))
        ```
        
        Output:
        
        ```jsx
        Largest = 25
        ```
        
    - Q15. Function Calling Another Function, Write a function square(n) that returns the square of a number. Write another function cube(n) that uses square() and returns the cube.
        
        ```python
        def square(n):
            return n * n
        
        def cube(n):
            return n * square(n)
        
        print("Square of 4 =", square(4))
        print("Cube of 4 =", cube(4))
        ```
        
        Output:
        
        ```jsx
        Square of 4 = 16
        Cube of 4 = 64
        ```
        
    - Q16. Function With User Input Inside Function, Write a function that asks the user to enter a number and prints its factorial inside the function.
        
        ```python
        def print_factorial():
            n = int(input("Enter a number: "))
            fact = 1
            for i in range(1, n + 1):
                fact *= i
            print("Factorial of", n, "=", fact)
        
        print_factorial()
        ```
        
        Output (sample run):
        
        ```jsx
        Enter a number: 5
        Factorial of 5 = 120
        ```