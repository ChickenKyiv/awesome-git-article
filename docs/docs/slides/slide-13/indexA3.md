---
id: slide13aaaa
title: Simple example - Git merge
sidebar_label: Simple example - Git merge
---


Let’s say you’re creating a feature branch off a master for a new feature you are about to implement.

You finish up your work on the feature branch while one of your colleagues is making some changes on the master branch.

Before creating a pull request, you might want to make sure you have the most updated master on your feature branch.

There are a couple of ways to do this: Git merging and Git rebasing.


#### What it is

I think of a merge as saying, “Git, please cram all of my new stuff into the existing stuff.

If you cannot figure out how to cram it all together, ask me to resolve the conflicts.”

#### How it works

Say that Lydia creates an empty repo with a text file.

She adds, “Hello World.” to the file and commits the change as C1.

Lydia then realizes that she should have added more to this file, so she adds, “This is a sentence.” as the second commit (C2).

HelloWorld.text now looks like this:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/A-00-hello.png)


And the commit tree looks like this:

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/0-c1-c2-master-branch.png)


Then, Lydia decides she wants to add even more sentences to HelloWorld.txt, so she creates a branch.

Let’s call the branch feature/more-sentences.

She adds the sentence, “Another sentence.” to the HelloWorld.text file and commits that change as C3.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/1-c1-c2-c3-feature.png)

As this is happening, another developer decides that “This is a sentence” should become “This is a second line.”  

She commits this change to master as C4.




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/2-c1-c2-c3-c4-master.png)


On master, HelloWorld.txt looks like this:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/A-02-hello.png)




On feature/more-sentences, HelloWorld.txt looks like this:

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/A-01-hello.png)



To get the updates on master into her feature branch, Lydia could merge master into feature/more-sentences.

The last commit on master (C4) is not an ancestor of the last commits on the branch feature/more-sentences (C3), meaning that there have been additional commits on master since the feature branch was created.



To resolve the new commits on master with the feature branch, Git does a three-way merge between the tips of the two branches (C4 for master and C3 for feature/more-sentences) and the last common ancestor of those two branches (C2).

The three-way merge creates a new commit with C3 and C4 as its parents.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/3-c1-c2-c3-c4-merge-commit.png)



HelloWorld.txt now looks like this:


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/A-03-hello.png)


#### Tradeoffs

Merging does not re-write Git history. If you want to keep an accurate representation of your repository without losing any history, merging might be the way to go.

However, a historic Git history might mean compromising a clean Git history.  Using merging as the primary means of integration might mean more work-in-progresss commits and merge commits.
