# main file

This is markdown main file in the main branch 
we will have examples for git commands.


```bash
git init

git add .
git status
```

Explanation for the above commands:

- `git init`: This command initializes a new Git repository in the current directory. It creates a hidden `.git` folder that contains all the necessary files and data for version control.

- `git add .`: This command stages all the changes in the current directory (and its subdirectories) for the next commit. The `.` indicates that all files should be added to the staging area.

- `git status`: This command shows the current status of the working directory and staging area. It displays which files are staged for the next commit, which files have changes that are not staged, and which files are untracked (not being tracked by Git). It helps you understand what changes are ready to be committed and what changes still need to be staged or ignored.

## check the status of the file using graphical 


## commit the file to the repository

```bash
git commit -m "first commit in main file in main branch"
```

```bash
git log
or
git log --all --graph --decorate 
or
git log --oneline --graph --decorate --all
```

difference between git status and git log is that git status shows the current state of the working directory and staging area, while git log shows the commit history of the repository.



# git branch

A branch in Git is a separate line of development that allows you to work on different features or bug fixes without affecting the main codebase. It is essentially a pointer to a specific commit in the repository's history. 

When you create a new branch, it starts from the current commit, and you can make changes and commits on that branch without affecting the main branch (usually called "main" or "master"). This allows for parallel development and makes it easier to manage different features or bug fixes. 
To create a new branch, you can use the following command:

```bash
git branch <branch-name>
```

To switch to a different branch, you can use the following command:

```bash
git checkout <branch-name>
```



# git merge

Git merge is a command used to combine the changes from one branch into another branch. It allows you to integrate the changes made in a feature branch back into the main branch (or any other branch). 

When you merge a branch, Git takes the commits from the source branch and applies them to the target branch. If there are no conflicts between the branches, Git will automatically merge the changes. However, if there are conflicting changes (i.e., changes made to the same lines of code in both branches), Git will prompt you to resolve the conflicts manually.
To merge a branch, you can use the following command:

```bash
git merge <source-branch>
```
