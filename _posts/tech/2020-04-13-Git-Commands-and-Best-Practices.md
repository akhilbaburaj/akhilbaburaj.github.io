---
layout : "page"
Title : ":/Title"
---

Now that my work requires me to work with version control it has become curcial for me to improve my game with Git. So I decided to document some of the most common things I expect someone to come across and will be needed to work on. 

##Clone a Git Repo
You want the content so you download it to your PC.
`git clone <URL/PATH>`

<br>
##Create a Branch for the Repo
If we own the repo we can directly make commits to the 'master' branch however, it is always good to create a 'feature' branch (a clone of the master to edit and work on). This way the working code remains as the same and you test your commits against a clone/duplicate of it. If you mess up you can always be sure that the master copy is not impacted.
`git checkout -b <branch-name>`

<br>
##Switch between branches
Since every branch is its own copy it may require us to switch between them work with different 'versions' of the same file. 
`git checkout <existing-branch-name>`

Note: That the -b is not present as -b would go ahead and create a branch if not present. 

Altenately, to switch to the previously 'checked' branch you can use '-' to avoid typing the name of the branch.
`git checkout -`

<br>
##Update feature branch to reflect master branch update.
Since we don't always get direct access to master branch, and assuming that the master will be updated while you are working on the feature branch you may require to update your local copies to the most latest one present. This involves few series of steps which uses either 'merge' or 'rebase'. You can read more about them on google and youtube however, these are the steps you can perform 

1) Switching to master branch using checkout
`git checkout master`

2) Fetching latest updates from master
`git fetch -p origin`

3) Syncing updates of remote master(from online Git repo) to local
`git merge origin/master`

4) Switching back to you last used branch(basically your feature branch)
`git checkout -`

5) Syncing update from local master(downloaded copy) to feature branch
`git merge master`

<br>

I will keep adding more commands as I get more time to understand, practice and implement them. So a lot more would eventunally updated here. 