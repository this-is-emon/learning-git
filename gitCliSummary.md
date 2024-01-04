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

## 13. Pull from GitHub

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

## 14. Sending pull request to our own project

> **Scenario :** When a new feature needed to be developed, the collaborator create a new branch. Then he develop the feature and send a `pull request` to the Github repo. There is a person(Tech Lead) who is responsible to open any `pull request`, inspect it, send necessary instruction to the collaborator, if any further changes needed. At last if everything is ok he merge the new branch to the main branch. Here we will create a new baranch and send it as a `pull request` to our own project as a _collaborator_. Then we will also act as an _merger manager or Tech lead_, who will Open the `pull request`

#### ➡ As a collaborator :

- Making a new branch and getting into it :

  `git checkout -b <new branch name>`

- Modify necessary codes and add, commit :

  `git add --all`

  `git commit -m "<commit message>"`

- Pushing the new branch into Github

  `git push origin <new branch name>`

#### ➡ As a tech-lead/ourself/particular collaborator :

- Go to GitHub project, in the upper left side of project file listing, you will find all the branch including the new branch :

  ![git brances](https://github.com/this-is-emon/learning-git/blob/main/gitBranch.png?raw=true)

- A message "This branch is 1 commit ahead of main" will be seen. To accept it by the master go to _Contribute --> Open pull request_ button, click it and go to the next page :

  ![Open pull request](https://github.com/this-is-emon/learning-git/blob/main/openPullRequest.png?raw=true)

- In the next window we will see all the code modification with list. For creating a pull request we can make some comments as well. Then click the "Create pull request" button like the image below:

  ![Create pull request](https://github.com/this-is-emon/learning-git/blob/main/createPullRequest.png?raw=true)

- As a pull request is created in GitHub, in the next step a merge manager is responsible to check the **pull request tab** freqently. He then checks the newly created pull requests, accept or discard them.

## 15. Cloning project from gitHub

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
