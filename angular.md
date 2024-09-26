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

* Components
  - Metadata
  - Selectors
  - Templates
  - Styles
  * Clases
    * Attributes
      - Properties
      * Methods
        - Constructor
- Services
- Dependencies
- Directives
- Routing

* Components
  * Decorator
    * Attributes
      - Selector
      - Template
      - Styles
  * Class
    - Attributes
  * Lifecycle
    - ngOnInit
    - ngOnChanges
    - ngOnDestroy
* Create a new component
  - Manually
  * Automatically
    - CLI
  - Template inline
  - Styles inline
- Declarate a new component
- Use a new component
- Interpolation
- Event
- Property binding
- Event binding
- Handling Events
- Two-way binding, bidirectional binding, Banana in a Box
* Data binding
  - Interpolation
  * Binding
    - One way binding
    - Event binding
    - Two way binding
* Directives
  * Component
    * Built-in
      - @Component
      - @Module
    - Custom
  * Attribute
    - Ex: ngStyle, ngClass, ngModel
  * Structure
    - Ex: ngIf, ngFor, ngSwitch, ngPlural, ngTemplate, ngComponentOutlet
* Component interaction
  - @Input
  - @Output
* Services
  - Data Services
* Modules
  * Import module
    - Ex: RouterModule
    - Ex: FormsModule

- Routing

- Install packages
- Config file
- The RxJS library
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
