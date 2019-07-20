---
id: slide13a
title: Slide13a
sidebar_label: Slide13 - What is Git
---

<!-- #### Slide 14: Commit your changes and publish them at Github
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/03-git-github-logos.jpeg) -->



#### Git merge

Git merge is a very huge topic inside of Git.
We wouldn't touch everything on this course.
For more details or advanced cases - I will share 3-4 important links in the bottom of this slide.

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

Note that all of the commands, that I will show later are merging into the current branch.

And the current branch will be updated to reflect the merge, but the target branch will be completely unaffected.

Again, this means that `git merge` is often used together
- with `git checkout` for selecting  the current branch,
- then you run a `git merge`
- then you use `git branch -d` for deleting the obsolete target branch.

Or you can keep it for some time if you worried that some of your latest changes can break your current branch and you want to be able quickly rollover your changes.

#### How it works?

Git merge will combine multiple sequences of commits into one unified history.

In the most frequent use cases, `git merge` is used to combine two branches.

**The following examples in these slides will focus on this branch merging pattern.**

In these scenarios, `git merge` takes two commit pointers, usually the branch tips, and will find a common base commit between them.



- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
- https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging
- https://help.github.com/en/articles/about-merge-methods-on-github
- https://help.github.com/en/articles/merging-an-upstream-repository-into-your-fork
- https://help.github.com/en/articles/about-merge-conflicts
