# :memo: Notes
## NODEJS
- - -
### Resources
* [Node.js](https://nodejs.org)
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
    - HTTP
    - Buffer
    - File System
    - Stream
    * Events
      - Action into app
      - Define
      - Emit
      - Listen
      * EventEmitter
        - Emitters
      - Event Handler or Event Listener
    - Util
    - Timers
    - Path
    - URL
    - Query String
    - Sniffer
    * Forms
      - GET
      - POST
    - Debugger
    - v8
    - readLine
    - os
    - url
    - assert

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
  * Some packages project dependency
    - node-inspector
    - supervisor
    - nodemon
    - forever
    - pm2
    - formidable
    - fs-extra
    - q
  * Some packages development dependency
    - grunt
    - gulp
    - webpack
    -bower
    - stylus
    - less
    - browserify
    - jshint
    - babel

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

* Model: client-server
  * HTTP protocol
    * Request
      - Methods HTTP or Verbs HTTP
    * Response
      - Status codes HTTP

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


* Some Nodejs frameworks
  - Express
  - Sails
  - Hapi
  - Locomotive
  - Koa
  - Kraken
  - Express.IO
  - SocketStream
  - Geddy
  - Total
  - Partial
  - Flatiron

* Express
  * Core
    - Express
    - Application
    - Request
    - Response
    - Router
  * Web application framework
    - Routes
    - Parameters
    - Forms
    - Upload files
    - Cookies
    - Sessions
    - Templates

* Middlewares
  - Are functions that have access to the request object (req), the response object (res).
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

* Express generator

* Manual generator

* Templates Engines
  - Jade
  - Ejs
  - Handlebars
  - Pug
  - Hogan
  - Mustache
  - Dust
  - Nunjucks

* Ghost
  - Platform for creating a new media platform

* Data Persistence
  - CRUD (Create, Read, Update, Delete)
  - REST (Representational State Transfer)
  * SQL (Structured Query Language)
    - MySQL
  * NoSQL (Not only SQL)
    - Mongo
  * API REST MySQL
    - mysql
    - express-myconnection
    - express-method-override
  - API REST MongoDB

* MongoDB
  - Based on JS
  - BSON format (Binary Script Object Notation)
  * Documental (records)
    - Collections (tables)
    - 16Mb limit
  * Some commands
    - mongod
    - mongo
    - show dbs
    - use <name db>
    - show collections
  * ODM
    - Mongoose

* Isoformicas app

* Full Stack JavaScript Developer
  - MERN (MongoDB, Express, React, Node)
- - -
## Software Developer
[Javier Andrés Garzón Patarroyo](https://javierandresgp.com)
