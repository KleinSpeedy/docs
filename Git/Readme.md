# Git Guide
## Overview

1. [Git Configuration](Readme.md#git-configuration) 
1. [Git Branches](Readme.md#git-branches)
1. [Git Stage](Readme.md#git-stage)
1. [Git Share and Update](Readme.md#git-share-and-update)
1. [Temporary Save](Readme.md#temporary-change-save)

---

### Git Configuration
Set the name that will be attached to your commits and tags.

    git config --global user.name “Your Name”

Set the e-mail address that will be attached to your commits and tags.

    git config --global user.email “you@example.com”

Enable some colorization of Git output.
    
    git config --global color.ui auto
---
### Git Branches
Deletes a local branch.

    git branch -d $branchname

Gets a branch in a **remote**.

    git fetch origin
    git checkout --track origin/$branchname

Creates a new branch **locally** then pushes it.

    git checkout -b $branchname
    git push origin $branchname --set-upstream

Deletes **remote** Branch, works for tags, too!

    git push origin --delete :$branchname

Deletes origin/* branches in your **local** copy. **Doesn’t affect the remote**.

    git remote prune origin

Existing branches are listed. Current branch will be highlighted with an asterisk.

    git branch --list

Go back to previous branch.  
    
    git checkout **

---

### Git Stage

Show modified files in working directory, staged for your next commit.

    git status

Add a file as it looks now to your next commit (stage).

    git add [file]

Unstage a file while retaining the changes in working directory.
    
    git reset [file]

Diff of what is changed but not staged.

    git diff

Diff of what is staged but not yet committed.
    
    git diff --staged

Commit your staged content as a new commit snapshot.
    
    git commit -m “[descriptive message]”

---

### Git Share and Update

Add a git URL as an alias.
    
    git remote add [alias] [url]

Fetch down all the branches from that Git remote.
    
    git fetch [alias]

Merge a remote branch into your current branch to bring it up to date.
    
    git merge [alias]/[branch]

Transmit local branch commits to the remote repository branch.
    
    git push [alias] [branch]

Fetch and merge any commits from the tracking remote branch.
    
    git pull

Rebase your changes on top of the remote master.
    
    git pull --rebase upstream master

---

### Temporary Change Save

Save modified and staged changes.
    
    git stash

List stack-order of stashed file changes.
    
    git stash list

write working from top of stash stack.
    
    git stash pop

Discard the changes from top of stash stack.

    git stash drop
