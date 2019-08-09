https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow















---
id: s2d8
title: Git merge Part2
sidebar_label: Git merge Part2
---

#### Branching in the Forking Workflow
All of these personal public repositories are really just a convenient way to share branches with other developers.

Everybody should still be using branches to isolate individual features, just like in the Feature Branch Workflow and the Gitflow Workflow.
The only difference is how those branches get shared. In the Forking Workflow, they are pulled into another developer’s local repository, while in the Feature Branch and Gitflow Workflows they are pushed to the official repository.


---
id: s2d9
title: Git merge Part2
sidebar_label: Git merge Part2
---

#### Fork a repository
git fork workflow - fork a repositiory
All new developers to a Forking Workflow project need to fork the official repository.
As previously stated, forking is just a standard git clone operation.
It’s possible to do this by SSH’ing into the server and running `git clone` to copy it to another location on the server.
Popular Git hosting services like GitHub, offer repo forking features that automate this step.


---
id: s2d10
title: Git merge Part2
sidebar_label: Git merge Part2
---
#### Clone your fork
Next each developer needs to clone their own public forked repository.
They can do this with the familiar `git clone` command.

Assuming the use of GitHub to host these repositories, developers on a project should have their own GitHub account and they should clone their forked copy of the repository with:

`git clone https://user@host/user/repo.git`


---
id: s2d11
title: Git merge Part2
sidebar_label: Git merge Part2
---

#### Adding a remote

Whereas other Git workflows use a single origin remote that points to the central repository, the Forking Workflow requires two remotes—one for the official repository, and one for the developer’s personal server-side repository.

While you can call these remotes anything you want, a common convention is to use origin as the remote for your forked repository (this will be created automatically when you run git clone) and upstream for the official repository.

`git remote add upstream https://github.com/maintainer/repo`

You’ll need to create the upstream remote yourself using the above command.
This will let you easily keep your local repository up-to-date as the official project progresses.
Note that if your upstream repository has authentication enabled (i.e., it's not open source), you'll need to supply a username, like so:

`git remote add upstream https://user@host/maintainer/repo.git`

This requires users to supply a valid password before cloning or pulling from the official codebase.


---
id: s2d12
title: Git merge Part2
sidebar_label: Git merge Part2
---

Working in a branch: making & pushing changes
In the developer's local copy of the forked repository they can edit code, commit changes, and create branches just like in other Git workflows:

`git checkout -b some-feature`

# Edit some code
`git commit -a -m "Add first draft of some feature"`

All of their changes will be entirely private until they push it to their public repository.
And, if the official project has moved forward, they can access new commits with git pull:

`git pull upstream master`

Since developers should be working in a dedicated feature branch, this should generally result in a fast-forward merge.


---
id: s2d13
title: Git merge Part2
sidebar_label: Git merge Part2
---

#### Making a Pull Request
Git Fork Workflow - Making a pull request
Once a developer is ready to share their new feature, they need to do two things.
First, they have to make their contribution accessible to other developers by pushing it to their public repository.
 Their origin remote should already be set up, so all they should have to do is the following:

`git push origin feature-branch`

This diverges from the other workflows in that the origin remote points to the developer’s personal server-side repository, not the main codebase.


Second, they need to notify the project maintainer that they want to merge their feature into the official codebase.
GitHub provides a “pull request” button that leads to a form asking you to specify which branch you want to merge into the official repository.
Typically, you’ll want to integrate your feature branch into the upstream remote’s master branch.
