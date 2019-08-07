---
id: sf2aa
title: Feature Branch Workflow example
sidebar_label: Feature Branch Workflow example
---





The following is an example of the type of scenario in which a feature branching workflow is used.

The scenario is that of a team doing code review around on a new feature pull request.

This is one example of the many purposes this model can be used for.


#### Mary begins a new feature


Before she starts developing a feature, Mary needs an isolated branch to work on.
She can request a new branch with the following command:

`git checkout -b marys-feature master`

This checks out a branch called `marys-feature` based on master, and the **-b** flag tells Git to create the branch if it doesn’t already exist.

On this branch, Mary edits, stages, and commits changes in the usual fashion, building up her feature with as many commits as necessary:

```
git status
git add <some-file>
git commit
```



#### Mary goes to lunch
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/flows/feature/1-Mary-goes-on-launch.png)


Mary adds a few commits to her feature over the course of the morning. Before she leaves for lunch, it’s a good idea to push her feature branch up to the central repository. This serves as a convenient backup, but if Mary was collaborating with other developers, this would also give them access to her initial commits.

`git push -u origin marys-feature`

This command pushes marys-feature to the central repository (origin), and the -u flag adds it as a remote tracking branch.
After setting up the tracking branch, Mary can call git push without any parameters to push her feature.




#### Mary finishes her feature

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/flows/feature/2-Mary-done.png)

When Mary gets back from lunch, she completes her feature. Before merging it into master, she needs to file a pull request letting the rest of the team know she's done. But first, she should make sure the central repository has her most recent commits:

`git push`


Then, she files the pull request in her Git GUI asking to merge `marys-feature` into `master`, and team members will be notified automatically.
The great thing about pull requests is that they show comments right next to their related commits, so it's easy to ask questions about specific changesets.



---


#### John receives the pull request

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/flows/feature/3-Mary-PR.png)



John gets the pull request and takes a look at `marys-feature`. He decides he wants to make a few changes before integrating it into the official project, and he and Mary have some back-and-forth via the pull request.





---

#### Mary makes the changes


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/flows/feature/4-Mary.png)


To make the changes, Mary uses the exact same process as she did to create the first iteration of her feature.
She edits, stages, commits, and pushes updates to the central repository.

All her activity shows up in the pull request, and John can still make comments along the way.





If he wanted, John could pull `marys-feature` into his local repository and work on it on his own. Any commits he added would also show up in the pull request.

---

#### Mary publishes her feature
<!-- Feature Branch Workflow: Merging a feature branch -->

Once John is ready to accept the pull request, someone needs to merge the feature into the stable project (this can be done by either John or Mary):

```
git checkout master
git pull
git pull origin marys-feature
git push
```

This process often results in a merge commit. Some developers like this because it’s like a symbolic joining of the feature with the rest of the code base. But, if you’re partial to a linear history, it’s possible to rebase the feature onto the tip of master before executing the merge, resulting in a fast-forward merge.


Some GUI’s will automate the pull request acceptance process by running all of these commands just by clicking an “Accept” button.

If yours doesn’t, it should at least be able to automatically close the pull request when the feature branch gets merged into master.




---



Meanwhile, John is doing the exact same thing

While Mary and John are working on `marys-feature` and discussing it in her pull request, John is doing the exact same thing with his own feature branch.

By isolating features into separate branches, everybody can work independently, yet it’s still trivial to share changes with other developers when necessary.
