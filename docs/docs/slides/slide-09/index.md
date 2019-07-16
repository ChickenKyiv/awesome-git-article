---
id: slide9
title: Slide9
sidebar_label: Slide1 - What is Git
---

﻿#### Slide 10: This info will help to understand who exactly made that changes in Git history.

#3 step — A good cover
It’s time to make your first modification to your repository. What do you think about creating a cover for it, a kind of welcome text?

## a. A local version of your project

Your first mission is to get a copy of the repository on your computer. To do that, you need to “clone” the repository. On the repository page, you need to get the “HTTPS” address.


![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/b-07-empty-repository.png)

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/04-github-empty-repository.png)

<!-- Repository page with “HTTPS” address -->

Once you had the address of the repositories, you need to use your terminal (through shell commands) to move in the place where you want to put the directory copy (for example you can move in your “Documents” folder). When you are ready, you can enter:

`$ git clone [HTTPS ADDRESS]`

> This command will make a local copy of the repository hosted at the given address.


![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/b-08-done-clone-cli.png)
<!-- Output message of “git clone” command -->

Now, your repository is on your computer. You need to move in it with:

`$ cd [NAME OF REPOSITORY]`

> Note: When you clone, Git will create a repository on your computer. If you want, you can access your project with the computer user interface.
