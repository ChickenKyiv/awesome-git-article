


﻿#### Comparing Workflows


A Git Workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner.

Git workflows encourage users to leverage Git effectively and consistently.

Git offers a lot of flexibility in how users manage changes.

Given Git's focus on flexibility, there is no standardized process on how to interact with Git.

When working with a team on a Git managed project, it’s important to make sure the team is all in agreement on how the flow of changes will be applied. To ensure the team is on the same page, an agreed upon Git workflow should be developed or selected.

There are several publicized Git workflows that may be a good fit for your team.














































































































#### Example
Let’s take a general example at how a typical small team would collaborate using this workflow.

We’ll see how two developers, John and Mary, can work on separate features and share their contributions via a centralized repository.

**John works on his feature**

Git Workflows: Edit Stage Commit Feature Process

In his local repository, John can develop features using the standard Git commit process: edit, stage, and commit.

Remember that since these commands create local commits, John can repeat this process as many times as he wants without worrying about what’s going on in the central repository.

**Mary works on her feature**

Git Workflows: Edit Stage Commit Feature

Meanwhile, Mary is working on her own feature in her own local repository using the same edit/stage/commit process.
Like John, she doesn’t care what’s going on in the central repository, and she really doesn’t care what John is doing in his local repository, since all local repositories are private.



**John publishes his feature**
Git Workflows: Publish Feature
Once John finishes his feature, he should publish his local commits to the central repository so other team members can access it. He can do this with the git push command, like so:

`git push origin master`

Remember that origin is the remote connection to the central repository that Git created when John cloned it.

The master argument tells Git to try to make the origin’s master branch look like his local master branch.

Since the central repository hasn’t been updated since John cloned it, this won’t result in any conflicts and the push will work as expected.

**Mary tries to publish her feature**
Git Workflows: Push Command Error
Let’s see what happens if Mary tries to push her feature after John has successfully published his changes to the central repository. She can use the exact same push command:

`git push origin master`

But, since her local history has diverged from the central repository, Git will refuse the request with a rather verbose error message:

```error: failed to push some refs to '/path/to/repo.git'
hint: Updates were rejected because the tip of your current branch is behind

hint: its remote counterpart. Merge the remote changes (e.g. 'git pull')
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

This prevents Mary from overwriting official commits.

She needs to pull John’s updates into her repository, integrate them with her local changes, and then try again.

**Mary rebases on top of John’s commit(s)**
Git Workflows: Git Pull Rebase
Mary can use git pull to incorporate upstream changes into her repository. This command is sort of like svn update—it pulls the entire upstream commit history into Mary’s local repository and tries to integrate it with her local commits:

`git pull --rebase origin master`

The **--rebase** option tells Git to move all of Mary’s commits to the tip of the master branch after synchronising it with the changes from the central repository, as shown below:

Git workflows: Rebasing to Master

The pull would still work if you forgot this option, but you would wind up with a superfluous “merge commit” every time someone needed to synchronize with the central repository. For this workflow, it’s always better to rebase instead of generating a merge commit.

**Mary resolves a merge conflict**

Git Workflows: Rebasing on Commits

Rebasing works by transferring each local commit to the updated master branch one at a time.

This means that you catch merge conflicts on a commit-by-commit basis rather than resolving all of them in one massive merge commit. This keeps your commits as focused as possible and makes for a clean project history.

In turn, this makes it much easier to figure out where bugs were introduced and, if necessary, to roll back changes with minimal impact on the project.

If Mary and John are working on unrelated features, it’s unlikely that the rebasing process will generate conflicts.

But if it does, Git will pause the rebase at the current commit and output the following message, along with some relevant instructions:

`CONFLICT (content): Merge conflict in <some-file>`

Git workflows: Conflict Resolution

The great thing about Git is that anyone can resolve their own merge conflicts.

In our example, Mary would simply run a git status to see where the problem is. Conflicted files will appear in the Unmerged paths section:
```
# Unmerged paths:
# (use "git reset HEAD <some-file>..." to unstage)
# (use "git add/rm <some-file>..." as appropriate to mark resolution)
#
# both modified: <some-file>
```

Then, she’ll edit the file(s) to her liking. Once she’s happy with the result, she can stage the file(s) in the usual fashion and let git rebase do the rest:

```
git add <some-file>
git rebase --continue
```

And that’s all there is to it.
Git will move on to the next commit and repeat the process for any other commits that generate conflicts.

If you get to this point and realize and you have no idea what’s going on, don’t panic. Just execute the following command and you’ll be right back to where you started:

`git rebase --abort`

**Mary successfully publishes her feature**

Git Workflows: Synchronize Central Repo
After she’s done synchronizing with the central repository, Mary will be able to publish her changes successfully:

`git push origin master`










#### Where to go from here

As you can see, it’s possible to replicate a traditional Subversion development environment using only a handful of Git commands.

This is great for transitioning teams off of SVN, but it doesn’t leverage the distributed nature of Git.

The Centralized Workflow is great for small teams.

The conflict resolution process detailed above can form a bottleneck as your team scales in size.

If your team is comfortable with the Centralized Workflow but wants to streamline its collaboration efforts, it's definitely worth exploring the benefits of the Feature Branch Workflow.

By dedicating an isolated branch to each feature, it’s possible to initiate in-depth discussions around new additions before integrating them into the official project.






#### Other common workflows
The Centralized Workflow is essentially a building block for other Git workflows.

Most popular Git workflows will have some sort of centralized repo that individual developers will push and pull from.

Below we will briefly discuss some other popular Git workflows.

These extended workflows offer more specialized patterns in regard to managing branches for feature development, hot fixes, and eventual release.










## Feature branching

Feature Branching is a logical extension of Centralized Workflow.

The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated branch instead of the master branch.

This encapsulation makes it easy for multiple developers to work on a particular feature without disturbing the main codebase.

It also means the master branch should never contain broken code, which is a huge advantage for continuous integration environments.











## Gitflow Workflow

The Gitflow Workflow was first published in a highly regarded 2010 blog post from Vincent Driessen at nvie.

The Gitflow Workflow defines a strict branching model designed around the project release.

This workflow doesn’t add any new concepts or commands beyond what’s required for the Feature Branch Workflow.

Instead, it assigns very specific roles to different branches and defines how and when they should interact.









## Forking Workflow

The Forking Workflow is fundamentally different than the other workflows discussed in this tutorial. Instead of using a single server-side repository to act as the “central” codebase, it gives every developer a server-side repository. This means that each contributor has not one, but two Git repositories: a private local one and a public server-side one.

















#### Guidelines

There is no one size fits all Git workflow.

As previously stated, it’s important to develop a Git workflow that is a productivity enhancement for your team.

In addition to team culture, a workflow should also complement business culture.

Git features like branches and tags should complement your business’s release schedule.

If your team is using task tracking project management software you may want to use branches that correspond with tasks in progress.
















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












#### Summary
In this section we discussed Git workflows.

We took an in-depth look at a Centralized Workflow with practical examples.

Expanding on the Centralized Workflow we discussed additional specialized workflows.
Some key takeaways from this section are:

- There is no one-size-fits-all Git workflow

- A workflow should be simple and enhance the productivity of your team

- Your business requirements should help shape your Git workflow
