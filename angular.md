# :memo: Notes
## ANGULAR
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Angular Docs v16](https://v16.angular.io/docs)
- [Angular Docs v18](https://angular.dev/)
- [Angular Tutorials](https://angular.dev/tutorials)
- [The Angular CLI](https://angular.dev/tools/cli)
- [Angular Language Service](https://angular.dev/tools/language-service)
- [Angular DevTools](https://angular.dev/tools/devtools)
### Requirements
- Nodejs
### Install
Angular CLI
```
$ npm install -g @angular/cli
$ ng version
```
### Setup
Project
```
$ ng new <app name>
$ ng new <app name> --directory ./
$ cd <app name>
$ ng serve
$ ng serve --open
```
Components
```
$ ng generate component <name>
```
Simple component
```
$ ng generate component <name> --skip-tests --inline-style --inline-template
```
Services
```
$ ng generate service <name>
```
Guards
```
$ ng generate guard <name>
```
Custom Directive
```
$ ng generate directive <name>
```
Custom Pipe
```
$ ng generate pipe <name>
```
---
Migrate Angular project from CSS to SCSS (Sass) [Also for Angular Material Projects]
```
#### Please Backup your project first!!!!!!!!
# run this in your project root folder
# rename all your src files
cd src
find . -name "*.css" -exec bash -c 'mv "$1" "${1%.css}".scss' - '{}' \;
cd ..

# change angular cli config in angular.json
sed -i -e 's/styles.css/styles.scss/g' angular.json

# Change all ts-files (change .css to .scss) in @Module styleUrls
find ./src -name "*.ts" -exec sed -i -e 's/\(.*styleUrls.*\)\.css\(.*\)/\1\.scss\2/g' {} +
find ./src -name "*.ts-e" -exec bash -c 'rm "$1"' - '{}' \;

# Angular <6.1 (running on 8 doesn't break anything)
ng set defaults.styleExt scss
# Angular 6+ version of the above one
ng config schematics.@schematics/angular:component.styleext scss
# Angular 9> version of the above one
ng config schematics.@schematics/angular:component.style scss

# Add node-sass npm module
npm install node-sass --save-dev

# Everything should work now!
```
### Terms and concepts
- Framework
- Angular

* First steps
  - Install de Angular CLI
  - Create a workspace and initial application
  - Run the application
  - Up app
  - Down app

- SPA
- Structure
- Default component
- Default selector
- Flow

- Modules
- Standalone Components
- Components
- Services
- Dependencies
- Directives
- Pipes
- Routing
- Forms

* Components
  - Metadata
  - Selectors
  - Templates
  - Styles
  - Class

* Components
  * Create
    - Manually
    * Automatically
      - CLI
  - import
  * Decorator
    * Attributes
      - Selector
      * Template
        - external
        - inline
      * Styles
        - external
        - inline
  * Class
    * Attributes
      - Properties
      * Methods
        - Constructor
  * Lifecycle
    - ngOnInit
    - ngOnChanges
    - ngOnDestroy

- Event
- Handling Events
- Two-way binding, bidirectional binding, Banana in a Box

* Data binding
  - Interpolation
  * Binding
    - Property binding
    - One way binding
    - Two way binding
    - Event binding

* Component interaction
  * @Input
    - Property binding
  * @Output
    - EventEmitter
  - Services

- Services

* Dependencies
  * Inject
    - on constructor method
    - with inject

* Directives
  * Built-in
    * Attribute
      - Property binding
      - Styles
    * Structure
      * Control Structures
        - Conditionals
        - Loops
        - Container / Content
    - Event
  - Custom

* Pipes
  - Built-in
  - Custom

* Routing
  * Routes
    - single
    - params
  * Directives
    - router-outlet
    - routerLink
    - routerLinkActive
    - ngClass
  * ActivatedRoute
    - params
  * Router
    - redirect

* Forms
  * Template driven
    - FormsModule
  * Reactive
    - ReactiveFormsModule

- Install packages
- Config file
- The RxJS library
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
