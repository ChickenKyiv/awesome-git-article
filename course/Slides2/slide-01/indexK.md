---
id: s2slide13aa
title: Centralized workflow. Managing conflicts
sidebar_label: Centralized workflow. Managing conflicts
---


<!--
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)


#### Managing conflicts -->

The central repository represents the official project, so its commit history should be treated as sacred and immutable.

If a developer’s local commits diverge from the central repository, Git will refuse to push their changes because this would overwrite official commits.


Before the developer can publish their feature, they need to fetch the updated central commits and rebase their changes on top of them.

This is like saying, __I want to add my changes to what everyone else has already done.__ The result is a perfectly linear history, just like in traditional SVN workflows.

If local changes directly conflict with upstream commits, Git will pause the rebasing process and give you a chance to manually resolve the conflicts.

The nice thing about Git is that it uses the same `git status` and `git add` commands for both generating commits and resolving merge conflicts.

This makes it easy for new developers to manage their own merges.

Plus, if they get themselves into trouble, Git makes it very easy to abort the entire rebase and try again (or go find help).
