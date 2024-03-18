# _'Git and GitHub at a glance' by Junayed Ahmed_

# Topic 01 : Start

- To be updated....

# Topic 02 : Git

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

# Topic 03 : GitHub

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

> **Scenario :** When a new feature needed to be developed, the collaborator create a new branch. Then he develop the feature and send a `pull request` to the Github repo. There is a person(Tech Lead) who is responsible to open any `pull request`, inspect it, send necessary instruction to the collaborator, if any further changes needed. At last if everything is ok he merge the new branch to the main branch. Here we will create a new branch and send it as a `pull request` to our own project as a _collaborator_. Then we will also act as an _merger manager or Tech lead_, who will Open the `pull request`

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

  ![git brances](https://github.com/this-is-emon/learning-git/blob/main/images/gitBranch.png?raw=true)

- A message "This branch is 1 commit ahead of main" will be seen. To accept it by the master go to _Contribute --> Open pull request_ button, click it and go to the next page :

  ![Open pull request](https://github.com/this-is-emon/learning-git/blob/main/images/openPullRequest.png?raw=true)

- In the next window we will see all the code modification with list. For creating a pull request we can make some comments as well. Then click the "Create pull request" button like the image below:

  ![Create pull request](https://github.com/this-is-emon/learning-git/blob/main/images/createPullRequest.png?raw=true)

- As a pull request is created in GitHub, in the next step a merge manager is responsible to check the **pull request tab** freqently. He then checks the newly created pull requests, accept or discard them.

## 15. Cloning project from gitHub

- `git clone <GitHub Repo URL> <Local Directory Name>`

  \* _Local directory name is optional_

## 15. Pull request to others project

1. Fork the project into our github account
2. Clone the project from from our remote to local
3. Make necessary changes in the code
4. Add, Commit, push
5. Send pull request to the project.

# Topic 04 : Contribution in Projects

## 00. Searching Project

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 01. Forking Project

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 02. Contribute

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 03. Not done yet

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

## 04. Celebrate

- `git --version`
- ``
- ``
- ``
- ``
- ``
- ``

# Topic 05 : Explore Git

## 00. Git Restore

> **Scenario :** git restore কমান্ডটি মূলত আপনাকে কোন ফাইল বা
> ডিরেক্টরীর আগের অবস্থায়(শেষ commit এর অবস্থায়) ফিরিয়ে নিতে
> সাহায্য কের। এটা মূলত `লোকাল uncommitted` চেঞ্জেসগুলোেক
> undo (পূর্বের অবস্থায় ফিরিয়ে নিতে সাহায্য) করে, অথবা `git add দিয়ে 
Stagging` এ অ্যাড করা চেঞ্জেসগুলোেকে undo (পূর্বের অবস্থায় ফিরিয়ে নিতে সাহায্য) করতে ব্যবহার করা
> যায়।

- To restore changes of a local uncommited file

  `git restore <file>`

- To restore changes of a local uncommited directory

  `git restore <directory>`

- To restore all uncommited changes inside the repo

  `git restore .`

- For stagged uncommited changes we just need to add `--staged` keyword with the above instructions.

  `git restore --staged <file> `

  `git restore --staged <directory> `

  `git restore --staged .`

## 01. Git Stash

> **Scenario :** গিট স্ট্যাশ কমান্ডের সাহায্যে আপনি আপনার
> করা অর্ধেক কাজটা(From one branch) একপাশে ফেলে রেখে অন্যান্য কাজ(to another branch ) করতে
> পারবেন । তারপর আপনার সেই অন্য কাজ শেষ হলে আবার সেই পুরোনো(uncommitted)
> কাজগুলো খুব সহেজই আরেকটা কমান্ড দিয়ে ফিরে পেয়ে যাবেন।

- The command below omit all the **uncommitted** changes and store them in the **Stash Memory**. Eventually it will take you back to your last **commit state** :

  `git stash`

- The commad below will _'cut'_ all the stashed(uncommitted) changes from **Stash Memory** and _'paste'_ them in the local.

  `git stash pop`

  \*\* মনে রাখবেন এই pop কমান্ডটি আপনার সর্বশেষ স্ট্যাশ করা
  কাজগুলোই ব্যাক করেব এবং স্ট্যাশ লিস্ট থেকেও এটাকে ক্লিয়ার
  করে দিবে। তবে স্ট্যাশে যেহেতু আপনি একাধিক চেঞ্জেস রাখতে পারবেন, সেক্ষেত্রে pop দিতে থাকলে সবার শেষে অ্যাড করা চেঞ্জেসগুলো প্রথম হিসেবে পর্যায়ক্রমে আসতে থাকবে ।

- If you want to _'copy'_ all the stashed(uncommitted) changes from **Stash Stack Memory** and _'paste'_ them in the local. As a result your changes will remain in the Stash as well as in the local.

  `git stash apply`

- To see all the changes in the stash in a **list**.

  `git stash list`

- To **Pop** or **apply** any particular item number of stash _"stash@{n}"_

  `git stash pop stash@{3}`

  `git stash apply stash@{1}`

- To clear the **stash list**

  `git stash clear`

- To remove a specific item from stash

  `git stash drop stash@{n}`

- If you added a new **file** or **directory** after your last commit and want to stash it, then :

  `git stash -u`

## 02. Git Reset

- `git restore` or `git stash` are used for undo **uncomitted** changes. But to undo **comitted** changes, we use `git reset`.
- To undo all changes that you made after an spcific commits :

  `git reset <commit_id>`

  \*\*এক্ষেত্রে আপনার উক্ত কমিটের পরবর্তী যে যে চেঞ্জেসগুলো ছিলো
  সেগুলো আনকমিটেড অবস্থায় চলে যাবে । তবে আপনি যদি চান যে
  উক্ত কমিটের পরবর্তী চেঞ্জেসগুলো একেবারেই চলে যাক তাহলে
  উপরোক্ত কমান্ডটি এভাবে দিতে হবে :

  `git reset <commit_id> --hard`

- If you have **push** the 'commited codes' then it is not recommended to use the 'Git Reset' option. Because the other contributors might become confused on the missing commited code. On that scenario `git revert` command is more useful.

## 03. Git Revert

- You have commit and pushed codes into the remote repo. But now want to remove some codes that pushed after a particular commit.

  `git revert <commit_id>`

  \*\*কমান্ডটি দেওয়ার পর কমিট ম্যাসেজ লিখার জন্য একটা প্রম্পট
  আসবে, যেখানে আপনি চাইলে কাস্টম ম্যাসেজ দিতে পারেন অথবা
  ডিফল্ট রেখেও **:wq (write & quite)** লিখে বেরিয়ে আসতে
  পারেন ।

- The main difference between `git reset` and `git revert` is that, `git revert` keep a trace of the **removed pushed codes** by making a 'new commit'. As the result other contributor can clearly see changes in the remote repo through this 'new commit'.

## 04. Git Rebase

> **Scenario :** সাহির প্রোজেক্টে নতুন একটি ফিচার নিয়ে কাজ করবে, তাই সে
> main ব্রাঞ্চ থেকে চেকআউট করে নতুন ফিচার ডেভলপেমন্ট এর
> জন্য আরেকটা ব্রাঞ্চ feature ক্রিয়েট করলো। এখন সাহির তার
> নতুন feature ব্রাঞ্চে নতুন ফিচার নিয়ে কাজ করছে, অল্প অল্প
> করে কাজ করে সে তার কাজগুলোেক কমিটও করে যাচ্ছে। এরমধ্যে
> ওয়াফি আবার মেইন প্রোডাকশন main ব্রাঞ্চে আরো নতুন কি ছু
> কাজ যুক্ত করেছে । এখন এদিকে সাহিরও চাচ্ছে তার feature
> ব্রাঞ্চেও যাতে main এর সেই নতুন কাজগুলো পাওয়া যায়। সেজন্য
> সে কি করতে পারে?

1. `git merge main` -- by being in the 'feature' branch

   \*\*With the above command from **feature** branch the changes in the main branch creates a new commit with the new changes. So in the feature branch Sahir can see the changes along with the changes he made in the feature branch by `git log`. But commits both in 'main' and 'feature' branch makes the code messy.

2. `git rebase` -- by being in the 'feature' branch

   \*\*With the above command from **feature** branch,

   ➡ First, Git finds a _'common commit'_ where codes of both _'main'_ and _'feature'_ are same.

   ➡ Then all the new commits of the 'feature brach' is _'kept aside'_.

   ➡ In the feature branch, _"all the new commits of the 'main' branch"_ is attached after the _'common commit'_ .

   ➡ In the feature branch, _"all the 'kept aside' new commits of the 'feature' branch"_ are added with the _updated code base_ of the feature branch.

- `git rebase` make the commits looks cleaner but reduce tracibility of the commits.

## 05. Git Squashing

> **Scenario :** ওয়াফি প্রোজেক্টে নতুন একটি ফিচার নিয়ে কাজ করার চিন্তাভাবনা
> করে , তাই সে তাদের প্রোডাকশন main ব্রাঞ্চ থেকে চেকআউট
> করে নতুন আরেকটি ব্রাঞ্চ new-feature তৈরি করলো। এখন
> সে এই নতুন ব্রাঞ্চে তার ডেভলপেমন্ট শুরু করলো। সে
> ডেভলপেমন্ট শেষ করার পর সেটা সাহির এর সাথে শেয়ার করার
> সিদ্ধান্ত নিলো যে , তারা এটা তােদর মেইন প্রোডাকশন main ব্রাঞ্চে মার্জ
> করবে। এখন তারা খেয়াল করলো তার এই new-feature ব্রাঞ্চে
> অনেকগুলো কমিট তৈরি করা হেয়েছ ডেভলপেমন্ট এর সময়, অথচ
> ফিচারটা খুবই ছোটো একটা ফিচার। কমিট হিস্টোরিতে এতগুলো
> ছোটো ছোটো কমিট থাকেল সেটা একটু আনক্লিন দেখা যেতে পারে।
> এই অবস্থায় বেটার হয় যিদ new-feature ব্রাঞ্চের সব আপেডট
> জাস্ট একটা কমিটের মাধ্যেমে মেইন main ব্রাঞ্চে আনা যায়। হ্যা!
> ঠিক সেইম কাজটাই সম্ভব গিট স্কোয়ািশং এর সাহায্যে।

- `git merge new-feature --squash` -- at _'main'_ branch

  \*\* Here you are suashing all the commits of _'new-feature'_ into the _'main'_ branch.

- Remember all the changes of the _'new-feature'_ branch will be staged into the _'main'_ branch after the above command. So, make another commit to add all the staged changes

  `git commit -m “new feature introduced”`

## 06. Differnce between `git rebase` & `git squash`

- Follow the video below to see the differences:

  [Git MERGE vs REBASE](https://www.youtube.com/watch?v=0chZFIZLR_0&t=199s)

- The image below summarises pros and cons among _Git Merge_, _Git Rebase_, _Git Squash_.

  ![Git-merge,rebase,squash](https://github.com/this-is-emon/learning-git/blob/main/images/mergeRebseSquash.png?raw=true)

# **Topic 06** : _"Others"_

## 00. Will not use Github

- You can use alternate 'Hosting provider', but basic of git functionality remain same. Links of hosting providers :

1. [Bitbucket](https://bitbucket.org/)
2. [GitLab](https://about.gitlab.com/)

## 01. Do not want to use SSH in Github

> **Scenario :** For some limited access to your git repo, like to `only read` codes of some `particular repo` from a `specified machine`

- Go to `Github Settings` --> `Developer settings`

  ![GitHub settings](https://github.com/this-is-emon/learning-git/blob/main/images/gitHubSettings.png?raw=true)
  ![Developer Settings](https://github.com/this-is-emon/learning-git/blob/main/images/developerSettings.png?raw=true)

- Then go to `Personal access tokens` --> `Fine-grained tokens`. Fine grained tokens provides more control for accessibilty.

  ![Personal access tokens](https://github.com/this-is-emon/learning-git/blob/main/images/personalAccessTokens.png?raw=true)

- Click on `Generate new tokens` button

  ![Generate new tokens](https://github.com/this-is-emon/learning-git/blob/main/images/generateNewTokens.png?raw=true)

- There will be many options after that, try to choose the option carfully. `Resource owner` describes user name or organaization name

  ![Token Description](https://github.com/this-is-emon/learning-git/blob/main/images/tokenDescription.png?raw=true)

- Scope of `Repository access` : আমরা এখােন Repository permissions এ জাস্ট উপরের
  সিলক্টকৃত রিপোতে কন্টেন্টস(Contents) Read and write
  অ্যাক্সেস দিয়েছি (এটা সেট করেল আেরকটা ফিল্ড(Metadata)
  অটোই Read-only অ্যাক্সেস পেেয় যায়, যেহতুএটাও ম্যান্ডাটির)।
  আর এই পারিমশনটাই আমােদরেক উক্ত রিপো থেকে পুল পুশ করেত পারমিশন দিবে।

  ![Permissions](https://github.com/this-is-emon/learning-git/blob/main/images/permissionScope.png?raw=true)

- Click on `Generate token` button in the Overview section :

  ![Overview](https://github.com/this-is-emon/learning-git/blob/main/images/overViewScope.png?raw=true)

- Save the `Genarated token` somewhere for future use, as Git provide this token for only one time.

  ![Token](https://github.com/this-is-emon/learning-git/blob/main/images/generatedToken.png?raw=true)

- Token is ready to use. But one thing to remember: ক্লোন করার সময় এখান থেকে SSH সিলেক্ট না কের HTTPS সিলেক্ট করে ক্লোন করেত হেব যেহেতু আমরা আর SSH ব্যবহার করছি না।

  ![HTTPS Selection](https://github.com/this-is-emon/learning-git/blob/main/images/httpsSelection.png?raw=true)

## 02. Github for students

- Click the link below to get the service for free! :

  [GitHub Student Pack](https://education.github.com/pack)

## 03. Something more

- Adding someone as a _Contributor_ in a Project :
  `Settings` -> ` Collaborators` -> Give `userName` of the collaborator
- Adding `README.md` in a project
- Ignoring a file or folder using `.gitignore`
