## Day 4: Python Basics - Part 2

### Tasks
1. **Continue Learning Python Basics**
   - **Control Flow Statements**
     - Understand how to use `if`, `else`, and `elif` statements to control the flow of your program.
     - Example:
       ```python
       x = 10
       if x > 0:
           print("x is positive")
       elif x == 0:
           print("x is zero")
       else:
           print("x is negative")
       ```
   - **Loops**
     - Learn the difference between `for` and `while` loops and when to use each.
     - **For Loop Example:**
       ```python
       for i in range(5):
           print(i)
       ```
     - **While Loop Example:**
       ```python
       count = 0
       while count < 5:
           print(count)
           count += 1
       ```
   - **Functions**
     - Learn how to define and call functions.
     - Understand function parameters and return values.
     - Example:
       ```python
       def greet(name):
           return "Hello, " + name

       print(greet("Alice"))
       ```
     - Explore recursion and scope in functions.
     - **Recursive Function Example:**
       ```python
       def factorial(n):
           if n == 0:
               return 1
           else:
               return n * factorial(n - 1)

       print(factorial(5))
       ```

2. **Write Small Programs to Solidify Your Understanding**
   - Implement small programs that make use of loops, functions, and data structures.
   - Examples:
     - **Factorial Program (Iterative and Recursive):**
       ```python
       def factorial_iterative(n):
           result = 1
           for i in range(1, n + 1):
               result *= i
           return result

       def factorial_recursive(n):
           if n == 0 or n == 1:
               return 1
           else:
               return n * factorial_recursive(n - 1)

       number = int(input("Enter a number: "))
       print("Factorial (Iterative):", factorial_iterative(number))
       print("Factorial (Recursive):", factorial_recursive(number))
       ```

     - **Bubble Sort Program:**
       ```python
       def bubble_sort(arr):
           n = len(arr)
           for i in range(n):
               for j in range(0, n-i-1):
                   if arr[j] > arr[j+1]:
                       arr[j], arr[j+1] = arr[j+1], arr[j]
           return arr

       numbers = [64, 34, 25, 12, 22, 11, 90]
       print("Sorted array is:", bubble_sort(numbers))
       ```

     - **Word Count Program:**
       ```python
       def word_count(text):
           words = text.split()
           word_dict = {}
           for word in words:
               if word in word_dict:
                   word_dict[word] += 1
               else:
                   word_dict[word] = 1
           return word_dict

       sample_text = "hello world hello"
       print("Word count:", word_count(sample_text))
       ```

3. **Explore Python Data Structures**
   - Learn about lists, tuples, sets, and dictionaries.
   - **Lists:**
     - Example:
       ```python
       fruits = ["apple", "banana", "cherry"]
       for fruit in fruits:
           print(fruit)
       ```
   - **Tuples:**
     - Example:
       ```python
       coordinates = (10, 20)
       print(coordinates[0])
       ```
   - **Sets:**
     - Example:
       ```python
       unique_numbers = {1, 2, 3, 3, 4}
       print(unique_numbers)
       ```
   - **Dictionaries:**
     - Example:
       ```python
       student_grades = {"Alice": 90, "Bob": 85, "Charlie": 92}
       for student, grade in student_grades.items():
           print(student, grade)
       ```

### Resources
- **Python Loops and Control Flow**
  - [Python Loops Tutorial](https://www.w3schools.com/python/python_for_loops.asp)
  - [Python Control Flow](https://docs.python.org/3/tutorial/controlflow.html)

- **Python Functions**
  - [Functions in Python](https://www.programiz.com/python-programming/function)
  - [Scope and Lifetime of Variables in Python](https://www.geeksforgeeks.org/scope-resolution-in-python-legb-rule/)

- **Data Structures**
  - [Python Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
  - [GeeksforGeeks - Python Data Structures](https://www.geeksforgeeks.org/python-data-structures/)

### Summary
By the end of Day 4, you should have a solid understanding of Python loops, functions, and basic data structures. Practice these concepts through small programs to reinforce your learning. Use the resources provided to deepen your understanding and continue building a strong foundation in Python.
