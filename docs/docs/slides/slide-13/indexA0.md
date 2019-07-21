---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


Note that all of the commands, that I will show later are merging into the current branch.

And the current branch will be updated to reflect the merge, but the target branch will be completely unaffected.

Again, this means that `git merge` is often used together
- with `git checkout` for selecting  the current branch,
- then you run a `git merge`
- then you use `git branch -d` for deleting the obsolete target branch.

Or you can keep it for some time if you worried that some of your latest changes can break your current branch and you want to be able quickly rollover your changes.

#### How it works?

Git merge will combine multiple sequences of commits into one unified history.

In the most frequent use cases, `git merge` is used to combine two branches.

**The following examples in these slides will focus on this branch merging pattern.**

In these scenarios, `git merge` takes two commit pointers, usually the branch tips, and will find a common base commit between them.
