# :memo: Notes
## NODEJS
---
### Resources
- [Node.js](https://nodejs.org)
* Node Version Manager
  - [nvm](https://github.com/nvm-sh/nvm)
  - [NVM for Windows](https://github.com/coreybutler/nvm-windows)
  - [n](https://github.com/tj/n)
### Terms and concepts
* Node.js
  * Fork
    - io.js
  * JavaScript runtime environment
    - Based on JS language
    - Built on Google's V8 engine for Backend
    - Interpeter
    - Based around events
    - Multiplatform
    - Asynchronous
    - I/O model
    - Asynchronous non blocking model
  * Asynchronous non blocking model
    - Synchronous, parallelism, simultaneous
    - Asynchronous, concurrence, alternate
    - Blocking
    - Non-blocking
    - Reactor design pattern
  * Single thread
    - Based on callbacks
    - Event loop

* REPL

* Good practices
  * Order
    - Libraries, Modules
    - Constants
    - Objects, Variables
    - Functions
    - Events
    - Executions
    - Mode strict
  * Prefer
    - lowerCamelCase
    - Single quotes

* Modules
  * Types
    - Core modules
    - Local modules
    - Third-party modules

* Core modules or Built-in modules
  - Stability level
  * Some modules of the core
    - Globals
    - Process
    - OS
    - File System
    * Events
      - Action into app
      - Define
      - Emit
      - Listen
      * EventEmitter
        - Emitters
      - Event Handler or Event Listener
    * HTTP
      * Model: client-server
      * HTTP protocol
      * Port
      * Request
        - Methods HTTP or Verbs HTTP
      * Response
        - Status codes HTTP
      - CRUD (Create, Read, Update, Delete)
    - URL
    - Routing
    - Buffer
    - Stream
    - Util
    - Timers
    - Path
    - Query String
    - Sniffer
    * Forms
      - GET
      - POST
    - Debugger
    - readLine
    - assert
    - v8

* Third-party modules

* NPM (Node Package Manager)
  - Package
  - Module
  - Dependency
  * Types packages
    - Globals
  * Installing packages
    - Unique: ```npm install <package_name>``` (not recommended)
    - Global: ```npm install <package_name> -g```
    - Project dependency: ```npm install <package_name> --save``` (package.json)
    - Development dependency: ```npm install <package_name> --save-dev``` (package.json)
  * Uninstalling packages
  * package.json
    - ```npm init``` (for a new project)
    - ```npm install``` (for an existing project)
  * package-lock.json
    - autogenerate when package.json or tree node_modules is modify
    - hold record of all dependencies
    - describe the tree generate for next installations
    - contain details

* Promises
  - pending
  - resolve
  - reject
  - then
  - catch
  - chaining promises
  - async
  - await

* Callback function

* Method chaining

* Inheritance

* Classes
  - class
  - constructor
  - extends
  - static
  - getter
  - setter
  - private field
  - public field

* Middlewares
  - Are functions that running after request and running before response.
  - Are functions that have access to the request object (req), the response object (res) and the next() function.
  * Scope
    - Global
    - Local
  * Type
    - Filters
    - Provider

* Some middlewares
  * Built-in
    - static
  * External
    - favicon
    - logger
    - cookie-parser
    - cookie-session
    - body-parser

* Full Stack JavaScript Developer
  - JAM stack (Javascript, APIs, Markup)
  - MERN stack (MongoDB, Express, React, Node)
  - MEAN stack (MongoDB, Express, Angular, Node)
  - MEVN stack (MongoDB, Express, Vue, Node)
  - MESN stack (MongoDB, Express, Svelte, Node)
---
## Software Developer
Built by [Javi](https://javierandres.dev) :copyright: 2020 - 2023  
Found a bug or have an idea? [Contact me](https://javierandres.dev).
