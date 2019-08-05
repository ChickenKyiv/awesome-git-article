




---
id: s7
title: Guidelines Part2
sidebar_label: Guidelines Part2
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
