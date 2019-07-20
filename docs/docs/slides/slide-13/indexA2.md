Let’s say you’re creating a feature branch off a master for a new feature you are about to implement. You finish up your work on the feature branch while one of your colleagues is making some changes on the master branch. Before creating a pull request, you might want to make sure you have the most updated master on your feature branch. There are a couple of ways to do this: Git merging and Git rebasing.

Git Merging
What it is
I think of a merge as saying, “Git, please cram all of my new stuff into the existing stuff. If you cannot figure out how to cram it all together, ask me to resolve the conflicts.”

How it works
Say that Lydia creates an empty repo with a text file. She adds, “Hello World.” to the file and commits the change as C1. Lydia then realizes that she should have added more to this file, so she adds, “This is a sentence.” as the second commit (C2).
