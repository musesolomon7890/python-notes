# python notes

# Python Overview

Python stands out as a high-level, interpreted programming language developed by Guido van Rossum, initially introduced in 1991. Renowned for its emphasis on readability through significant indentation, Python supports various programming paradigms, including procedural, object-oriented, and functional programming. Its dynamic typing and garbage collection enhance flexibility and ease of use. Python's extensive standard library earns it the moniker "batteries included."

## Tuples in Python

In Python, a tuple represents an ordered and immutable collection of elements, denoted by round brackets. For instance, `my_tuple = ("apple", "banana", "cherry")`. Once created, tuples cannot be modified. They find utility in scenarios where data immutability is desired, such as representing days of the week or calendar dates.

```python
mytuple = ("apple", "banana", "cherry")

```

Tuples offer versatility beyond immutability. They are commonly employed to store multiple values in a single variable. This feature proves handy when functions need to return multiple values simultaneously.

```python
def get_info():
    return ("John", "Doe", 25)

name, surname, age = get_info()

```

Python's tuples support various built-in functions like `count()` and `index()`. The former returns the frequency of a specified value, while the latter retrieves the position of a value within the tuple.

```python
mytuple = ("apple", "banana", "cherry", "apple")
print(mytuple.count("apple"))  # Outputs: 2
print(mytuple.index("banana"))  # Outputs: 1

```

Tuples facilitate sequence unpacking, where Python assigns tuple values to individual variables.

```python
fruits = ("apple", "banana", "cherry")
(a, b, c) = fruits
print(a)  # Outputs: apple

```

## Lists in Python

Contrary to tuples, lists in Python are mutable collections of ordered elements enclosed in square brackets. Lists allow dynamic addition, removal, and modification of elements after creation.

```python
mylist = ["apple", "banana", "cherry"]
mylist[1] = "blackcurrant"  # Updates the second item

```

Python offers a range of built-in functions and methods to manipulate lists effectively. For instance, the `append()` method adds an item to the end of a list.

```python
mylist = ["apple", "banana", "cherry"]
mylist.append("dragonfruit")  # Appends 'dragonfruit' to the end

```

Similarly, the `remove()` method eliminates the first occurrence of a specified element from the list.

```python
mylist = ["apple", "banana", "cherry"]
mylist.remove("banana")  # Removes 'banana' from the list

```

List comprehension provides a concise way to create lists based on existing ones, fostering readability and efficiency.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]

```

## Sets in Python

Sets in Python represent unique and unordered collections of elements, delineated by curly brackets. While set items are immutable, new items can be added to existing sets.

To add a single item, employ the `add()` method.

```python
myset = {"apple", "banana", "cherry"}
myset.add("orange")  # Adds 'orange' to the set

```

For multiple item addition, utilize the `update()` method.

```python
myset = {"apple", "banana", "cherry"}
myset.update(["orange", "mango", "grapes"])  # Adds multiple items

```

Removal of items from sets is achievable through methods like `remove()` or `discard()`.

```python
myset = {"apple", "banana", "cherry"}
myset.remove("banana")  # Removes 'banana' from the set

```

Python's set operations, including union, intersection, difference, and symmetric difference, offer additional versatility.

```python
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
print(set3)  # Outputs: {1, 2, 3, 'a', 'b', 'c'}

```

## Dictionaries in Python

Dictionaries represent unordered collections of indexed key-value pairs enclosed in curly brackets. Each element in a dictionary consists of a key and its associated value.

```python
mydict = {"brand": "Ford", "model": "Mustang", "year": 1964}
print(mydict["model"])  # Outputs: Mustang

```

Python permits modifications to dictionary values, as well as addition and removal of key-value pairs.

```python
mydict = {"brand": "Ford", "model": "Mustang",

 "year": 1964}
mydict["year"] = 2020  # Updates the value of 'year' key

```

New key-value pairs can be effortlessly appended to dictionaries.

```python
mydict = {"brand": "Ford", "model": "Mustang", "year": 1964}
mydict["color"] = "red"  # Adds 'color': 'red' to the dictionary

```

To remove key-value pairs, the `pop()` method proves handy.

```python
mydict = {"brand": "Ford", "model": "Mustang", "year": 1964}
mydict.pop("model")  # Removes the 'model' key-value pair

```

## Control Structures in Python

Python supports various control structures, including loops and conditional statements.

### Python `for` Loop

The `for` loop iterates over a sequence of elements, executing a block of code for each item.

```python
for i in range(0, 12):
    print(i)

```

### Python `enumerate()` Function

The `enumerate()` function generates pairs comprising a count and a value from an iterable.

```python
stud = ["tony", "melakel"]

for i, v in enumerate(stud):
    print(v)

for v in enumerate(stud):
    print(v)

```

### Python Conditional Statements (`if`, `elif`, `else`)

Conditional statements allow execution of different code blocks based on specified conditions.

```python
x = 5
y = 3

if x > y:
    print(x)
elif x == y:
    print("equal")
else:
    print(y)

```

## Python Functions

Functions encapsulate reusable blocks of code, enhancing code organization and reusability.

```python
def h():
    print("hi")

h()  # Outputs: hi

```

Functions can accept parameters to facilitate dynamic behavior.

```python
def greet(name):
    print(f'Hello, {name}')

greet('melakel')  # Outputs: Hello, melakel

```

Python functions may include default arguments, which serve as fallback values if no arguments are provided during function invocation.

```python
def greet(name, age, id='1'):
    print(f'Hello, {name}. Age: {age}. ID: {id}')

greet('melakel', age=21)  # Outputs: Hello, melakel. Age: 21. ID: 1

```

## Python Argument Passing

Python supports two argument-passing mechanisms: positional arguments and keyword arguments.

### Positional Arguments

Positional arguments must be passed in the same order as defined in the function declaration.

```python
def greet(name, age):
    print(f'Hello {name}, you are {age} years old')

greet('John', 21)  # Outputs: Hello John, you are 21 years old

```

### Keyword Arguments

Keyword arguments are passed with a keyword and equals sign, allowing flexibility in argument order.

```python
def greet(name, age):
    print(f'Hello {name}, you are {age} years old')

greet(age=21, name='John')  # Outputs: Hello John, you are 21 years old

```

## Formatted String Literals (F-strings)

F-strings enable embedding of expressions inside string literals using curly braces `{}`. Expressions are evaluated and replaced with their values at runtime.

```python
name = "John"
age = 30
print(f"Hello, {name}. You are {age} years old.")  # Outputs: Hello, John. You are 30 years old.

```

F-strings support inclusion of any valid Python expression within curly braces.

```python
x = 10
y = 20
print(f"The sum of {x} and {y} is {x + y}.")  # Outputs: The sum of 10 and 20 is 30.

```

F-strings offer a concise and readable means of creating formatted strings in Python, catering to a wide array of string formatting needs.