---
id: slide13aa
title: Centralized Workflow Intro
sidebar_label: Centralized Workflow Intro
---



![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/flows/centralized-workflow.png)

- Centralized Workflow
It has central(main) repository and local repositories

The Centralized Workflow is a great Git workflow for teams transitioning from SVN.

Like Subversion, the Centralized Workflow uses a central repository to serve as the single point-of-entry for all changes to the project.

Instead of trunk, the default development branch is called master and all changes are committed into this branch.

**In the trunk-based development model, all developers work on a single branch with open access to it. Often it’s simply the master branch. They commit code to it and run it. It’s super simple.

In some cases, they create short-lived feature branches. Once code on their branch compiles and passess all tests, they merge it straight to master. It ensures that development is truly continuous and prevents developers from creating merge conflicts that are difficult to resolve.**

Centralized workflow doesn’t require any other branches besides master.

Transitioning to a distributed version control system may seem like a daunting task, but you don’t have to change your existing workflow to take advantage of Git.

Your team can develop projects in the exact same way as they do with Subversion.
