# :memo: Notes
## SETUPS
---
### Mapping of IP addresses to URLs
/etc/hosts
```
127.0.0.1	localhost
::1		localhost
# 127.0.1.1	pop-os.localdomain	pop-os
# xxx.xxx.xxx.xxx	subdomain.domain.com
```
### JSDoc
Install
```
$ yarn add jsdoc
$ npm i jsdoc
```
jsdoc.json file
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
Run
```
$ jsdoc -c jsdoc.json
$ npx jsdoc -c jsdoc.json
```
package.json file
```
{
  "scripts": {
    "docs": "jsdoc -c jsdoc.json"
  }
}
```
.vscode/settings.json file
```
{
  "javascript.implicitProjectConfig.checksJs": true
}
```
---
### Visual Studio Code - CUSTOM settings.json
```
{
  "editor.bracketPairColorization.independentColorPoolPerBracketType": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.codeActionsOnSave": [
    "source.fixAll.eslint"
  ],
  "editor.cursorBlinking": "expand",
  "editor.cursorStyle": "line",
  "editor.cursorWidth": 1,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.detectIndentation": true,
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontLigatures": true,
  "editor.fontSize": 16,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.guides.bracketPairs": true,
  "editor.lineHeight": 0,
  "editor.minimap.enabled": false,
  "editor.minimap.maxColumn": 80,
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
  "eslint.validate": ["javascript", "javascriptreact", "typescript", "vue"],
  "extensions.ignoreRecommendations": true,
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "javascript.preferences.quoteStyle": "single",
  "javascript.updateImportsOnFileMove.enabled": "always",
  "prettier.singleQuote": true,
  "prettier.jsxSingleQuote": true,
  "svelte.enable-ts-plugin": true,
  "terminal.integrated.fontFamily": "JetBrains Mono",
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.copyOnSelection": true,
  "terminal.integrated.cursorBlinking": true,
  "typescript.preferences.quoteStyle": "single",
  "typescript.tsdk": "node_modules/typescript/lib",
  "workbench.colorTheme": "One Dark Pro",
  "workbench.colorTheme": "One Dark Pro Darker",
  "workbench.iconTheme": "vscode-icons",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.startupEditor": "none",
  "vsicons.dontShowNewVersionMessage": true,
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
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
    "editor.defaultFormatter": null,
    "editor.formatOnSave": false,
    "files.trimTrailingWhitespace": false
  }
}
```
---
### VI
.vimrc file
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
```
set cindent
```
---
### Shell
#### Betty linter
- Clone the [Betty repo](https://github.com/holbertonschool/Betty)
- ```cd``` into the Betty directory
- Install the linter with ```sudo ./install.sh```
- New file called ```betty```, and copy the script below:
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
- Once saved, exit file and change permissions to apply to all users with ```chmod a+x betty```
- Move the ```betty``` file into ```/bin/``` directory or somewhere else in your ```$PATH``` with ```sudo mv betty /bin/```
- You can now type ```betty <filename>``` to run the Betty linter!
---
###### :globe_with_meridians: Social
[GitHub](https://github.com/javierandres-dev/)  |  [Linkedin](https://www.linkedin.com/in/javierandres-dev/)
{::comment}
[Website](https://.../)  |  [Twitter](https://twitter.com/javierandresgp0)  |  [freeCodeCamp](https://www.freecodecamp.org/javierandresgp)  |  [HackerRank](https://www.hackerrank.com/javierandresgp)  |  |  [Reddit](https://www.reddit.com/user/javierandresgp0)  |  [StackOverflow](https://stackoverflow.com/users/13728583/javierandresgp)  |  [Medium](https://medium.com/@javierandresgp)  |  [Quora](https://es.quora.com/profile/Javier-Andr%C3%A9s-9)  |  [Meetup](https://www.meetup.com/es/members/305321275/)  |  [Facebook](https://www.facebook.com/javierandresgp0/)  |  [Instagram](https://www.instagram.com/javierandresgp/)
{:/comment}
