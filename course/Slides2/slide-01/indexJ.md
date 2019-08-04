---
id: s2slide13aa
title: Push new commits to central repository
sidebar_label: Push new commits to central repository
---


<!-- 
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)

#### Push new commits to central repository -->

Once the local repository has new changes committed.
 These change will need to be pushed to share with other developers on the project.

`git push origin master`

This command will push the new committed changes to the central repository.

When pushing changes to the central repository, it is possible that updates from another developer have been previously pushed that contain code which conflict with the intended push updates.

Git will output a message indicating this conflict.

In this situation, git pull will first need to be executed.

This conflict scenario will be expanded on in the following section.
