https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
































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
