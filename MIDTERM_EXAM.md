# Programming Fundamentals - Midterm Exam

**Name:** _______________________  
**Date:** _______________________  
**Time Allowed:** 90 minutes  
**Total Points:** 100

---

## Instructions
- Read all questions carefully before answering
- Show your work for coding problems
- You may use pseudocode or any programming language for coding questions
- Partial credit may be awarded for partially correct answers

---

## Part 1: Multiple Choice (20 points, 2 points each)

### Question 1
What is the time complexity of binary search on a sorted array?
- A) O(n)
- B) O(log n)
- C) O(n²)
- D) O(1)

### Question 2
Which data structure follows the Last-In-First-Out (LIFO) principle?
- A) Queue
- B) Stack
- C) Array
- D) Linked List

### Question 3
What will be the output of the following code?
```python
x = 5
y = 2
print(x // y)
```
- A) 2.5
- B) 2
- C) 3
- D) Error

### Question 4
Which of the following is NOT a valid variable name in most programming languages?
- A) myVariable
- B) _count
- C) 2ndPlace
- D) totalSum

### Question 5
What is the purpose of a constructor in object-oriented programming?
- A) To destroy an object
- B) To initialize an object's state
- C) To compare two objects
- D) To copy an object

### Question 6
Which sorting algorithm has the best average-case time complexity?
- A) Bubble Sort - O(n²)
- B) Insertion Sort - O(n²)
- C) Merge Sort - O(n log n)
- D) Selection Sort - O(n²)

### Question 7
What is recursion?
- A) A loop that runs indefinitely
- B) A function that calls itself
- C) A way to sort arrays
- D) A type of variable

### Question 8
In a linked list, what does the last node's next pointer contain?
- A) The first node's address
- B) NULL or None
- C) -1
- D) The previous node's address

### Question 9
What is the result of: 10 % 3?
- A) 3
- B) 1
- C) 3.33
- D) 0

### Question 10
Which of the following best describes an algorithm?
- A) A programming language
- B) A step-by-step procedure to solve a problem
- C) A data structure
- D) A debugging tool

---

## Part 2: Short Answer (20 points, 4 points each)

### Question 11
Explain the difference between a stack and a queue. Provide one real-world example for each.

**Answer:**

---

### Question 12
What is the difference between `pass by value` and `pass by reference`? Give an example of when you would use each.

**Answer:**

---

### Question 13
Describe what Big O notation is and why it is important in computer science.

**Answer:**

---

### Question 14
What is the difference between a syntax error and a logical error? Give an example of each.

**Answer:**

---

### Question 15
Explain what a hash table is and describe one advantage and one disadvantage of using hash tables.

**Answer:**

---

## Part 3: Code Reading and Analysis (20 points, 10 points each)

### Question 16
What is the output of the following code? Explain your reasoning.

```python
def mystery(n):
    if n <= 1:
        return 1
    else:
        return n * mystery(n - 1)

result = mystery(5)
print(result)
```

**Output:**

**Explanation:**

---

### Question 17
Identify and fix the bug(s) in the following code that is supposed to find the maximum value in an array:

```python
def find_max(arr):
    max_val = 0
    for num in arr:
        if num > max_val:
            max_val = num
    return max_val

numbers = [3, -5, 7, -2, 9, -1]
print(find_max(numbers))
```

**Bug(s) Identified:**

**Fixed Code:**

---

## Part 4: Coding Problems (40 points)

### Question 18 (15 points)
Write a function called `is_palindrome` that takes a string as input and returns `True` if the string is a palindrome (reads the same forwards and backwards) and `False` otherwise. Your function should ignore spaces and be case-insensitive. You may assume the input only contains letters and spaces (no punctuation).

**Example:**
- `is_palindrome("racecar")` → `True`
- `is_palindrome("hello")` → `False`
- `is_palindrome("A man a plan a canal Panama")` → `True`

**Your Solution:**

```python
def is_palindrome(s):
    # Your code here
    pass
```

---

### Question 19 (12 points)
Write a function called `fibonacci` that takes an integer `n` as input and returns the nth Fibonacci number. The Fibonacci sequence starts with 0, 1, and each subsequent number is the sum of the previous two.

**Example:**
- `fibonacci(0)` → `0`
- `fibonacci(1)` → `1`
- `fibonacci(6)` → `8` (sequence: 0, 1, 1, 2, 3, 5, 8)

**Your Solution:**

```python
def fibonacci(n):
    # Your code here
    pass
```

---

### Question 20 (13 points)
Write a function called `count_vowels` that takes a string as input and returns a dictionary with the count of each vowel (a, e, i, o, u) in the string. The function should be case-insensitive.

**Example:**
- `count_vowels("Hello World")` → `{'a': 0, 'e': 1, 'i': 0, 'o': 2, 'u': 0}`
- `count_vowels("Programming")` → `{'a': 1, 'e': 0, 'i': 1, 'o': 1, 'u': 0}`

**Your Solution:**

```python
def count_vowels(s):
    # Your code here
    pass
```

---

## Bonus Question (+5 points)

Write a function called `remove_duplicates` that takes a sorted array and removes duplicates in-place, returning the new length of the array. The array should be modified such that the first `k` elements contain the unique elements in the order they appeared.

**Example:**
- `remove_duplicates([1, 1, 2, 2, 3, 4, 4])` → `4` (array becomes `[1, 2, 3, 4, ...]`)

**Your Solution:**

```python
def remove_duplicates(arr):
    # Your code here
    pass
```

---

**End of Exam**

*Good luck!*
