# Programming Fundamentals - Midterm Exam Answer Key

---

## Part 1: Multiple Choice (20 points)

1. **B** - O(log n)
2. **B** - Stack
3. **B** - 2 (integer division)
4. **C** - 2ndPlace (cannot start with a number)
5. **B** - To initialize an object's state
6. **C** - Merge Sort - O(n log n)
7. **B** - A function that calls itself
8. **B** - NULL or None
9. **B** - 1 (modulo operator gives remainder)
10. **B** - A step-by-step procedure to solve a problem

---

## Part 2: Short Answer (20 points)

### Question 11
**Answer:**
- **Stack:** LIFO (Last-In-First-Out) structure. The last element added is the first to be removed.
  - Real-world example: A stack of plates - you add and remove plates from the top.
- **Queue:** FIFO (First-In-First-Out) structure. The first element added is the first to be removed.
  - Real-world example: A line at a store - first person in line is served first.

### Question 12
**Answer:**
- **Pass by value:** A copy of the variable's value is passed to the function. Changes inside the function don't affect the original variable.
  - Use when: You want to protect the original data from modification.
- **Pass by reference:** The memory address of the variable is passed. Changes inside the function affect the original variable.
  - Use when: You want to modify the original data or avoid copying large data structures.

### Question 13
**Answer:**
Big O notation describes the upper bound of an algorithm's time or space complexity as input size grows. It's important because:
- It helps compare algorithm efficiency independent of hardware
- It shows how performance scales with input size
- It guides us in choosing the best algorithm for a problem

### Question 14
**Answer:**
- **Syntax Error:** Violates the grammar rules of the programming language. The code won't run.
  - Example: `print("Hello"` (missing closing parenthesis)
- **Logical Error:** Code runs but produces incorrect results due to flawed logic.
  - Example: Using `+` instead of `*` in a calculation, causing wrong output

### Question 15
**Answer:**
A hash table is a data structure that maps keys to values using a hash function.
- **Advantage:** Fast O(1) average-case lookup, insertion, and deletion
- **Disadvantage:** Potential for hash collisions, may use more memory than needed, no ordering of elements

---

## Part 3: Code Reading and Analysis (20 points)

### Question 16
**Output:** `120`

**Explanation:**
This is a recursive factorial function. It calculates 5! = 5 × 4 × 3 × 2 × 1 = 120
- mystery(5) = 5 × mystery(4)
- mystery(4) = 4 × mystery(3)
- mystery(3) = 3 × mystery(2)
- mystery(2) = 2 × mystery(1)
- mystery(1) = 1 (base case)
- Result: 5 × 4 × 3 × 2 × 1 = 120

### Question 17
**Bug(s) Identified:**
- `max_val` is initialized to 0, which won't work if all numbers are negative
- The function will return 0 for an array of all negative numbers

**Fixed Code:**
```python
def find_max(arr):
    if not arr:  # Handle empty array
        return None
    max_val = arr[0]  # Initialize with first element
    for num in arr:
        if num > max_val:
            max_val = num
    return max_val

numbers = [3, -5, 7, -2, 9, -1]
print(find_max(numbers))  # Output: 9
```

---

## Part 4: Coding Problems (40 points)

### Question 18 Solution (15 points)
```python
def is_palindrome(s):
    # Remove spaces and convert to lowercase
    cleaned = s.replace(" ", "").lower()
    # Compare with reversed string
    return cleaned == cleaned[::-1]

# Alternative solution using two pointers:
def is_palindrome_v2(s):
    cleaned = s.replace(" ", "").lower()
    left, right = 0, len(cleaned) - 1
    while left < right:
        if cleaned[left] != cleaned[right]:
            return False
        left += 1
        right -= 1
    return True
```

**Grading:**
- Correct removal of spaces: 3 points
- Case-insensitive comparison: 3 points
- Correct palindrome logic: 7 points
- Working code: 2 points

---

### Question 19 Solution (12 points)
```python
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# More efficient iterative solution:
def fibonacci_iterative(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    
    prev, curr = 0, 1
    for i in range(2, n + 1):
        prev, curr = curr, prev + curr
    return curr
```

**Grading:**
- Correct base cases: 4 points
- Correct recursive/iterative logic: 6 points
- Working code: 2 points

---

### Question 20 Solution (13 points)
```python
def count_vowels(s):
    vowels = {'a': 0, 'e': 0, 'i': 0, 'o': 0, 'u': 0}
    s_lower = s.lower()
    
    for char in s_lower:
        if char in vowels:
            vowels[char] += 1
    
    return vowels

# Alternative using dictionary comprehension:
def count_vowels_v2(s):
    s_lower = s.lower()
    vowels = 'aeiou'
    return {v: s_lower.count(v) for v in vowels}
```

**Grading:**
- Correct dictionary initialization: 3 points
- Case-insensitive handling: 3 points
- Correct counting logic: 5 points
- Working code: 2 points

---

## Bonus Question Solution (+5 points)

```python
def remove_duplicates(arr):
    if not arr:
        return 0
    
    # Use two pointers
    write_index = 1
    
    for read_index in range(1, len(arr)):
        if arr[read_index] != arr[read_index - 1]:
            arr[write_index] = arr[read_index]
            write_index += 1
    
    return write_index

# Alternative solution:
def remove_duplicates_v2(arr):
    if not arr:
        return 0
    
    unique_count = 1
    for i in range(1, len(arr)):
        if arr[i] != arr[unique_count - 1]:
            arr[unique_count] = arr[i]
            unique_count += 1
    
    return unique_count
```

**Grading:**
- In-place modification: 2 points
- Correct duplicate detection: 2 points
- Correct length return: 1 point

---

## Grading Scale

- **90-105:** A (excellent understanding)
- **80-89:** B (good understanding)
- **70-79:** C (satisfactory understanding)
- **60-69:** D (minimal understanding)
- **Below 60:** F (needs improvement)

---

**Note:** Partial credit should be awarded for approaches that show understanding even if the implementation has minor errors.
