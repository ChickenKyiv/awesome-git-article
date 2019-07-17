---
id: slide8-2
title:
sidebar_label:
---



Two major processes working with git and version control systems are:
**Check-Out**: make a copy of the repository you wanted to.
Make changes locally, then once you have made your changes, Check-In your changes.

**Check-In**: add your changes back to the repository with an detailed explanation message about change you have made.

Git doing it with more steps, but logic is same
1) Clone the repository
2) Make changes
3) Commit changes with a message about changes
4) Push changes back to the GitHub Repository

Documentation at GitHub are fantastic and I advice you to use it frequently. Part of my information for this course are actually organized information from GitHub.


When you open your folder with repository(we don't have it yet, but in future), you will see a **.git** folder. It's like a history database, that store all changes, that was made at this repository.

There a few, very similar Git CheetShets, I provide a links to them here, you may use one, that is more suitable for you.
You can also print some data and keep it on your table, so it will be more easy to remember commands that we'll learn here

[]
---
The staging environment


One of the most confusing parts when you're first learning git is the concept of the **staging environment** and how it relates to a commit.

A **commit** is a record of what files you have changed since the last time you made a commit.

Essentially, you make changes to your repo (for example, adding a file or modifying one) and then tell git to put those files into a commit.

Commits make up the essence of your project and allow you to go back to the state of a project at any point.

So, how do you tell git which files to put into a commit?
This is where the staging environment or index come in.

When you make changes to your repo, git notices that a file has changed but won't do anything with it (like adding it in a commit).

To add a file to a commit, you first need to add it to the staging environment.
To do this, you can use the
`git add <filename>`

command (see Step 3 below).

Once you've used the git add command to add all the files you want to the staging environment, you can then tell git to package them into a commit using the git commit command.

> Note: The staging environment, also called **'staging'**, is the new preferred term for this, but you can also see it referred to as the **'index'**.
