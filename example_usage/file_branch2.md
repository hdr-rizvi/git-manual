# Branch-2 file

this is markdown file in the branch-2 branch
we will have examples for git commands related to branches.

```bash
git branch
```
This command lists all the branches in the repository. The current branch will be highlighted with an asterisk (*).
```bash
git branch <branch-name>
```
This command creates a new branch with the specified name. The new branch will be created based on the current branch you are on.
```bash
git checkout <branch-name>
```
This command switches to the specified branch. After running this command, you will be working on the new branch, and any commits you make will be on that branch until you switch back to another branch.



# Status of the file in branch-2

I already meges branch-2 in main. but may be by mistake i created again branch-2 and so, adding some changes in it. so now i want to check the status of the file in branch-2 and compare it with main branch.

I am now merging branch-2 to main branch and want to check the status of the file in branch-2 and compare it with main branch.

```bash
git checkout main
git merge branch-2
``` 
After merging branch-2 into main, you can check the status of the files in both branches using the following commands:

```bash
git checkout branch-2
git status
```
This will show you the status of the files in branch-2, including any changes that have been made since the last commit.

```bash
git checkout main
git status
```
This will show you the status of the files in the main branch, including any changes that have been made since the last commit. You can compare the status of the files in both branches to see if there are any differences or conflicts that need to be resolved after the merge.



# FAQs

Q: Can i change the branch (say branch-2) after mering it to main branch?
A: Yes, you can switch to the branch (branch-2) after merging it into the main branch. However, any changes you make in branch-2 after the merge will not be reflected in the main branch unless you merge branch-2 again into main. It's important to keep track of the branches and their changes to avoid confusion and ensure that your codebase remains organized.