Checking out pull requests locally





https://help.github.com/en/articles/checking-out-pull-requests-locally#modifying-an-active-pull-request-locally

#### When someone sends you a pull request from a fork or branch of your repository, you may want to merge it locally to resolve a merge conflict or to test and verify the changes on your local computer before merging on GitHub.

**Note: You can ask the person who created the pull request to allow anyone with push access to the upstream repository to push commits to their pull request to help their work merge faster.**


A. Modifying an active pull request locally
B. Modifying an inactive pull request locally
C.  Error: Failed to push some refs









C.  Error: Failed to push some refs

The remote `refs/pull/` namespace is `read-only`. If you try to push any commits there, you'll see this error:

```sh
! [remote rejected] HEAD -> refs/pull/1/head (deny updating a hidden ref)
error: failed to push some refs to 'git@github.local:USERNAME/REPOSITORY.git'
```


**Tip: When you remove or rename a remote reference, your local `refs/pull/origin/` namespace will not be affected by calls to `git-remote`.**
