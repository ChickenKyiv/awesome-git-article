---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)

#### Git Workflows: Managing conflicts

Before the developer can publish their feature, they need to fetch the updated central commits and rebase their changes on top of them.

This is like saying, “I want to add my changes to what everyone else has already done.” The result is a perfectly linear history, just like in traditional SVN workflows.

If local changes directly conflict with upstream commits, Git will pause the rebasing process and give you a chance to manually resolve the conflicts.

The nice thing about Git is that it uses the same git status and git add commands for both generating commits and resolving merge conflicts.

This makes it easy for new developers to manage their own merges.

Plus, if they get themselves into trouble, Git makes it very easy to abort the entire rebase and try again (or go find help).
