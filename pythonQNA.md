https://www.datacamp.com/blog/top-python-interview-questions-and-answers
# Basic Python Interview Questions

These are some of the questions you might encounter during an entry-level Python interview.

## 1. What is Python, and list some of its key features

Python is a versatile, high-level programming language known for its easy-to-read syntax and broad applications. Here are some of Python’s key features:

- **Simple and Readable Syntax**: Python’s syntax is clear and straightforward, making it accessible for beginners and efficient for experienced developers.
- **Interpreted Language**: Python executes code line by line, which helps in debugging and testing.
- **Dynamic Typing**: Python does not require explicit data type declarations, allowing more flexibility.
- **Extensive Libraries and Frameworks**: Libraries like NumPy, Pandas, and Django expand Python’s functionality for specialized tasks in data science, web development, and more.
- **Cross-Platform Compatibility**: Python can run on different operating systems, including Windows, macOS, and Linux.

---

## 2. What are Python lists and tuples?

Lists and tuples are fundamental Python data structures with distinct characteristics and use cases.

### List:
- **Mutable**: Elements can be changed after creation.
- **Memory Usage**: Consumes more memory.
- **Performance**: Slower iteration compared to tuples but better for insertion and deletion operations.
- **Methods**: Offers various built-in methods for manipulation.

```python
# Example
my_list = ["Data", "Camp", "Tutorial"]
my_list.append("Session")
print(my_list)  # Output: ['Data', 'Camp', 'Tutorial', 'Session']
```

### Tuple:
- **Immutable**: Elements cannot be changed after creation.
- **Memory Usage**: Consumes less memory.
- **Performance**: Faster iteration compared to lists but lacks the flexibility of lists.
- **Methods**: Limited built-in methods.

```python
# Example
a_tuple = ("Data", "Camp", "Tutorial")
print(a_tuple)  # Output: ('Data', 'Camp', 'Tutorial')
```

---

## 3. What is `__init__()` in Python?

The `__init__()` method is known as a constructor in object-oriented programming (OOP) terminology. It is used to initialize an object's state when it is created. This method is automatically called when a new instance of a class is instantiated.

### Purpose:
- Assign values to object properties.
- Perform any initialization operations.

```python
# Example
class BookShop:
    def __init__(self, title):
        self.title = title

    def display_book(self):
        print('The title of the book is', self.title)

book = BookShop('Sandman')
book.display_book()  # Output: The title of the book is Sandman
```

---

## 4. What is the difference between a mutable data type and an immutable data type?

### Mutable data types:
- **Definition**: Mutable data types are those that can be modified after their creation.
- **Examples**: List, Dictionary, Set.
- **Characteristics**: Elements can be added, removed, or changed.
- **Use Case**: Suitable for collections of items where frequent updates are needed.

```python
# List Example
a_list = [1, 2, 3]
a_list.append(4)
print(a_list)  # Output: [1, 2, 3, 4]

# Dictionary Example
a_dict = {'a': 1, 'b': 2}
a_dict['c'] = 3
print(a_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
```

### Immutable data types:
- **Definition**: Immutable data types are those that cannot be modified after their creation.
- **Examples**: Numeric (int, float), String, Tuple.
- **Characteristics**: Elements cannot be changed once set; any operation that appears to modify an immutable object will create a new object.

```python
# Numeric Example
a_num = 10
a_num = 20  # Creates a new integer object
print(a_num)  # Output: 20

# String Example
a_str = "hello"
a_str = "world"  # Creates a new string object
print(a_str)  # Output: world

# Tuple Example
a_tuple = (1, 2, 3)
# a_tuple[0] = 4  # This will raise a TypeError
print(a_tuple)  # Output: (1, 2, 3)
```

---

## 5. Explain list, dictionary, and tuple comprehension with an example.

### List Comprehension:
List comprehension offers a concise way to create a new list based on the values of an existing list.

```python
# Example
my_list = [i for i in range(1, 10)]
print(my_list)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### Dictionary Comprehension:
You can create a dictionary based on an existing iterable with a single line of code.

```python
# Example
my_dict = {i: i**2 for i in range(1, 10)}
print(my_dict)  # Output: {1: 1, 2: 4, 3: 9, ...}
```

### Tuple Comprehension:
Tuple comprehension uses round brackets `()` but returns a generator object.

```python
# Example
my_tuple = (i for i in range(1, 10))
print(list(my_tuple))  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

---

