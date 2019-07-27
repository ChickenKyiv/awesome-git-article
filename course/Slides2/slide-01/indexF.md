

## How it works

Developers start by cloning the central repository.

In their own local copies of the project, they edit files and commit changes as they would with SVN; however, these new commits are stored locally - they’re completely isolated from the central repository.

This lets developers defer synchronizing upstream until they’re at a convenient break point.

To publish changes to the official project, developers "push" their local master branch to the central repository.

This is the equivalent of svn commit, except that it adds all of the local commits that aren’t already in the central master branch.
