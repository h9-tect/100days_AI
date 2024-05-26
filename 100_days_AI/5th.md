# Day 5: Python Basics - Part 3

## Goal
Practice with Python modules and libraries to strengthen your programming skills and complete more exercises on HackerRank Python.

## Step-by-Step Guide

### 1. Review Basic Concepts
- **Functions**: Understand how to define and call functions in Python. Functions help organize your code into reusable blocks.
- **Loops**: Familiarize yourself with `for` and `while` loops. Loops are used to execute a block of code multiple times.
- **Data Structures**: Learn about lists, dictionaries, sets, and tuples. These structures help you store and organize data efficiently.

### 2. Learn About Python Modules and Libraries
- **Modules**: Reusable pieces of code (functions, classes, variables) that can be imported into your program to provide additional functionality.
- **Libraries**: Collections of modules that offer a wide range of capabilities for different tasks.

### 3. Explore Key Python Libraries
- **os**: This module provides a way to interact with the operating system, allowing you to handle files, directories, and execute system commands.
- **sys**: The sys module provides access to some variables used or maintained by the Python interpreter and to functions that interact strongly with the interpreter.
- **math**: This module provides mathematical functions like square roots, factorials, and trigonometric operations.
- **random**: The random module is used to generate random numbers, which can be useful for simulations, games, and testing.
- **datetime**: This module supplies classes for manipulating dates and times, allowing you to handle time-related tasks.
- **re**: The re module provides support for working with regular expressions, which are useful for string matching and manipulation.
- **json**: This module is used to parse JSON (JavaScript Object Notation), a popular data format for exchanging data between a server and a web application.
- **csv**: The csv module is used to read from and write to CSV (Comma Separated Values) files, which are a common format for tabular data.
- **statistics**: This module provides functions for calculating mathematical statistics of numeric data.
- **collections**: The collections module provides specialized container datatypes, such as namedtuples, deque, Counter, and OrderedDict.
- **itertools**: This module provides functions that create iterators for efficient looping, such as generating permutations and combinations.
- **functools**: The functools module is for higher-order functions that act on or return other functions, such as decorators and partial functions.
- **operator**: This module exports a set of efficient functions corresponding to the intrinsic operators of Python, such as addition, subtraction, and item getters for sorting.

### 4. Practice Exercises

#### 4.1 Using the `os` Module
- **Task**: Write a Python script that lists all files and directories in the current directory.

```python
import os

def list_files_and_directories():
    path = '.'
    files = os.listdir(path)
    for file in files:
        print(file)

list_files_and_directories()
### 5. HackerRank Exercises
Complete the following exercises on [HackerRank Python](https://www.hackerrank.com/domains/python):
```
#### 4.2 Using the `sys` Module
- **Task**: Write a Python script that prints the Python version you are using.
```python
import sys

def print_python_version():
    print(f"Python version: {sys.version}")

print_python_version()
```
#### 4.3 Using the `math` Module
- **Task**: Write a Python script that calculates the factorial of a number.
```python
  import math

def calculate_factorial(number):
    return math.factorial(number)

num = 5
print(f"The factorial of {num} is {calculate_factorial(num)}")
```
#### 4.4 Using the `random` Module
- **Task**: Write a Python script that generates a list of 5 random numbers between 1 and 100.
```python
import random

def generate_random_numbers():
    random_numbers = [random.randint(1, 100) for _ in range(5)]
    return random_numbers

print(generate_random_numbers())
```
#### 4.5 Using the `datetime` Module
- **Task**: Write a Python script that prints the current date and time
```python
from datetime import datetime

def print_current_datetime():
    now = datetime.now()
    print(f"Current date and time: {now}")

print_current_datetime()
```
#### 4.6 Using the `re` Module
- **Task**: Write a Python script that finds all email addresses in a given text.
```python
import re

def find_emails(text):
    email_pattern = r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}'
    emails = re.findall(email_pattern, text)
    return emails

text = "Please contact us at support@example.com or sales@example.com."
print(find_emails(text))
```
#### 4.7 Using the `json` Module
- **Task**: Write a Python script that parses JSON data and prints specific information.
```python
import json

def parse_json(data):
    parsed_data = json.loads(data)
    for key, value in parsed_data.items():
        print(f"{key}: {value}")

json_data = '{"name": "John", "age": 30, "city": "New York"}'
parse_json(json_data)
```
#### 4.8 Using the `csv` Module
- **Task**: Write a Python script that reads data from a CSV file and prints each row.
```python
import csv

def read_csv_file(file_path):
    with open(file_path, mode='r') as file:
        csv_reader = csv.reader(file)
        for row in csv_reader:
            print(row)

file_path = 'data.csv'
read_csv_file(file_path)
```
#### 4.9 Using the `statistics` Module
- **Task**: Write a Python script that calculates the mean and median of a list of numbers.
```python
import statistics

def calculate_statistics(numbers):
    mean = statistics.mean(numbers)
    median = statistics.median(numbers)
    return mean, median

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
mean, median = calculate_statistics(numbers)
print(f"Mean: {mean}, Median: {median}")
```
#### 4.10 Using the `collections` Module
- **Task**: Write a Python script that counts the frequency of elements in a list using collections.Counter.
```python
from collections import Counter

def count_elements(lst):
    counter = Counter(lst)
    return counter

lst = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple']
print(count_elements(lst))
```
##### 4.11 Using the `itertools` Module
- **Task**: Write a Python script that generates all possible permutations of a list of numbers.
```python
import itertools

def generate_permutations(lst):
    permutations = list(itertools.permutations(lst))
    return permutations

lst = [1, 2, 3]
print(generate_permutations(lst))
```
#### 4.12 Using the `functools` Module
- **Task**: Write a Python script that uses functools.reduce to compute the product of a list of numbers.
```python
from functools import reduce

def multiply_elements(lst):
    product = reduce(lambda x, y: x * y, lst)
    return product

lst = [1, 2, 3, 4]
print(multiply_elements(lst))
```
#### 4.13 Using the `operator` Module
- **Task**: Write a Python script that sorts a list of tuples based on the second element using operator.itemgetter.
```python
from operator import itemgetter

def sort_tuples(lst):
    sorted_lst = sorted(lst, key=itemgetter(1))
    return sorted_lst

lst = [(1, 'banana'), (2, 'apple'), (3, 'orange')]
print(sort_tuples(lst))
```
## Summary
- **Review**: Basic Python concepts.
- **Learn**: Key Python libraries and how to use them.
- **Practice**: Solve exercises using Python modules and libraries.
- **HackerRank**: Complete additional exercises to reinforce your learning.

Feel free to ask if you need help with any specific exercise or concept!
