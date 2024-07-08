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
- [tj/git-extras](https://github.com/tj/git-extras)
### Terms and concepts
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
* Version Control System (local)
  - Installation
  - Configuration
* Version Control Hosting (remote)
  - Sign up
  - Clone
  - Remote
  - Tokens
  - Fetch
  - Merge
  - Pull
  - Push
  - Fork
  - Rebase
* Repository
  - Local
  - Remote
  - Clone
  - Fork
  - Pull request
  - Issues
* Repository
  - Initialize
  - Delete
* Repository
  * Areas
    - Working directory
    - Preparation area or staging area
    * .git directory or core or repository
      - Metadata
      - All versions
  * Status (A specific version of the file)
    - Modified
    - Staged or prepared
    - Committed or confirmed
- CLI
- Tracking
- Status
- Add
- Unstage
* Commit
  - Timeline, status record
  - SHA ID or Secure Hash Algorithm ID
  - User
  - Email
  - Date
  - Custom message
- History
- Change last commit message
- Undo last commit
* Branch
  - Independent line of development
- Merge
- Conflicts
### Setup
```
$ sudo apt install git-all
$ sudo apt-get install install-info
$ git --version
$ git config --global init.defaultBranch <name>
$ git config --global user.name "<name>"
$ git config --global user.email <email>
$ git config --global core.editor "<editor --flag>"
$ git config --global core.editor "<code --wait>"
$ git config --global color.ui <true/false/always/auto>
$ git config --global color.branch <true/false/always>
$ git config --global color.diff <true/false/always>
$ git config --global color.interactive <true/false/always>
$ git config --global color.status <true/false/always>
$ git config --list
```
### COMMANDS
Branch
```
$ git branch
$ git branch -a
$ git branch -r
$ git branch <name>
$ git checkout -b <branch name>
$ git checkout <branch name>
$ git branch -m <current name> <new name>
$ git branch -m <new name>
$ git push --set-upstream origin <branch name>
$ git branch -d <branch name>
$ git branch -D <branch name>
$ git push origin --delete <branch name>
$ git branch -a
$ git checkout -b <new local branch name> origin/<remote branch name>
$ git checkout -t origin/<remote branch name>
```
History
```
$ git log
$ git log --oneline
$ git log --p
$ git log --author="<user name>"
$ git log --since=1.month.ago --until=1.day.ago
$ git log --pretty="format:%h %s"
$ git restore --source <id>
```
Tagging
```
$ git tag
$ git tag <tag name>
$ git describe --tag
$ git push --tag
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
$ git commit <see text editor>
$ git commit --amend -m <description>
$ git commit --amend <see text editor>
$ git reset --soft HEAD~1
$ git reset --hard HEAD~1
$ git push
$ git fetch
$ git merge
$ git merge --continue
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
Remote
```
$ git remote
$ git remote -v
$ git pull
$ git fetch
$ git checkout origin/main
$ git push
```
Rebase
```
$ git rebase -i <commit> or git rebase --interactive <commit>
$ git push or git push --force-with-lease
```
Create a new repository on the command line
```
$ echo '# repo-name' > README.md
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin <REMOTE_URL>
$ git push -u origin main
```
Push an existing repository from the command line
```
$ git remote add origin <REMOTE_URL>
$ git branch -M main
$ git push -u origin main
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
Git Extras
```
$ sudo apt-get install git-extras
$ git extras --version
$ git extras --help
$ git extras update
$ git info
$ git count
$ git count --all
$ git effort
$ git effort --above 15
$ git effort -- --since='last month'
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
### Git Branching
1. A **develop** branch is created from **main**
2. A *release* branch is created from **develop** `release/vX.X.X`
3. *feature* branches are created from **develop** `feature/myfeature`
4. When a *feature* is complete it is merged into the **develop** branch
5. When the *release* branch is done it is merged into **develop** and **main**
6. If an issue in **main** is detected a *hotfix* branch is created from **main** `hotfix/myfix`
7. Once the *hotfix* is complete it is merged to both **develop** and **main**
---
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
