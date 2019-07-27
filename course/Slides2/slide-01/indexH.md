---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)

#### Hosted central repositories

Central repositories are often created through 3rd party Git hosting services like Bitbucket Cloud or Bitbucket Server.

The process of initializing a bare repository discussed above is handled for you by the hosting service.

The hosting service will then provide an address for the central repository to access from your local repository.

#### Clone the central repository
Next, each developer creates a local copy of the entire project. This is accomplished via the git clone command:

`git clone ssh://user@host/path/to/repo.git`

When you clone a repository, Git automatically adds a shortcut called origin that points back to the “parent” repository, under the assumption that you'll want to interact with it further on down the road.
