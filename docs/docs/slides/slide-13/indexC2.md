---
id: slide13ccc
title: Resolving conflict
sidebar_label: Resolving conflict
---


#### Resolving conflict

If the two branches you're trying to merge both changed the same part of the same file, Git won't be able to figure out which version to use.

When such a situation occurs, it stops right before the merge commit so that you can resolve the conflicts manually.

The great part of Git's merging process is that it uses the familiar edit/stage/commit workflow to resolve merge conflicts.

When you encounter a merge conflict, running the `git status` command shows you which files need to be resolved.

For example, if both branches modified the same section of **hello.txt**, you would see something like the following:


```
On branch master
Unmerged paths:
(use "git add/rm ..." as appropriate to mark resolution)
both modified: hello.txt
```


#### How conflicts are presented

When Git encounters a conflict during a merge, It will edit the content of the affected files with visual indicators that mark both sides of the conflicting content.

These visual markers are:
- <<<<<<<
- =======,
- and >>>>>>>

It is helpful to search for a project for these indicators during a merge to find where conflicts need to be resolved.




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/git-merge-conflict.png)


Generally, the content before the **=======** marker is the receiving branch and the part after is the merging branch.

Once you've identified conflicting sections, you can go in and fix up the merge to your liking. When you're ready to finish the merge, all you have to do is run `git add` on the conflicted file(s) to tell Git they're resolved.

Then, you run a normal `git commit` to generate the merge commit.

It’s the same process as committing an ordinary snapshot, which means it’s easy for normal developers to manage their own merges.

Note that merge conflicts will only occur in the event of a 3-way merge.

It’s not possible to have conflicting changes in a fast-forward merge.
