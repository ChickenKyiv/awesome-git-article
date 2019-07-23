---
id: slide13cc
title: Fast forward and 3-way merge example
sidebar_label: Fast forward and 3-way merge example
---

Our first example demonstrates a fast-forward merge. The code below creates a new branch, adds two commits to it, then integrates it into the mainline with a fast-forward merge.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/git-merge-default.png)


This is a common workflow for short-lived topic branches that are used more as an isolated development than an organizational tool for longer-running features.

Also note that Git should not complain about the `git branch -d`, since new-feature is now accessible from the master branch.

If you require a merge commit during a fast forward merge for record-keeping purposes you can execute git merge with the --no-ff option.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/git-merge-no-fast-forward.png)

This command merges the specified branch into the current branch, but always generates a merge commit (even if it was a fast-forward merge). This is useful for documenting all merges that occur in your repository.

#### 3-way merge
The next example is very similar but requires a 3-way merge because master progresses while the feature is in progress. This is a common scenario for large features or when several developers are working on a project simultaneously.

Start a new feature


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/3-way-merge-workflow.png)


Note that it’s impossible for Git to perform a fast-forward merge, as there is no way to move master up to new-feature without backtracking.

For most workflows, new-feature would be a much larger feature that took a long time to develop, which would be why new commits would appear on master in the meantime. If your feature branch was as small as the one in the above example, you would probably be better off rebasing it onto master and doing a fast-forward merge. This prevents superfluous merge commits from cluttering up the project history.
