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
- [Angular Docs (previous)](https://angular.io/docs)
- [Angular v18](https://angular.dev/)
- [Angular Tutorials](https://angular.dev/tutorials)
- [The Angular CLI](https://angular.dev/tools/cli)
- [Angular Language Service](https://angular.dev/tools/language-service)
- [Angular DevTools](https://angular.dev/tools/devtools)
- [Angular Material](https://material.angular.io/)
- [Material Design](https://m3.material.io/)
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
100% StandAlone
```
$ ng generate @angular/core:standalone
```
---
Config Angular CLI
```
$ npm i -g @angular/cli
$ ng config -g cli.packageManager <yarn/pnpm/bun>
```
---
Add Angular Eslint
```
$ ng add @angular-eslint/schematics<@18.1.0.>
```
---
Add Angular Material
```
$ ng add @angular/material
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
- Library
- Framework
- Structural platform
- Angular
- Angular Way

* First steps
  - Install de Angular CLI
  - Create a workspace and initial application
  - Run the application
  - Up app
  - Down app

* Builders
  - browser (Webpack)
  - browser-esbuild (Vite Esbuild)
  - application (Vite Esbuild by default)
  - dev-server (Vite Esbuild)

- SPA
- Structure
- Default component
- Default selector
- Flow

- Modules
- Standalone Components

- Providers
- Components
- Services
- Dependencies
- Directives
- Syntax Template
- Pipes
- Routing
- Forms
- Observables
- Signals
- Effects
- Http
- Caching

* Control Flow
  - Directives
  - Syntax Template

* Change Detection
  - OnPush (Only when...User/Param/Event)
  - changeDetectionRef
  - markForChanges

* Config
  - Providers

* Component
  * Create
    - Manually
    * Automatically
      - CLI
  - import
  - Metadata
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

* Services
  * Built-in
    - HttpClient
  - Custom

* Dependencies
  * Inject
    - on constructor method
    * with inject
      - options

* Directives
  * Built-in
    * Attribute
      - Property binding
      - Styles
    * Structure
      * Control Structures
        - Conditionals
        - Loops
        - Deferrable views
        - Container
        - Content
    - Event
    - Image
  * Custom
    - Attribute
    - Structure

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
    - redirect with function
  - Guards
  - Resolvers

* Forms
  * Template driven
    - FormsModule
  * Reactive
    * ReactiveFormsModule
      - FormGroup
      - FormBuilder
      - Validators
      - FormControl
      - FormArray

* Observables
  - subscribe
  - unsubscribe
  - pipe
  - outputFromObservable
  - outputToObservable

* Signals
  - signal
  - computed
  - set
  - update
  - mutate
  * Signal Inputs
    - input
    - required
    - transform
    - alias
  * Signal Outputs
    - output
    - emit
    - outputFromObservable
    - outputToObservable
  * Signal Queries
    - viewChild
    - viewChildren
  * Model Inputs
    - model

* Effects
  - effect

* HTTP Client Service
  * HttpClientModule
    - HttpClient
  * provideHttpClient
    - HttpClient

* Caching
  - Pipes
  - Pure pipe
  - Memoization

- Install packages
- Config file
* Reactive Programming
  - The RxJS library
- CSR | Client Side Render
* SSR | Server Side Render
  - Hydration
  - WIZ
- SSG | Static Site Generation
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
