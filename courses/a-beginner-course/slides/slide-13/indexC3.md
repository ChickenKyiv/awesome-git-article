---
id: slide13cccc
title: Git merge summary and git merge conflict practice
sidebar_label:  Git merge summary and git merge conflict practice
---


#### update & merge
- to update your local repository with changes from remote repository, execute `git fetch`
- to update your local repository to the newest commit, execute
`git pull` in your working directory to fetch and merge remote changes.

- to merge another branch into your active branch (e.g. master), use
`git merge <branch>` in both cases git tries to auto-merge changes.

 Unfortunately, this is not always possible and results in conflicts.

 You are responsible to merge those conflicts manually by editing the files shown by git.

- After changing, you need to mark them as merged with
`git add <filename>`

- before merging changes, you can also preview them by using
`git diff <source_branch> <target_branch>`

#### Summary.
It was a basic overview of git merge command.
Merging is an essential process when working with Git.
We discussed the internal mechanics behind a merge and the differences between a fast forward merge and a three way, true merge.
Some key take-aways are:


- Git merging combines sequences of commits into one unified history of commits.
- There are two main ways Git will merge: Fast Forward and Three way
- Git can automatically merge commits unless there are changes that conflict in both commit sequences.

---

## Practice

Create a file at master branch.
Add one line into it, so git will be able to commit this file into git history.
Make a featured branch. Paste, save, commit one of the examples below at this branch.
Other example should be added to git history into another branch.

paste
```
1
- 11
- 12
- 13
 - 131
 - 132
- 14

2
- 21
- 22
- 23
- 24
- 25
```


paste
```
100
-101
-102
- 103
- 104
- 105
- 106
```


So you, put different content at the same file at the same lines for generating an issue
#### first way to solve this

rename a file at one of your branches - make a commit and issue will gone

#### second way
or copy your code, and place it after your changes from other branch

#### third way
If you need to keep only one version of changes, you may pick it and delete other side of conflict and commit changes into your repository

first two options it's maybe not the best way to solve coding conflicts, but it will give you an idea about how git tracking changes inside files


At next slide we'll have an advanced example that you might have at your commercial project.