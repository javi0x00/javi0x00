# :memo: Notes
## SETUPS
- - -
### JSDoc
```
$ yarn add jsdoc
$ npm i jsdoc
```
jsdoc.json
```
{
  "plugins": [],
  "source": {
    "includePattern": ".js$",
    "excludePattern": "(node_modules|docs)",
    "include": ["./src"],
    "exclude": ["./node_modules", "./docs"]
  },
  "templates": {
    "cleverLinks": false,
    "monospaceLinks": false
  },
  "opts": {
    "encoding": "utf8",
    "destination": "./docs/",
    "recurse": true
  }
}
```
```
$ jsdoc -c jsdoc.json
$ npx jsdoc -c jsdoc.json
```
package.json
```
{
  "scripts": {
    "docs": "jsdoc -c jsdoc.json"
  }
}
```
$ .vscode/settings.json
```
{
  "javascript.implicitProjectConfig.checksJs": true
}
```
- - -
###  TypeScript
```
$ npm install --save-dev typescript
$ node_modules/.bin/tsc --init
$ node --save-dev
```
- - -
###  React & TypeScript
```
$ npx create-react-app my-app --template typescript
$ npm install --save @types/react
```
- - -
###  Deploy to a Github page a React App
$ \my-app
```
$ npm install --save-dev gh-pages
```

package.json
```
"homepage": "https://<user>.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d build"
}
```

$ \my-app
```
$ npm run build
$ npm run deploy
```
- - -
### Visual Studio Code
#### Extensions
* Atom One Dark Theme - Mahmoud Ali
* Auto Rename Tag - Jun Han
* Better Comments - Aaron Bond
* Bracket Pair Colorizer2 - CoenraadS
* C/C++ - Microsoft
* Code Runner - Jun Han
* Debugger for Chrome - Microsoft
* Debugger for Java - Microsoft
* Docker - Microsoft
* Dracula Official - Dracula Theme
* ES7 React/Redux/GraphQL/React-Native snippets - dsznajder
* ESLint - Microsoft
* Flatland Monokai Theme - gerane
* GitHub Copilot - GitHub
* GitHub Pull Requests and Issues - GitHub
* GitLens - GitKraken
* Guides - spywhere
* Highlight Matching Tag - vincaslt
* Indent Rainbow - Oderwat
* Java Extension Pack - Microsoft
* Java Test Runner - Microsoft
* JavaScript (ES6) code snippets - charalampos karypidis
* Jupiter - Microsoft
* Jupiter Keymap - Microsoft
* Jupiter Notebook Renderers - Microsoft
* Language Support for Java(TM) by Red Hat
* Live Server - Ritwick Dey
* Maven for Java - Microsoft
* npm - Microsoft
* npm Intellisense - Christian Kohler
* One Dark Pro - binaryfy
* PHP Intelephense - Ben Mewburn
* PHP Intelephense - Felix Becker
* Prettier Code formatter - Prettier
* Project Manager for Java - Microsoft
* Pylance - Mricrosoft
* Python - Microsoft
* Quokka Statusbar Buttons - Sketchbuch
* Quokka.js - Wallaby.js
* Remote WSL - Microsoft
* Remove empty lines - Alexander
* REST Client - Huachao Mao
* Simple React Snippets - Burke Holland
* SQL Formatter - adpyke
* Svelte 3 Snippets - fivethree
* Svelte Auto Import - pivaszbs
* Svelte for VS Code - Svelte
* Svelte Intellisente - ardenivanov
* Tabnine Autocomplete AI - TabNine
* Tailwind CSS IntelliSense - Tailwind Labs
* Version Lens - pflannery
* Visual Studio IntelliCode - Microsoft
* Vim - vscodevim
* vscode-icons - VSCode Icons Team
* vscode-styled-components - Styled Components
#### Fonts
* [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
##### settings.json
```
{
  "editor.bracketPairColorization.enabled": true,
  "editor.detectIndentation": true,
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontSize": 13,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.fontLigatures": true,
  "editor.guides.bracketPairs": "active",
  "editor.lineHeight": 22,
  "editor.multiCursorModifier": "ctrlCmd",
  "editor.renderWhitespace": "all",
  "editor.rulers": [
    {
      "column": 80,
      "color": "#FF00FF"
    }
  ],
  "editor.snippetSuggestions": "top",
  "editor.suggestSelection": "first",
  "editor.tabSize": 2,
  "editor.wordWrap": "wordWrapColumn",
  "editor.wordWrapColumn": 80,
  "extensions.ignoreRecommendations": true,
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "javascript.preferences.quoteStyle": "single",
  "javascript.updateImportsOnFileMove.enabled": "always",
  "prettier.singleQuote": true,
  "prettier.jsxSingleQuote": true,
  "svelte.enable-ts-plugin": true,
  "terminal.integrated.fontFamily": "Consolas, 'Courier New', monospace",
  "typescript.preferences.quoteStyle": "single",
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
  "workbench.colorTheme": "One Dark Pro",
  "workbench.iconTheme": "vscode-icons",
  "workbench.startupEditor": "none",
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[svelte]": {
    "editor.defaultFormatter": "svelte.svelte-vscode"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.formatOnSave": false,
    "files.trimTrailingWhitespace": false
  }
}
```
- - -
### VI
#### .vimrc
```
set encoding=utf-8
set number
set colorcolumn=80
syntax enable
colorscheme ron
filetype on
augroup C_Python_JavaScript_Settings
        autocmd fileType java source ~/vi-settings/java.vi
        autocmd fileType sql source ~/vi-settings/sql.vi
        autocmd fileType c source ~/vi-settings/c.vi
        autocmd fileType python source ~/vi-settings/python.vi
        autocmd fileType javascript source ~/vi-settings/javascript.vi
        autocmd fileType css source ~/vi-settings/css.vi
        autocmd fileType html source ~/vi-settings/html.vi
augroup END
```
#### Default
```
set tabstop =2
set softtabstop =2
set shiftwidth =2
set expandtab
```
#### Python
```
set tabstop =4
set softtabstop =4
set shiftwidth =4
set expandtab
```
#### C
```set cindent```
- - -
### Shell
#### Betty linter
* Clone the [Betty repo](https://github.com/holbertonschool/Betty)
* ```cd``` into the Betty directory
* Install the linter with ```sudo ./install.sh```
* New file called ```betty```, and copy the script below:
```
#!/bin/bash
# Simply a wrapper script to keep you from having to use betty-style
# and betty-doc separately on every item.
# Originally by Tim Britton (@wintermanc3r), multiargument added by
# Larry Madeo (@hillmonkey)

BIN_PATH="/usr/local/bin"
BETTY_STYLE="betty-style"
BETTY_DOC="betty-doc"

if [ "$#" = "0" ]; then
    echo "No arguments passed."
    exit 1
fi

for argument in "$@" ; do
    echo -e "\n========== $argument =========="
    ${BIN_PATH}/${BETTY_STYLE} "$argument"
    ${BIN_PATH}/${BETTY_DOC} "$argument"
done
```
* Once saved, exit file and change permissions to apply to all users with ```chmod a+x betty```
* Move the ```betty``` file into ```/bin/``` directory or somewhere else in your ```$PATH``` with ```sudo mv betty /bin/```
* You can now type ```betty <filename>``` to run the Betty linter!
- - -
###### :globe_with_meridians: Social
[WebSite](https://www.javierandresgp.com)  |  [GitHub](https://github.com/javierandresgp/)  |  [Linkedin](https://www.linkedin.com/in/javierandresgp/)  |  [Twitter](https://twitter.com/javierandresgp0)  |  [freeCodeCamp](https://www.freecodecamp.org/javierandresgp)  |  [HackerRank](https://www.hackerrank.com/javierandresgp)  |  |  [Reddit](https://www.reddit.com/user/javierandresgp0)  |  [StackOverflow](https://stackoverflow.com/users/13728583/javierandresgp)  |  [Medium](https://medium.com/@javierandresgp)  |  [Quora](https://es.quora.com/profile/Javier-Andr%C3%A9s-9)  |  [Meetup](https://www.meetup.com/es/members/305321275/)  |  [Facebook](https://www.facebook.com/javierandresgp0/)  |  [Instagram](https://www.instagram.com/javierandresgp/)
