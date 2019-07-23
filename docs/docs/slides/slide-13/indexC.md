---
id: slide13c
title: Using git merge
sidebar_label: Using git merge
---

<!-- https://www.atlassian.com/git/tutorials/using-branches/git-merge -->

Say we have a new branch feature that is based on the master branch.
We now want to merge this feature branch into master.


Invoking this command will merge the specified branch feature into the current branch, we'll assume master.

Git will determine the merge algorithm automatically (discussed below).


Merge commits are unique against other commits in the fact that they have two parent commits.

When creating a merge commit Git will attempt to "auto magically" merge the separate histories for you.

If Git encounters a piece of data that is changed in both histories it will be unable to automatically combine them. This scenario is a version control conflict and Git will need user intervention to continue.

#### Preparing to merge

Before performing a merge there are a couple of preparation steps to take to ensure the merge goes smoothly.


When learning git, you might find **Head** term.
**HEAD** is a reference to the last commit in the currently check-out branch. You can think of the HEAD as the "current branch".

When you switch branches with **git checkout**, the **HEAD** revision changes to point to the tip of the new branch.


#### Confirm the receiving branch


Execute `git status` to ensure that **HEAD** is pointing to the correct merge-receiving branch.

If needed, execute `git checkout <receiving branch>` to switch to the receiving branch. In our case, we will execute `git checkout master`.

#### Fetch latest remote commits

Make sure the receiving branch and the merging branch are up-to-date with the latest remote changes.

Execute `git fetch` to pull the latest remote commits.

Once the fetch is completed ensure the master branch has the latest updates by executing `git pull`.


#### Merging

Once the previously discussed "preparing to merge" steps have been taken a merge can be initiated by executing
`git merge <branch name>` where **<branch name>** is the name of the branch that will be merged into the receiving branch.


#### Fast Forward Merge

A fast-forward merge can occur when there is a linear path from the current branch tip to the target branch. Instead of “actually” merging the branches, all Git has to do to integrate the histories is move (i.e., **“fast forward”**) the current branch tip up to the target branch tip.

This effectively combines the histories, since all of the commits reachable from the target branch are now available through the current one.
For example, a fast forward merge of some-feature into master would look something like the following:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/fast-forward-merge.jpg)

However, a fast-forward merge is not possible if the branches have diverged.

When there is not a linear path to the target branch, Git has no choice but to combine them via a 3-way merge. 3-way merges use a dedicated commit to tie together the two histories.

The nomenclature comes from the fact that Git uses three commits to generate the merge commit: the two branch tips and their common ancestor.



While you can use either of these merge strategies, many developers like to use fast-forward merges (facilitated through rebasing) for small features or bug fixes, while reserving 3-way merges for the integration of longer-running features.

In the latter case, the resulting merge commit serves as a symbolic joining of the two branches.
