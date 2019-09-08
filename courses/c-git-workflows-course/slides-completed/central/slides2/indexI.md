---
id: s2slide9
title: Make changes and commit to central repository
sidebar_label: Make changes and commit to central repository
---


<!--
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)
#### Make changes and commit -->

Once the repository is cloned locally, a developer can make changes using the standard Git commit process: edit, stage, and commit.

If you’re not familiar with the staging area, it’s a way to prepare a commit without having to include every change in the working directory.

This lets you create highly focused commits, even if you’ve made a lot of local changes.

```
git status # View the state of the repo
git add <some-file> # Stage a file
git commit # Commit a file</some-file>
```

Remember that since these commands create local commits, Developer can repeat this process as many times as he wants without worrying about what’s going on in the central repository.

This can be very useful for large features that need to be broken down into simpler, more atomic chunks.
