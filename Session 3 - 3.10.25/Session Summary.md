# Session Summary: More Python & Key Concepts

- Lists and Iterables
  - Lists are ordered collections of items that can hold different data types. They are mutable, meaning you can change their contents.
  - Iterables are objects that can be looped over, like lists, strings, or ranges. We use loops like `for` to go through them one by one.
  - Common operations include adding/removing items, sorting, and accessing elements by index.

- Types
  - Python has various data types: integers, floats, strings, booleans, lists, etc. Each type behaves differently.
  - Type conversion lets you change one type to another (e.g., `int("5")` turns a string into a number).
  - Use `type()` to check what type a variable is.

- Strings & f-strings
  - Strings are sequences of characters. You can concatenate them, slice them, and use methods like `upper()` or `split()` (__We didn't really cover this__).
  - f-strings (formatted strings) allow addin variables directly into strings for easy formatting, like `f"Hello, {name}!"`.

- Functions
  - Functions are reusable blocks of code that perform specific tasks. You define them with `def`, and call/use them by their name.
  - They can take arguments (inputs) and return values (outputs). This helps **organize code and avoid repetition.**

- Libraries and Importing
  - Libraries are collections of pre-written code that extend Python's capabilities, like `math` for calculations or `random` for generating random numbers.
  - Use `import` to bring them into your script, e.g., `import math`. Then access functions/methods like `math.sqrt()`.

- Tuples, Enumerate, Zip
    - Tuples are immutable (unchangeable once created) lists, useful for fixed data (ex: coordinates). Created with parentheses: `(1, 2, 3)` or `(5, 9)`.
    - `enumerate()` adds an index to each item in an iterable, useful for loops where you need the position **(this method/function is IMPORTANT and will be used a lot)**.
        - Example:  
            ```python
            fruits = ["apple", "banana", "cherry"]
            for index, fruit in enumerate(fruits):
                    print(index, fruit)
            # Output:
            # 0 apple
            # 1 banana
            # 2 cherry
            ```

    - `zip()` combines multiple iterables into pairs, like zipping two lists together.
        - Example:  
            ```python
            names = ["Alice", "Bob", "Charlie"]
            scores = [85, 92, 78]
            for name, score in zip(names, scores):
                    print(f"{name}: {score}")
            # Output:
            # Alice: 85
            # Bob: 92
            # Charlie: 78
            ```

    - Slices & Indices (Indexes)
        - Indices access individual elements, starting from 0 (e.g., `my_list[0]` gets the first item).
            - Example:  
                ```python
                my_list = [10, 20, 30, 40]
                print(my_list[0])  # 10
                print(my_list[1])  # 20
                print(my_list[3])  # 40
                ```
        - Negative indices count from the end: `-1` is the last item, `-2` is the second-to-last, etc.  
            Example:  
            ```python
            my_list = [10, 20, 30, 40]
            print(my_list[-1])  # 40
            print(my_list[-2])  # 30
            ```
        - Slicing extracts parts of lists or strings using `[start:end]` (based on how indices work: zero for 1st item in iterable), like `my_string[2:5]` for characters 3 to 5 (end is not included).  
            Example:  
            ```python
            my_string = "abcdef"
            print(my_string[2:5])  # "cde"
            ```
        - You can omit `start` or `end` to slice from the beginning or to the end:  
            ```python
            print(my_list[:2])   # [10, 20]
            print(my_list[2:])   # [30, 40]
            ```
        - Slicing with negative indices lets you select parts relative to the end:  
            ```python
            print(my_list[-3:-1])  # [20, 30]
            print(my_string[:-2])  # "abcd"
            print(my_string[-3:])  # "def"
            ```
        - Slices can also use a step: `[start:end:step]`  
            Example:  
            ```python
            print(my_list[::2])   # [10, 30]
            print(my_list[::-1])  # [40, 30, 20, 10]  # reverses the list
            ```

# Homework

- Do as many problems as you can in the [CSE_CLUB_PROBLEMS.pdf](CSE_CLUB_PROBLEMS.pdf)
- As a bonus, learn about the Walrus Operator (`:=`) in Python. It's a handy feature introduced in Python 3.8 that allows you to assign values to variables within expressions. Search for tutorials or documentation online, and try to understand its usage with some simple examples. Feel free to ask questions if you have any!