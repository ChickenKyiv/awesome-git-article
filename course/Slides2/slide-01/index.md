---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/merge/simple-git-flow.png)


﻿#### Comparing Workflows


A Git Workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner.

Git workflows encourage users to leverage Git effectively and consistently.

Git offers a lot of flexibility in how users manage changes.

Given Git's focus on flexibility, there is no standardized process on how to interact with Git.

When working with a team on a Git managed project, it’s important to make sure the team is all in agreement on how the flow of changes will be applied. To ensure the team is on the same page, an agreed upon Git workflow should be developed or selected.

There are several publicized Git workflows that may be a good fit for your team.




























---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


#### Where to go from here

As you can see, it’s possible to replicate a traditional Subversion development environment using only a handful of Git commands.

This is great for transitioning teams off of SVN, but it doesn’t leverage the distributed nature of Git.

The Centralized Workflow is great for small teams.

The conflict resolution process detailed above can form a bottleneck as your team scales in size.

If your team is comfortable with the Centralized Workflow but wants to streamline its collaboration efforts, it's definitely worth exploring the benefits of the Feature Branch Workflow.

By dedicating an isolated branch to each feature, it’s possible to initiate in-depth discussions around new additions before integrating them into the official project.








---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


#### Other common workflows
The Centralized Workflow is essentially a building block for other Git workflows.

Most popular Git workflows will have some sort of centralized repo that individual developers will push and pull from.

Below we will briefly discuss some other popular Git workflows.

These extended workflows offer more specialized patterns in regard to managing branches for feature development, hot fixes, and eventual release.











---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


## Feature branching

Feature Branching is a logical extension of Centralized Workflow.

The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated branch instead of the master branch.

This encapsulation makes it easy for multiple developers to work on a particular feature without disturbing the main codebase.

It also means the master branch should never contain broken code, which is a huge advantage for continuous integration environments.










---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


## Gitflow Workflow

The Gitflow Workflow was first published in a highly regarded 2010 blog post from Vincent Driessen at nvie.

The Gitflow Workflow defines a strict branching model designed around the project release.

This workflow doesn’t add any new concepts or commands beyond what’s required for the Feature Branch Workflow.

Instead, it assigns very specific roles to different branches and defines how and when they should interact.








---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


## Forking Workflow

The Forking Workflow is fundamentally different than the other workflows discussed in this tutorial. Instead of using a single server-side repository to act as the “central” codebase, it gives every developer a server-side repository. This means that each contributor has not one, but two Git repositories: a private local one and a public server-side one.


















---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


#### Guidelines

There is no one size fits all Git workflow.

As previously stated, it’s important to develop a Git workflow that is a productivity enhancement for your team.

In addition to team culture, a workflow should also complement business culture.

Git features like branches and tags should complement your business’s release schedule.

If your team is using task tracking project management software you may want to use branches that correspond with tasks in progress.














---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---



In addition, some guidelines to consider when deciding on a workflow are:

#### Short-lived branches

The longer a branch lives separate from the production branch, the higher the risk for merge conflicts and deployment challenges. Short-lived branches promote cleaner merges and deploys.

#### Minimize and simplify reverts
It’s important to have a workflow that helps proactively prevent merges that will have to be reverted. A workflow that tests a branch before allowing it to be merged into the master branch is an example.

However, accidents do happen.

That being said, it’s beneficial to have a workflow that allows for easy reverts that will not disrupt the flow for other team members.

#### Match a release schedule
A workflow should complement your business’s software development release cycle.

If you plan to release multiple times a day, you will want to keep your master branch stable.

If your release schedule is less frequent, you may want to consider using Git tags to tag a branch to a version.













---
id: slide13aa
title: Git merge Part2
sidebar_label: Git merge Part2
---


#### Summary
In this section we discussed Git workflows.

We took an in-depth look at a Centralized Workflow with practical examples.

Expanding on the Centralized Workflow we discussed additional specialized workflows.
Some key takeaways from this section are:

- There is no one-size-fits-all Git workflow

- A workflow should be simple and enhance the productivity of your team

- Your business requirements should help shape your Git workflow
