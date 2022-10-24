# :memo: Notes
## COMMANDS
---
### Angular
Setup
```
$ npm install -g @angular/cli
$ ng --version
$ ng new my-app
$ cd my-app
$ ng serve --open
```
Components
```
$ ng generate component <name>
```
Services
```
$ ng generate service <name>
```
Guards
```
$ ng generate guard <name>
```
### Git
Setup
```
$ sudo apt install git-all
$ git --version
$ git config --global user.name "<name>"
$ git config --global user.email <email>
$ git config --global core.editor "<editor --flag>"
$ git config --list
```
Branch
```
$ git branch
$ git checkout -b <branch name>
$ git checkout <branch name>
$ git push --set-upstream origin <branch name>
$ git branch -d <branch name>
$ git branch -D <branch name>
$ git push origin --delete <branch name>
$ git branch -a
$ git checkout -b <remote branch name> origin/<remote branch name>
```
Tagging
```
$ git tag
$ git tag <tag name>
$ git push --tags
$ git push --delete origin <tag name>
$ git tag -d <tag name>
```
Basic
```
$ git clone <url>
$ git status
$ git pull
$ git add
$ git add <filename>
$ git rm <filename>
$ git commit -m <description>
$ git commit --amend -m <description>
$ git push
$ git merge
```
More
```
$ git checkout
$ git init
$ git rm --cached <filename>
$ git rm --force <filename>
$ git commit
$ git commit -a <description>
$ git commit -am <description>
$ git show
$ git log
$ git log --stat
$ git diff
$ git diff <id> <id>
$ git reset <id>
$ git reset <id> --soft
$ git reset <id> --hard
$ git reset HEAD
$ git fetch
$ git stash
$ git clean
$ git reflog
$ git reset
$ git remote
$ git remote -v
$ gitk
```
---
## Software Developer
[Javier Andrés Garzón Patarroyo](https://javierandresgp.com)
