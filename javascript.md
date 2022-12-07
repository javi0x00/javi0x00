# :memo: Notes
## JAVASCRIPT
---
### Resources
- [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript and HTML DOM Reference](https://www.w3schools.com/jsref/default.asp)
- [JavaScript at Microsoft](https://docs.microsoft.com/en-us/javascript/)
- [The Modern JavaScript Tutorial](https://javascript.info/)
- [JavaScript Tutorial](https://www.javascripttutorial.net/)
- [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)
- [Web technology for developers](https://developer.mozilla.org/en-US/docs/Web)
### Requirements
- A browser or server environment
### Terms and concepts
* ECMAScript
* JavaScript
* JavaScript uses
  - Web language
  - Interactive
  - Validate
  - Process
  - Front-End
  - Back-End
  - Desktop apps
  - Mobile apps

* script
  * script js?
    * The script tag
      - async
      - defer
    - External file
    - Comments
    - Syntax
    - Reserved Words
    - Keywords
    - Strict mode
    - Sloppy mode
  * The noscript tag

* Debugging
  - ```console```
  - Browser debugging tools
  * Snippets 
    - performance.now
  - debugger

* Statements
  - Values, Operators, Expressions, Keywords, and Comments.

* Expressions
  - values, variables, and operators, which computes to a value.

* Variables
  * Stages
    - Declaration
    - Initializing
    - Modification
  - Scope
  - Hoisting
  - Context
  * Coercion
    - Implicit
    - Explicit
  - Constants

* Data types
  * Primitives:
    - Boolean
    - String
    - Number
    - NaN - Not a Number
    - BigInt
    - undefined
    - null (Special primitive)
    * Symbol
      - Descriptions
  * Non-primitive:
    - object (for more complex data structures)

* Object wrapper
  - Boolean
  - String
  - Number

* Data structures
  * Arrays
    - Array of objects
  * Objects (Special non-data)
    * Propierties
      - Key, Value
      - getter
      - setter
      - prototype
      - call
      - apply
    * Tools
      - freeze
      - seal
  * Sets
    - WeakSets
  * Maps
    - WeakMaps
  * Proxies
    - Handler
  - Functions (non data structure)
- Properties
* Methods
  - Strings methods
  - Numbers methods
  - Array methods
  - Object methods
  - Set methods
  - Map methods

* Operators
  - Unary
  - Binary
  - Operand
* Operands
* Operations

* Operators
  - Arithmetic operators
  - Increment operators
  - Decrement operators
  - Assignment operators
  - Comparison operators
  - Logical Operators
  - “Unary +” Operator
  - Grouping
  - Concatenation
  - Type coercion
  - Type Operators
  - Bitwise Operators
  - Constructor
  - Short circuit operators
  - Spread operator or Rest operator

* Control structures
  - Sequential
  * Conditional
    - Comparisons
    - Strict equality check
    * Statements
      - if
      - if ... else
      - if ... else if ... else
      - switch
      - Ternary operator
  * Loops
    - Do While
    - While
    - For
    - For ... in
    - For ... of
    - ForEach
    - map
    - filter
    - "own loop"
    * Iterator object
      - keys
      - values
      - entries
  * Flow handling
      - Break
      - Continue

* Errors
  * Anatomy (is an object)
    * name/type
      - SyntaxError
      * Logic errors
        - ReferenceError
        - TypeError
    * message
      - Describe causing
    - file name
    - row or line
    - column or character
    - stack trace
  * Error handling
    - Try ... Catch ... Finally
    - Throw

* Destructuring
  - Assign by Destructuring
  - Destructuring, Functions, Arrays and Objects

* Objects
  - Propierties or Attributes
  - Methods
  - Dot notation
  - Square bracket notation
  - This
  * Binding
    - Implicit
    - Explicit
    - New
    - Window
  * Object literal (it is the opposite of destructuring)
    - Static and nonreusable
  * Object constructor
    - Dynamic and reusable
  - Property method

* Strings
  - Properties
  - Methods
  - Single, double and backtick quotes
  - Scaping characters
  - Concatenating strings

- Template literals or template strings or literal strings
- Fragments
- Templates and "clone"
- REST parameters (to received)
- Spread operator (to send)

* Functions
  * Funtion
    * With arguments
      - Parameter list
    * Without arguments
      - No parameter list
  - Implicit return or default return
  - Built-in
  - Function declaration (search in the same object, in the current object)
  - Function expression
  - Call function
  - Parameters function
  - Arguments function
  - Parameters by default
  - Anonymous function
  - Self-executing anonymous function
  - Immediately Invoked Function Expression
  - Fat Arrow Function (search in the global window)
  - Constructor function
  - Generator function (return an iterator)
  - IIFE function (runs as soon as it is defined)
  - Async Await
  - Callbacks
  - Promises
  - First-class function
  - Pure function

* Hoisting
  - hoist variable declaration (not initialization)
  - hoist functions declared
  - Register/Record
  - Execute

* Scope
  - Lexical scoping or static scoping
  - Scope chain
  - Global
  - Function
  - Block
  - Module

* Call Stack
  - LIFO (Last In First Out)
  - Stacktrace
  * Execution contexts
    - Global execution context
    - Function execution context

* Closures
  - retorna una función desde otra función, con acceso al entorno de variables 
  de un ámbito exterior
  - Ex:
```
function IamAclosure() {
  const varLocal = 'xyz'
  return function() {
    return varLocal.toUpperCase()
  }
}

const closure = IamAclosure()
```

* IIFE or Inmediately Invoked Function Expression

* Callback
  - Synchronous
  - Asynchronous

* Prototypes
  * Constructor object or constructor function
    - Dynamic and reusable
  - Object prototype (better with function declaration for the scope)
  - Prototype chain
  - Prototypical inheritance

* Syntactic sugar
  - Prototypes - Classes

* OOP
  * Classes
    - Declaration class
    - Expression class
    - Attributes or Properties
    - Methods
    - Static methods
    - Constructors
    - Inheritance
    - super
    - Scope chain
    - Private attributes or properties
    - Private methods
    - Setters
    - Getters
    - Overwrite methods
    - Polymorphism
  - Maps

* this keyword
  - is a reference according to the context
  * Mehods
    - call
    - apply
    - bind

* strict mode
  - avoid create global variables accidentally
  - readonly attributes
  - objects not extensibles
  - avoid duplicate parameters
  - octal system, octal literal
  - avoid errors with delete operator
  - 'arguments' and 'eval' are keywords
  - 'with' statement not allowed
  - more keywords
  - free functions

* Prototype
  - Prototypical inheritance

* Object
  - Static object (ej: Math)
 
* Some Objects
  - Window
  - Console
  - Date
  - Math
  - RegExp
  * Iterator object
    - keys
    - values
    - entries

* Some Methods
  - alert
  - confirm
  - prompt
  - test
  - exec

* Some Constructors
  - Object
  - Array
  - RegExp

* Some Object Methods
  - ```use strict````
  - Object.freeze
  - Object.seal
  - Object.assign
  - Object.keys
  - Object.values
  - Object.entries

* Regular Expressions

* Modules
  - module
  - nomudule
  - Import
  - Export
  - Export default
  - Alias

* Code ordering
  - Import modules
  - Variables
  - Functions
  - Executables

* Timers
  - TimeOut
  - ClearTimeOut
  - TimeInterval
  - ClearInterval

* Asynchronous
  - I/O
  - Single thread
  - Multi thread
  - Event loop
  - Stack
  - LIFO
  - Concurrence
  - Parallelism
  - Blocking
  - Non-blocking
  - Synchronous
  - Asynchronous

* Callbacks
  - Callback hell

* Recursive
* Trampoline (technique)
* Closure

* Promises
  - Pending
  - Fulfilled
  - Rejected
  * Resolve
    - Then
  * Reject
    - Catch
  * Methods
    - all

* Async Await
  - Try
  - Catch

* Iterables & Iterators
  - next
  - done

* Generators
  - yield

* Async functions

* Reactivity
  * State (the data at a specific time)
    * UI based on state
      - change data, then, change content (reder)
  * Component (visual pattern, independent code snippet)
    - reusable
    - unique function
    - independent
    - self-contained

* Window
  - This, Self and Window
  - Global
  * Scope
    - Call
    - Apply
    - Bind

* API (Application Programming Interface)
  * Web APIs
    - Console
    - DOM (Document Object Model)
    - CSSOM (CSS Object Model)
    - BOM (Browser Object Model)
    - Fetch
  - External APIs

* API's Architectures
  - REST (Representational State Transfer)
  - SOAP (Simple Object Access Protocol)

* DOM Nodes
  * Node is an object with properties and methods
    * Properties
      - Like ids, classes, styles, texts, etc
    * Methods
      - For finding/adding/removing/altering or handle on manipulating
  - tree nodes
  - nodelist
  - array of nodes
  - Elements
  - Traversing
  - Fragments

* DOM Events
  - Allow handle on manipulating the DOM dynamically, or on demand
  - Listeners
  - Remove

* DOM Event flow
  - Propagation
  - Bubble
  - Capture
  - Stop propagation or stop bubbling
  - preventDefault

* DOM Event delegation

* Responsible and Responsive
* User Agent

* CORS (Cross-Origin Resource Sharing)
* HTTP response status codes
* HTTP verbs

* JSON
  - Parse
  - Stringify

* XML
* JSON
* AJAX
  - ActiveXObject
  - XMLHTTPRequest
* Fetch
  - With Async Await
* Axios
  - With Async Await

* SPA (Single Page Application)

* PWA (Progresive Web Application)
  - Fast
  - Instalable
  - Offline support
  * Requeriments
    - Manifest
    - Domain
    - Fetch event listener

* Service Workers
  - Base of the PWA
  - Working offline
  - Not access the DOM
  - Automatly load
  - Work without interferir

* Functional JS
  - Inmutability
  - Separate data functions
  - First-class functions

* Higer order functions
* Pure function
* Closure
* Partials, Currying
* Composition

* Engine
  - Source
  - AST (Abstract Syntax Tree)
  - Bytecode
  - Machinecode

* Event loop
  * Stack FILO
    - push
    - pop
  - Heap
  * Queue FIFO
    - Scheduled tasks (e.g. setTimeout)
    - Microtask queue (e.g. Promises)
    - task queue

* Design Patterns
  * Create code
    - Class Pattern
    - Constructor Pattern
    - Singleton Pattern
    - Factory Pattern
  * Organize code
    - Module Pattern
    - Mixin Pattern
    - Namespace Pattern
    - Mediator Pattern

* Hashing
  - Auth
  - bcrypt

* Tools
  - Babel
  - ESLint
  - Webpack
  - Gulp
  - Style guide (Standard, Google, Airbnb)

* Testing
  - Test Driven Development or TDD
  * Techniques
    - Integration
    - End to End
    - Unit
    - Static
  * Tools
  - Jest
  - Cypress
---
## Software Developer
[Javier Andrés Garzón Patarroyo](https://javierandresgp.com)
