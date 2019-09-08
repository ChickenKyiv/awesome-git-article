---
id: slide13b
title: Git Merge advanced example
sidebar_label: Git Merge advanced example
---

<!-- https://www.atlassian.com/git/tutorials/using-branches/git-merge -->



Ok, so imagine that we have this git history of commits

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/one.png)




You’ve decided that you’re going to work on issue **#53** in whatever issue-tracking system your company uses.

To create a new branch and switch to it at the same time, you can run the **git checkout** command with the **-b** switch:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-00-merge-example.png)
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-01-merge-example.png)


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/two.png)


You work on your website and do some commits. Doing so moves the **feature/iss53** branch forward because you have it checked out (that is, your **HEAD** is pointing to it):


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-02-merge-example.png)





![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/three.png)



Now you get the call that there is an issue with the website, and you need to fix it immediately.

With Git, you don’t have to deploy your fix along with the **feature/iss53** changes you’ve made, and you don’t have to put a lot of effort into reverting those changes before you can work on applying your fix to what is in production.




All you have to do is switch back to your master branch.

However, before you do that, note that if your working directory or staging area has uncommitted changes that conflict with the branch you’re checking out, Git won’t let you switch branches.

It’s best to have a clean working state when you switch branches.

There are ways to get around this (**stashing and commit amending**) but we wouldn't touch it at this course.

For now, let’s assume you’ve committed all your changes, so you can switch back to your master branch:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-03-merge-example.png)


At this point, your project working directory is exactly the way it was before you started working on issue **#53**, and you can concentrate on your hotfix.

This is an important point to remember: when you switch branches, Git resets your working directory to look like it did the last time you committed on that branch.

It adds, removes, and modifies files automatically to make sure your working copy is what the branch looked like on your last commit to it.

Next, you have a hotfix to make. Let’s create a hotfix branch on which to work until it’s completed:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-04-merge-example.png)


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/four.png)




 You can run your tests, make sure the hotfix is what you want, and finally merge the hotfix branch back into your master branch to deploy to production.

 You do this with the git merge command:

 ![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-05-merge-example.png)




You’ll notice the phrase **“fast-forward”** in that merge.

Because the commit C4 pointed to by the branch hotfix you merged in was directly ahead of the commit C2 you’re on, Git simply moves the pointer forward.

To phrase that another way, when you try to merge one commit with a commit that can be reached by following the first commit’s history, Git simplifies things by moving the pointer forward because there is no divergent work to merge  — this is called a **“fast-forward.”**

Your change is now in the snapshot of the commit pointed to by the master branch, and you can deploy the fix.




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/five.png)




After your super-important fix is deployed, you’re ready to switch back to the work you were doing before you were interrupted.

However, first, you’ll delete the hotfix branch, because you no longer need it — the master branch points at the same place. You can delete it with the **-d** option to **git branch**:

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-06-merge-example.png)



Now you can switch back to your work-in-progress branch on issue **#53** and continue working on it.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-07-merge-example.png)


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/six.png)


It’s worth noting here that the work you did in your **hotfix branch** is not contained in the files in your **feature/iss53 branch**.

If you need to pull it in, you can merge your master branch into your **feature/iss53 branch** by running `git merge master`, or you can wait to integrate those changes until you decide to pull the **feature/iss53 branch** back into master later.

#### Basic Merging

Suppose you’ve decided that your issue **#53** work is complete and ready to be merged into your **master branch**.

To do that, you’ll merge your **feature/iss53 branch** into **master**, much like you merged your **hotfix branch** earlier.

All you have to do is check out the branch you wish to merge into and then run the `git merge` command:

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-08-merge-example.png)


This looks a bit different than the **hotfix merge** you did earlier.
In this case, your development history has diverged from some older point.

Because the commit on the branch you’re on isn’t a direct ancestor of the branch you’re merging in, Git has to do some work.

In this case, Git does a simple three-way merge, using the two snapshots pointed to by the branch tips and the common ancestor of the two.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/seven.png)



Instead of just moving the branch pointer forward, Git creates a new snapshot that results from this three-way merge and automatically creates a new commit that points to it.

This is referred to as a merge commit and is special in that it has more than one parent.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/eight.png)


Now that your work is merged in, you have no further need for the **feature/iss53** branch.

You can close the ticket in your ticket-tracking system, and delete the branch:

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/advanced/b-09-merge-example.png)


<!--
https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging -->
