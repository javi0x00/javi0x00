# :memo: Notes
## REACT
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [React](https://react.dev/)
- [ViteJS](https://vitejs.dev/)
- [Create React App](https://create-react-app.dev/)
- [React Bootstrap](https://react-bootstrap.github.io/)
- [styled-components](https://styled-components.com/)
- [MATERIAL-UI](https://material-ui.com/)
* Extension
  - react developer tools
- [Training React](https://github.com/javierandres-dev/training-react)
### Requirements
- Nodejs
### Setup
#### Vite
```
$ npm create vite@latest
```
#### Vite & TypeScript
```
$ npm create vite@latest <app-name> -- --template react-ts
```
##### Deploy to a Github pages a React App (Vite)
Install gh-pages
```
$ npm install --save-dev gh-pages
```
Set package.json
```
"homepage": "https://<user>.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d dist"
}
```
Set vite.config.js
```
base: "/<repo>"
```
Run
```
$ npm run predeploy
$ npm run deploy
```
#### CRA
```
$ npx create-react-app <name>
$ cd <name>
$ npm start
```
#### CRA & TypeScript
```
$ npx create-react-app my-app --template typescript
$ npm install --save @types/react
```
##### Deploy to a Github pages a React App (CRA)
Install gh-pages
```
$ npm install --save-dev gh-pages
```
Set package.json
```
"homepage": "https://<user>.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d build"
}
```
Run
```
$ npm run predeploy
$ npm run deploy
```
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
