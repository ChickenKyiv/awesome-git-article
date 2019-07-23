---
id: slide13aaaaa
title: Git Rebasing
sidebar_label: Git Rebasing
---


#### What it is
Rebasing is similar to asking Git, “Can you just add my new stuff on top of the stuff that has already been done?”

#### How it works
Let’s go back to the previous scenario: Lydia created the branch feature/more-sentences off the master.

In the meantime, another developer had been adding commits to master.

It looked like this:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/c1-c2-c3-feature-rebase.png)


If Lydia wanted to get the updates from master into her current branch without doing a merge commit, she could rebase her current branch on master (Git rebase master).

Rebasing off of master would replay all feature branch commits onto the tip of master.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/c1-c2-c4-c3-rebased.png)


Because the commits on the feature/more-sentences branch are stored in a temporary file and replayed onto master, Lydia will essentially re-write her Git history with new commits.

If there were any conflicts when replaying the commits on to the tip of master, Lydia would get to decide how to resolve them for the new commit being created.

#### Tradeoffs

Rebasing on a public branch can cause confusion.

This method changes history by creating entirely new commits.

If you rebase and push the changes to the remote, the remote might have a different history than someone else’s local copy of the same branch (if they have not yet fetched).

The deviated history could lead to chaos if a developer pushes commits from their local branch to the rebased remote branch.

So if you ever rebase a public branch, it is important to communicate that to the rest of the team.

If rebasing is used carefully, it can give you a lot of flexibility.

You can do things like create a Feature Branch A off of Feature Branch B, and then move the commits on Branch B (but not Branch A) over to master.

For more on rebasing branches off of other branches, you can check out my colleague’s article on Git gardening.

Rebasing also allows you to clean up unnecessary or poorly worded commits.

When rebasing one branch onto another, you can rename commits, combine commits, or entirely delete commits.

This helps you maintain a cleaner Git history and makes it easier to find a commit when performing something like a Git bisect.

My personal favorite is that you no longer have merge commits in your Git history.

When I am looking through Git history to find a specific change, I am concerned with figuring out distinct steps to create the feature, not with understanding the ins and outs of the implementation history.

Though merge commits might show how the features were implemented and merged in, they don’t concisely sum up a chunk of work.
