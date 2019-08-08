https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow



---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



#### Git Feature Branch Workflow

The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated branch instead of the master branch.

This encapsulation makes it easy for multiple developers to work on a particular feature without disturbing the main codebase.

It also means the master branch will never contain broken code, which is a huge advantage for continuous integration environments.



---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


Encapsulating feature development also makes it possible to leverage pull requests, which are a way to initiate discussions around a branch.

They give other developers the opportunity to sign off on a feature before it gets integrated into the official project.

Or, if you get stuck in the middle of a feature, you can open a pull request asking for suggestions from your colleagues.

The point is, pull requests make it incredibly easy for your team to comment on each other’s work.





The Git Feature Branch Workflow is a composable workflow that can be leveraged by other high-level Git workflows.

We discussed that other Git workflows at slides before.













---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


Git Feature Branch Workflow is branching model focused, meaning that it is a guiding framework for managing and creating branches.

Other workflows are more repo focused.

The Git Feature Branch Workflow can be incorporated into other workflows.

The Gitflow, and Git Forking Workflows traditionally use a Git Feature Branch Workflow in regards to their branching models.






---
id: slide13aa
title: How it works
sidebar_label: How it works
---


The Feature Branch Workflow assumes a central repository, and master represents the official project history.

Instead of committing directly on their local master branch, developers create a new branch every time they start work on a new feature.

Feature branches should have descriptive names, like **animated-menu-items** or **issue-#1061**.

The idea is to give a clear, highly-focused purpose to each branch.

Git makes no technical distinction between the master branch and feature branches, so developers can edit, stage, and commit changes to a feature branch.






---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


In addition, feature branches can (and should) be pushed to the central repository.

This makes it possible to share a feature with other developers without touching any official code.

Since master is the only “special” branch, storing several feature branches on the central repository doesn’t pose any problems.

Of course, this is also a convenient way to back up everybody’s local commits.

The following is a walk-through of the life-cycle of a feature branch.






---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


#### Start with the master branch

All feature branches are created off the latest code state of a project.

This guide assumes this is maintained and updated in the master branch.

```
git checkout master
git fetch origin
git reset --hard origin/master
```

This switches the repo to the master branch, pulls the latest commits and resets the repo's local copy of master to match the latest version.

Then you creating a new branch for working on separated issue/feature.




---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



#### Create a new-branch

Use a separate branch for each feature or issue you work on.
 After creating a branch, check it out locally so that any changes you make will be on that branch.

`git checkout -b new-feature`

This checks out a branch called new-feature based on master, and the **-b** flag tells Git to create the branch if it doesn’t already exist.



#### Update, add, commit, and push changes

On this branch, edit, stage, and commit changes in the usual fashion, building up the feature with as many commits as necessary.

Work on the feature and make commits like you would any time you use Git.

When ready, push your commits, updating the feature branch on GitHub.

```
git status
git add <some-file>
git commit
```






---
id: slide13aa
title: Push feature branch to remote
sidebar_label: Push feature branch to remote
---





It’s a good idea to push the feature branch up to the central repository.

This serves as a convenient backup, when collaborating with other developers, this would give them access to view commits to the new branch.

`git push -u origin new-feature`

This command pushes new-feature to the central repository (origin), and the **-u** flag adds it as a remote tracking branch.

After setting up the tracking branch, `git push` can be invoked without any parameters to automatically push the new-feature branch to the central repository.

To get feedback on the new feature branch, create a pull request in a repository management solution like GitHub repositories.

From there, you can add reviewers and make sure everything is good to go before merging.









---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



#### Resolve feedback

Now teammates comment and approve the pushed commits.

Resolve their comments locally, commit, and push the suggested changes to GitHub.

Your updates appear in the pull request.



#### Merge your pull request

Before you merge, you may have to resolve merge conflicts if others have made changes to the repo.

When your pull request is approved and conflict-free, you can add your code to the master branch.

Merge from the pull request in GitHub Pull Requests tab at your repository.




#### Pull requests

Aside from isolating feature development, branches make it possible to discuss changes via pull requests.

Once someone completes a feature, they don’t immediately merge it into master.

Instead, they push the feature branch to the central server and file a pull request asking to merge their additions into master.

This gives other developers an opportunity to review the changes before they become a part of the main codebase.







---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



Code review is a major benefit of pull requests, but they’re actually designed to be a generic way to talk about code.

 You can think of pull requests as a discussion dedicated to a particular branch.

 This means that they can also be used much earlier in the development process.
 For example, if a developer needs help with a particular feature, all they have to do is file a pull request. Interested parties will be notified automatically, and they’ll be able to see the question right next to the relevant commits.



Once a pull request is accepted, the actual act of publishing a feature is much the same as in the Centralized Workflow. First, you need to make sure your local master is synchronized with the upstream master. Then, you merge the feature branch into master and push the updated master back to the central repository.





Pull requests can be facilitated by product repository management solutions like GitHub Pull Requests.
