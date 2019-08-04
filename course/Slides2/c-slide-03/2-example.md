
Example
A complete example demonstrating a Feature Branch Flow is as follows. Assuming we have a repo setup with a master branch.

git checkout master
git checkout -b develop
git checkout -b feature_branch

# work happens on feature branch

git checkout develop
git merge feature_branch
git checkout master
git merge develop
git branch -d feature_branch
In addition to the feature and release flow, a hotfix example is as follows:

git checkout master
git checkout -b hotfix_branch

# work is done commits are added to the hotfix_branch

git checkout develop
git merge hotfix_branch
git checkout master
git merge hotfix_branch
