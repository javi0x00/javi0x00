# :memo: Notes
## GIT
---
### Resources
- [Git](https://git-scm.com/)
- [Git Reference Manual](https://git-scm.com/docs)
- [Pro Git book](https://git-scm.com/book)
- [Git Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
- [GitHub](https://github.com/)
- [GitLab](https://gitlab.com/)
- [git-flow cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)
- [Multiple Accounts and SSH Keys](https://dbushell.com/2013/01/27/multiple-accounts-and-ssh-keys/)
### Setup
```
$ sudo apt install git-all
$ git --version
$ git config --global user.name "<name>"
$ git config --global user.email <email>
$ git config --global core.editor "<editor --flag>"
$ git config --list
```
### COMMANDS
Branch
```
$ git branch
$ git branch -a
$ git branch -r
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
$ git clone <REMOTE_URL>
$ git status
$ git add
$ git add <filename>
$ git rm <filename>
$ git commit -m <description>
$ git commit --amend -m <description>
$ git push
$ git fetch
$ git merge
$ git pull
```
Fecth
```
$ git fetch
$ git fetch <REMOTE BRANCH>
$ git fetch --all
$ git log --oneline <LOCAL BRANCH>..<REMOTE BRANCH>
$ git merge <ORIGIN BRANCH>
$ git push
```
Adding a local repository to VCH
```
$ git init -b main
$ echo '# repo-name' > README.md
$ git add . && git commit -m "initial commit"
$ git remote add origin <REMOTE_URL>
$ git remote -v
$ git push origin main
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
$ git remote add upstream
$ git show
$ gitk
```
Config file
```
Host github.com
  HostName github.com
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host gitlab.com
  HostName gitlab.com
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host bitbucket.org
  HostName bitbucket.org
  User git
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<KEY>

Host bitbucket-<SECONDARY ACCOUNT>
  HostName bitbucket.org
  User git
  PreferredAuthentications publickey
  IdentitiesOnly yes
  IdentityFile ~/.ssh/<SECONDARY KEY>
```
Bitbucket - App passwords
```
$ git remote set-url origin https://USERNAME:APP_PASSWORD@bitbucket.org/WORKSPACE/REPO.git
```
### Terms and concepts
- Version Control System
- Version Control Hosting
* Repository
  - Clone
  - Fork
---
## Software Developer
Built by [Javi](https://javierandres.dev) :copyright: 2020 - 2023
Found a bug or have an idea? [Contact me](https://javierandres.dev).
