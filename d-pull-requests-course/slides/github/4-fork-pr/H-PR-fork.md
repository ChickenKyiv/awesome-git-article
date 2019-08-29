#### Creating a pull request from a fork

If you've forked a repository and made changes to the fork, you can ask that the upstream repository accept your changes by creating a pull request.

You can open a pull request to the upstream repository from any branch or commit in your fork.

We recommend that you make changes in a topic branch, so that you can push `follow up commits` if
you receive feedback on your pull request.

You also have the option to give the upstream repository's maintainers the
ability to make commits on your topic branch to update your pull request.

If your pull request compares your topic branch with a branch in the upstream
repository as the base branch, then your topic branch is also called the compare branch of the pull request.



**Note: To open a pull request in a public repository, you must have write access to the head or the source branch or, for organization-owned repositories, you must be a member of the organization that owns the repository to open a pull request.**


[IMG]
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


- Navigate to the original repository you created your fork from.

- To the right of the Branch menu, click New pull request.


pull-request-start-review-button
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


- On the Compare page, click compare across forks.


compare-across-forks-link
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


- Confirm that the `base fork` is the repository you'd like to merge changes into.

Use the `base branch` drop-down menu to select the branch of the upstream repository you'd like to merge changes into.


choose-base-fork-and-branch
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


- Use the `head fork` drop-down menu to select your fork, then use the
`compare branch` drop-down menu to select the branch you made your changes in.


choose-head-fork-compare-branch (1)
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


- Type a title and description for your pull request.


pullrequest-description
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)



- If you do not want to allow anyone with push access to the upstream repository to make changes to your PR, unselect **Allow edits from maintainers**.


allow-maintainers-to-make-edits (1)
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


To create a pull request that is ready for review, click **Create Pull Request**.

To create a draft pull request, use the drop-down and select **Create Draft Pull Request**, then click **Draft Pull Request**.


pullrequest-send
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/commands/02-reset.png)


<!--
"Working with forks"
"Creating a pull request"

"Allowing changes to a pull request branch created from a fork"

"Committing changes to a pull request branch created from a fork"

-->
