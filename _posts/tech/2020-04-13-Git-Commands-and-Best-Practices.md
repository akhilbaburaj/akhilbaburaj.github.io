---
layout : "page"
Title : ":/Title"
---

Now that my work requires me to work with version control it has become curcial for me to improve my game with Git. So I decided to document some of the most common things I expect someone to come across and will be needed to work on. 

## Clone a Git Repo
As simple as it sounds, you want the content so you clone/download it to your PC. 
```
git clone <URL/PATH>
```
<br>
## Create a Branch for the Repo
If we own the repo we can directly make commits to the 'master' branch however, it is always good to create a 'feature' branch (a clone of the master to edit and work on). This way the working code remains as the same and you test your commits against a clone/duplicate of it. If you mess up you can always be sure that the master copy is not impacted.
```
git checkout -b <branch-name>
```
<br>
## Delete a Branch
To delete a local branch you would have use the git branch command with -d or -D(force delete) option.
```
git branch -d <branch-name>
git branch -D <branch-name>
```
To delete a branch that was pushed(we will discuss about this later) you will use it with the push command.
```
git push origin --delete <branch-name>
```

## Switch between branches
Since every branch is its own copy it may require us to switch between them work with different 'versions' of the same file. 
```
git checkout <existing-branch-name>
```
**Note:** That the -b is not present as -b would go ahead and create a branch if not present. 

Altenately, to switch to the previously 'checked' branch you can use '-' to avoid typing the name of the branch.
```
git checkout -
```

<br>
## Commit on a branch
Commit means you are saving the changes to your version control system. This process allows you create a track of the changes.

Eg. if you save a file with few contents and commit it. Then, next time you make changes version control will be able to report the new changes. However, lets say you start off fresh and add 10 lines to your file. You save the file (ctrl+s) then, delete the file. You cannot expect version control to remember the file you delete. This is because you had not saved it to version control using commit. Similarly if you change the lines from 10 to 100 and save the file again without doing a commit, you cannot roll to the previous version(10 lines file). This is again because there was no commit done. 

The commit process goes through two stage. 
+ Adding file to staging area (basically let it know you want 'x' files to be remembered by version control)
+ Commit the changes.

**Commands:**
```
git add .
git commit -m "The message to remember what you did"
```

<br>
## Amending your commits
Let's say you were creating a file that had someone's name on it. You do your add and commit and you are set. But then, you realise that you spelled it incorrectly. So you make changes and do add and commit again. WHile this is fine, your branch now has 2 commits. Assume you are doing some testing so you have to iterate your changes again and again. This leads to a large number of commits into your branch. 

For such testing purposes and changes you can always use 'amend' along with your commit command. What it does, is rewrites your previous commit (the most recent) with the new commit.
This way the number of commit results to 1 in the previous example.

```
git add .
git commit --amend -m "The message to remember what you did and the changes you just did"
``` 

**Note:** The amend will help you update your local commit history however, if you had performed a git push to the remote branch then, you need to make sure your changes reflect there as well. 

If you do a generic 'git push' the push will fail. This is because the information on your system will not match the one on the remote. Thus you would have to 'force' the change.
```
git push -f origin head
``` 
<br>
## Update feature branch to reflect master branch update
Since we don't always get direct access to master branch, and assuming that the master will be updated while you are working on the feature branch you may require to update your local copies to the most latest one present. This involves few series of steps which uses either 'merge' or 'rebase'. You can read more about them on google and youtube however, these are the steps you can perform 

1) Switching to master branch using checkout
```
git checkout master
```

2) Fetching latest updates from master
```
git fetch -p origin
```

3) Syncing updates of remote master(from online Git repo) to local
```
git merge origin/master
```

4) Switching back to you last used branch(basically your feature branch)
```
git checkout -
```

5) Syncing update from local master(downloaded copy) to feature branch
```
git merge master
```

<br>

I will keep adding more commands as I get more time to understand, practice and implement them. So a lot more would eventunally updated here. 