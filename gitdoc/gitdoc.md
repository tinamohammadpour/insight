# Git & GitHub

---

## What is GitHub?

**[GitHu](https://github.com/)b** is one of the most popular resources for developers to share code and work on projects together. It’s free, easy to use, and has become central in the movement toward open-source software. It makes it easy for developers to share code files and collaborate with fellow developers on open-source projects.

## What is Version control?

The Git version control system, as the name suggests, is a system that records all the modifications made to a file or set of data so that a specific version may be called up later if needed. The system makes sure that all the team members are working on the file’s latest version, and everyone can work simultaneously on the same project.

## What is Git?

Git is a version control system used for tracking changes in computer files. It is used to coordinate the workflow among project team members and track their progress over time. It also benefits both programmers and non-technical users by keeping track of their project files. Git allows multiple users to work together without disrupting each other’s work.

## How does GitHub work?

- **Repository (repo)** — a folder in which all files and their version histories are stored.
- **Branch** — a workspace in which you can make changes that won’t affect the live site.
- **Markdown (.md)**— a way to write in GitHub that converts plain text to GitHub code.
- **Commit Changes** — a saved record of a change made to a file within the repo.
- **Pull Request (PR)** — the way to ask for changes made to a branch to be merged into another branch that also allows for multiple users to see, discuss and review work being done.
- **Merge** — after a pull request is approved, the commit will be pulled in (or merged) from one branch to another and then, deployed on the live site.
- **Issues** — how work is tracked when using git. Issues allow users to report new tasks and content fixes, as well as allows users to track progress on a project board from beginning to end of a specific project.
- F**ederalist** — a platform that securely deploys a website from a GitHub repository in minutes and lets users preview proposed and published changes.

### how to start with GitHub?

After you have created your account it’s time to start. first you need to create a repository(you can also use other user’s repositories.)

Then you should get a copy of the repository on your computer. To do that, you need to “*clone*” the repository(if the repository is for another user and you want it to be just under your control you can fork the repository and then clone it ).

It’s time to add or edit files. it is safer to create a new branch and make the changes there and if they were good then you can merge them with the master branch but you can also make the changes in master branch.

Once you’ve made changes that you want you should “add” , “commit” and then “push” them .Then you need to create a pull request (PR) to inform a repository owner that they should **review the changes** you've made to their code. Then the owner can **approve the pull request** and merge the changes into the main repository.

## Some of the important Git commands:

### 1-Git clone

Git clone is a command for downloading existing source code from a remote repository (like GitHub, for example).

git clone <https://name-of-the-repository-link>

This will make a copy of the project to your local workspace so you can start working with it.

### 2-Git branch

This command will create a branch **locally**

git branch <branch-name>

to view branches:

git branch or git branch —list

to delete any branch:

git branch -d <branch-name>

### 3-Git checkout

We use **git checkout** mostly for switching from one branch to another. We can also use it for checking out files and commits.

git checkout <branch-name>

to create and switch to the branch at the same time:

git checkout -b <branch-name>

### 4-Git status

We can gather information like:

- Whether the current branch is up to date
- Whether there is anything to commit, push or pull
- Whether there are files staged, unstaged or untracked
- Whether there are files created, modified or deleted

git status

### 5-Git add

When we create, modify or delete a file, these changes will happen in our local and won't be included in the next commit. We need to use the git add command to include the changes of a file(s) into our next commit.

to add a single file:

git add <file-name>

to add multiple files at once:

git add .

### 6-Git commit

Once we reach a certain point in development, we want to save our changes. Git commit is like setting a checkpoint in the development process which you can go back to later if needed.

We also need to write a short message to explain what we have developed or changed in the source code.

git commit -m ”commit message”

### 7-Git push

After committing your changes, the next thing you want to do is send your changes to the remote server. Git push uploads your commits to the remote repository.

git push <remote><branch-name>

However, if your branch is newly created, then you also need to upload the branch with the following command:

git push -u origin <branch-name>

or:

git push —set-upstream <remote><branch-name>

### 8-Git pull

The **git pull** command is used to get updates from the remote repo. This command is a combination of **git fetch** and **git merge** which means that, when we use git pull, it gets the updates from remote repository (git fetch) and immediately applies the latest changes in your local (git merge).

git pull <remote>

### 9-Git revert

Sometimes we need to undo the changes that we've made. There are various ways to undo our changes locally or remotely (depends on what we need), but we must carefully use these commands to avoid unwanted deletions.

A safer way that we can undo our commits is by using **git revert**. To see our commit history, first we need to use:

git log —oneline

Then we just need to specify the hash code next to our commit that we would like to undo:

git revert 3321844

The advantage of using **git revert**
 is that it doesn't touch the commit history. This means that you can still see all of the commits in your history, even the reverted ones.

### 10-Git merge

When you've completed development in your branch and everything works fine, the final step is merging the branch with the parent branch (dev or master). This is done with the git merge command.

Git merge basically integrates your feature branch with all of its commits back to the dev (or master) branch. It's important to remember that you first need to be on the specific branch that you want to merge with your feature branch.

for example :

first you should switch to master branch:

git checkout master

before merging you should update your local master branch:

git fetch 

finally

git merge <branch-name>