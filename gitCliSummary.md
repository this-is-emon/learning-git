# 'Git and GitHub at a glance' by Junayed Ahmed

## 01. Git setup

- `git --version`

## 02. Git configure

- `git config --global user.name "Md. Mofijul Islam"`
- `git config --global user.email "mofijul.islam.emon@gmail.com"`

## 03. Git Repository Setup

- `git init`

## 04. Git Status Check

- `git status`

## 05. Taking to staging area

- `git add <file name>`
- `git add .`
- `git add --all`

## 06. Git Final Commit

- `git commit -m "Commit message"`

## 07. To see all the commits

- `git log`
- `git log --oneline`

## 08. To see particular commit

- `git checkout <commit-name>`
- `git checkout <new-branch-name>`

## 09. Git Branch

#### Finding Branch names :

- `git branch`

#### Making a new branch :

- `git branch <branch name>`

#### Getting into a branch

- `git checkout <branch name>`

#### Create and check inot a new brach simultanously:

- `git checkout -b <branch name>`

#### Delete a branch:

- `git branch -D <branch name>`

#### Merging a branch with the main :

- `git merge <branch name>` \* _Make sure you are in the main branch_

## 10. Linking gitHub folder to local

#### If you have no local folder yet :

1. Create a new repository in github
2. Follow the first set of instructions

#### If you have a local folder :

1. Create a new repository in gitHub
2. Follow the second set of instructions

## 11. Git push

1. Adding 'remote origin' (if not added yet)

- `git remote add origin <github project folder link>`

2. Now push after commit

- `git push origin master/main`

2. Now push after commit from a branch

- `git push origin <branch name>`

## 12. SSH key setup

#### 1. Checking if the key is exits:

- `ls -al ~/.ssh`

#### 2.'if not' then to generating the SSH key:

- `ssh-keygen -t rsa -b 4096 -C "<yourGithubEmailAddress@gmail.com>"`

#### 3.To run the 'SSH agent' in background:

- `eval "$(ssh-agent-s)"`

#### 4.Adding the 'private key'(id_rsa) of our newly created SSH key inside the 'SSH agent':

- `ssh-add ~/.ssh/id_rsa`

#### 5.Copying the 'public key'(id_rsa.pub) :

- `cat ~/.ssh/id_rsa.pug | clip`

#### 6.Pasting the 'public key'(id_rsa.pub) in GitHub :

Click on the Githu profile pic -> settings -> SSH and GPG keys -> New SSH key -> paste the key

\* _Now you can push directly_

## 13. Pull request in Own project

1. No changes in code is done in Local but some changes done in GitHub by you or other collaborators. Then you can pull directly :

   - `git pull origin main`

2. Some changes in code is done in Local but not comitted yet. But some changes done in GitHub by you or other collaborators :

   - **Delete the Extra Codes(if the codes are not essential)**
   - `git pull origin main`

3. Some changes in code is done in Local but not comitted yet. But some changes done in GitHub by you or other collaborators :

   - **Commit the new codes (if the codes are essential)**
   - `git pull origin main`

     _if the codes are not pushed after commit, There might be COFLICT and needed to be MERGED._

     > Merging Steps : **1.** After opening the conflict file in vs code, Remove the conflict markers (<<<<<<< HEAD, =======, >>>>>>>) and modify the content to reflect the final desired version **2.** `git add . ` **3.**`git commit -m "commit message"` **4**`git push origin main`

## 14. Cloning project from gitHub

- `git clone <GitHub Repo URL> <Local Directory Name>`

  \* _Local directory name is optional_

## 15. Pull request to others project

1. Fork the project into our github account
2. Clone the project from from our remote to local

\*Update later

## 01. Git setup

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 01. Git setup

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 01. Git setup

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``
