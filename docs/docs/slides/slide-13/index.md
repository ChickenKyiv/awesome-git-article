---
id: slide13a
title: Git merge Part1
sidebar_label: Git merge Part1
---


Git merge is a very huge topic inside of Git.
We wouldn't touch everything on this course.
For more details or advanced cases - I will share 3-4 important links in the end of this section.

Git Merge joins two or more development histories together.



#### What is Doing?

Incorporates changes from the named commits
(Because sometimes git histories diverged from the current branch) into the current branch.

This command is used by `git pull` to incorporate changes from another repository.

And can be used by hand to merge changes from one branch to another

#### Details

Merging is git's way of putting a forked history back together again.

Like, reverse branching.

The `git merge` command lets you take the independent lines of development, created by `git branch` or `git checkout -b` and integrate them into a single branch.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/c-carbon7.png)
