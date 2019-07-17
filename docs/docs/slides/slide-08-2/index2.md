---
id: slide8-3
title: The staging environment
sidebar_label: The staging environment
---

One of the most confusing parts when you're first learning git is the concept of the **staging environment** and how it relates to a commit.

A **commit** is a record of what files you have changed since the last time you made a commit.

Essentially, you make changes to your repo (for example, adding a file or modifying one) and then tell git to put those files into a commit.

Commits make up the essence of your project and allow you to go back to the state of a project at any point.

So, how do you tell git which files to put into a commit?
This is where the staging environment or index come in.

When you make changes to your repo, git notices that a file has changed but won't do anything with it (like adding it in a commit).

To add a file to a commit, you first need to add it to the staging environment.
To do this, you can use the
`git add <filename>` command 

Once you've used the git add command to add all the files you want to the staging environment, you can then tell git to package them into a commit using the git commit command.

> Note: The staging environment, also called **'staging'**, is the new preferred term for this, but you can also see it referred to as the **'index'**.
