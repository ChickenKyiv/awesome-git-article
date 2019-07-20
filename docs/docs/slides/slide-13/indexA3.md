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

----


generate a merge conflict
1 branch

paste
```
1
- 11
- 12
- 13
 - 131
 - 132
- 14

2
- 21
- 22
- 23
- 24
- 25
```

paste
```
100
-101
-102
- 103
- 104
- 105
- 106
```

same file for generating an issue
first version to solve this

rename a file at one of your branches - make a commit and issue will gone

or copy your code, and place it after your changes from other branch

it's maybe not the best way to solve coding conflicts, but it will give you an idea about how git tracking changes inside files


---
