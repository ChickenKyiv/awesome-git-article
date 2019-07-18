---
id: slide12
title: Branching workflow
sidebar_label: Branching workflow
---


Branching is a great approach to make changes in your code, organized as separated place.

It's like a second room where you keeping your things.
Assume that you want to make some changes, but you are worried that it can break code that you have at your main "place".

At this time you need to implement git branches to your coding workflow.

It will also help you to move between of "states" of your project.

At previous videos we use a command `git push origin master`.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/a-009-git-push-origin-mster.png)



If we convert this command into human language it will be
'move git history of my local modifications into server-side repository at master branch'

So before all of our local changes was stored at your local master branch.

Example: you have a repository that store your website.
And you have 10 pages that looks good and you made them accessible from browser URL.

And you want to add a new page to your website, but you don't want to make it visible while you didn't perfect it.

So you are creating a separated branch, that will have a copy of all your previously create 10 pages.

At this separated branch you can play with that pages, without affecting a **master** branch.

When it's done, you can **merge** your changes(that you commited to the git history of that branch) with code that you have at **master** branch.

When you create a new branch, git tracks of which commit your branch was "branched". So all history of changes that was made before will be saved for each branch at repository separately.

In order to create a new branch from your master branch you need to run

`git checkout -b <branchName>`
`git checkout -b feature1`

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/b-11-git-checkout-b.png)


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/b-11-git-checkout-b.png)


this command combine 2 commands
it creates a new branch and move you inside of it(so you can actually start to make your changes). Those changes will be stored at separated history line from **master** branch.

Please create a separated branch on your local repository, make changes and push them to github repository.

> **Note: you'll need to adjust push command, in order to move your new branch to GitHub.**

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/b-09-git-push-origin.png)


if you want to see list of your branches you can run this command

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/c-carbon4.png)

OR

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/b-010-git-branch-a.png)


If you want to create a new branch but don't switch your branch, you need to run this command

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/c-carbon5.png)

then you can checkout this branch via

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/c-carbon6.png)
