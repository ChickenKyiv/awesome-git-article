#### update & merge
to update your local repository to the newest commit, execute
`git pull`
in your working directory to fetch and merge remote changes.
to merge another branch into your active branch (e.g. master), use
`git merge <branch>``
in both cases git tries to auto-merge changes. Unfortunately, this is not always possible and results in conflicts. You are responsible to merge those conflicts manually by editing the files shown by git. After changing, you need to mark them as merged with
`git add <filename>`
before merging changes, you can also preview them by using
`git diff <source_branch> <target_branch>`
