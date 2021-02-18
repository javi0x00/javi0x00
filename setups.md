# :memo: Notes
## SETUPS
- - -
###  TypeScript
```
npm install --save-dev typescript
node_modules/.bin/tsc --init
node --save-dev
```
- - -
###  React & TypeScript
```
npx create-react-app my-app --template typescript
```
- - -
###  Deploy to a Github page a React App
$\my-app
```
npm install --save-dev gh-pages
```

package.json
```
"homepage": "https://javierandresgp.github.io/<repo>"
"scripts": {
  "predeploy": "npm run build ",
  "deploy": "gh-pages -d build"
}
```

$\my-app
```
npm run build
npm run deploy
```
- - -
### Visual Studio Code
#### Extensions
* Atom One Dark Theme - Mahmoud Ali
* Better Comments - Aaron Bond
* Bracket Pair Colorizer2 - CoenraadS
* C/C++ - Microsoft
* Code Runner - Jun Han
* Debugger for Chrome - Microsoft
* Debugger for Java - Microsoft
* Dracula Official - Dracula Theme
* ES7 React/Redux/GraphQL/React-Native snippets - dsznajder
* ESLint - Dirk Baeumer
* Flatland Monokai Theme - gerane
* GitHub Pull Requests and Issues - GitHub
* Java Extension Pack - Microsoft
* Java Test Runner - Microsoft
* JavaScript (ES6) code snippets - charalampos karypidis
* Jupiter - Microsoft
* Language Support for Java(TM) by Red Hat
* Live Server - Ritwick Dey
* Maven for Java - Microsoft
* PHP Intelephense - Ben Mewburn
* PHP Intelephense - Felix Becker
* Prettier Code formatter - Prettier
* Project Manager for Java - Microsoft
* Python - Microsoft
* Quokka Statusbar Buttons - Sketchbuch
* Quokka.js - Wallaby.js
* Remote WSL - Microsoft
* Remove empty lines - Alexander
* REST Client - Huachao Mao
* Simple React Snippets - Burke Holland
* Tabnine Autocomplete AI - TabNine
* Tailwind CSS IntelliSense - Brad Cornes
* Visual Studio IntelliCode - Microsoft
* Vim - vscodevim
* vscode-icons - Microsoft
* vscode-styled-components - Julien Poissonnier
#### settings.json
```
{
  "editor.fontFamily": "'Consolas, 'Courier New', monospace",
  "editor.tabSize": 2,
  "editor.fontSize": 16,
  //"editor.wordWrap": "wordWrapColumn",
  "editor.wordWrap": "on",
  "editor.autoIndent": "advanced",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.detectIndentation": true,
  "editor.multiCursorModifier": "ctrlCmd",
  "editor.snippetSuggestions": "top",
  "editor.renderWhitespace": "all",
  "editor.rulers": [
    {
      "column": 80,
      "color": "#FF00FF"
    }
  ],
  "emmet.syntaxProfiles": {
    "javascript": "html"
  },
  "emmet.includeLanguages": {
    "javascript": "html"
  },
  "emmet.triggerExpansionOnTab": true,
  "extensions.ignoreRecommendations": true,
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "workbench.startupEditor": "newUntitledFile",
  "workbench.colorTheme": "Flatland Monokai",
  "workbench.iconTheme": "vscode-icons",
  "[markdown]": {
    "editor.formatOnSave": false,
    "files.trimTrailingWhitespace": false
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
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
  "[php]": {
    "editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
  },
  "prettier.singleQuote": true,
  "php.validate.executablePath": "C:/xampp/php/php.exe",
  "terminal.integrated.fontFamily": "Consolas, 'Courier New', monospace",
  "terminal.integrated.fontSize": 16,
  "python.showStartPage": false,
  "editor.suggestSelection": "first",
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
  "python.languageServer": "Microsoft",
  "workbench.sideBar.location": "left",
  "vsicons.dontShowNewVersionMessage": false,
  "java.home": "C:\\Program Files\\Java\\jdk-11.0.9",
  "tabnine.experimentalAutoImports": true,
  // Command Prompt
  //"terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe"
  // PowerShell
  "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  "javascript.preferences.quoteStyle": "single",
  "typescript.preferences.quoteStyle": "single",
  "prettier.jsxSingleQuote": true
  // Git Bash
  //"terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe"
  // Bash on Ubuntu (on Windows)
  //"terminal.integrated.shell.windows": "C:\\Windows\\System32\\bash.exe"
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
