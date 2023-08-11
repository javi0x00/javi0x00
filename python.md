# :memo: Notes
## PYTHON
---
### Resources
- [Python](https://www.python.org/)
- [The Python Tutorial](https://docs.python.org/3/tutorial/index.html)
- [Python Documentation contents](https://docs.python.org/3/contents.html)
- [venv — Creation of virtual environments](https://docs.python.org/3/library/venv.html)
- [PEP - Python Enhancement Proposals](https://www.python.org/dev/peps/)
- [Python Package Index](https://pypi.org/)
- [Tools and Features for Python Development](https://www.jetbrains.com/research/python-developers-survey-2017/#tools-and-features)
##### Style
- PEP8
- Pycodestyle
##### Zen
```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than -right- now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```
### Setup
Install ENV as package for creating virtual environment
```
$ sudo apt install python3-dev python3-venv
```
Install VIRTUALENV as package for creating virtual environment...
Install PIPENV as package for creating virtual environment...
### Setup Virtual Environment
Create virtual environment
```
$ python -m venv <virtual_environment_name>
```
Activate virtual environment
```
$ source <virtual_environment_name>/bin/activate
```
Deactivate virtual environment
```
$ deactivate
```
### COMMANDS
```
$ python --version
```
### Terms and concepts
1. What and why
2. What do
3. Why use
4. Getting started
5. Concepts
6. Code samples
7. API documentation
- Python REPL (Read-Evaluate-Print-Loop)
- IDLE (Integrated Development and Learning Environment)
- Python interpreter
- Python coding style
- Python scripts
- PIP
* Basic syntax
  * Keywords
    * I/O
      - format()
      - input()
      - open()
      - print()
      - return
  - Indentation
  - Comments single line, inline and multiline
* Data types
  * Numbers
    - Integers
    - Floating-Point
    - Complex
  - Strings
  - Booleans
* Operators
  * Arithmetics
    - PEMDAS (Parentheses, Exponent, Multiplication, Division, Addition, Subtraction)
  - Assignment
  - Comparison or relational
  * Logical
    - Truth table
    - Priority (not, and, or, left to right)
  - Identity
  - Membership
  - Bitwise
  - Ternary
* Data Structures
  - Variables
  - Lists
  - Tuples
  - Dictionaries
  - Sets
  - Extra
    - Arrays
* Methods
  - String
  - List
  - Tuple
  - Dictionary
  - Set
* Functions
  - Parameters/arguments
  * Return
    - Reference
    - Value
  - Scope
  - Lambda
* Control flow
  * Conditionals
    - if
    - if ... else
    - if ... elif ... else
  * Loops
    - for in
    - while
    - while else
  - pass
  - continue
  - break
  - Nested
* Generators
  - yield
  - yield from
  - next
* Errors and Exceptions
  - Errors
  - Exceptions
  - EOL (End Of line)
  * Handling Exceptions
    - try
    - except
    - finaly
    - raise
* POO
  * Object
    - Properties/Attributes
    - Methods/Actions
    - State
  * Class
    * Constructor
      - Properties
      - Initial state
    - Methods
  - Instance
  * Modularity
    - import
    - from ... import
    - Packages
    * Building and Distributing Packages
      - setup
      - sdist
      - install
      - uninstall
  * Encapsulation
    - __
  * Inheritance
    - Superclass
    - Subclass
    - Overwrite methods
    - Multi inheritance
  - Polymorphism

* Data persistence
  * External files
    * io module
      - Creation, Opening, Manipulation, Closing.
      - Pointer
  * Files
    - Binary files
    - JSON files
  - Databases

* Handle data files
  - Data serialization
  - Data deserialization
  * pickle module
    - dump
    - load

* Async IO
  - Async
  - Await
  - asyncio

* Asynchronous Comprehensions
  - asynchronous generator
  - async comprehensions
  - type-annotate generators

* Graphic User Interface
  - tkinter module

* Some special methods
  - __init__
  - __str__
  -  ...

*  Some Built-in functions
  - range()
  - len()
  - super()
  - isinstance()

* Some external libraries
  - smtplib
  - numpy
  - pandas
  - seaborn
  - matplotlib

- Regular Expressions
- Docstrings
- pydoc

- Doctest
- Unitest
---
## Software Developer
Built by [Javi](https://javierandres.dev) :copyright: 2020 - 2023
Found a bug or have an idea? [Contact me](https://javierandres.dev).
