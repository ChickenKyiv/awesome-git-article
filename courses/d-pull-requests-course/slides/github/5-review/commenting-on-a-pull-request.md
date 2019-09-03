---
id: s3review10
title: Commenting on a pull request
sidebar_label: Commenting on a pull request
---


#### After you open a pull request in a repository, collaborators or team members can comment on the comparison of files
#### between the two specified branches, or leave general comments on the project as a whole.


In this section we'll talk about:

- About pull request comments
- Adding line comments to a pull request
- Resolving conversations


## About pull request comments


You can comment on a pull request's `Conversation` tab to leave general comments, questions, or props.

conversation.png

You can also comment on specific sections of a file on a pull request's Files changed tab in the form of individual line comments or as part of a pull request review. Adding line comments is a
great way to discuss questions about implementation or provide feedback to the author.

We talked about it before, when I explain to you a reviewing process.


**Note: If you reply to a pull request via email, your comment will be added on the Conversation tab and will not be part of a pull request review.**

To reply to an existing line comment, you'll need to navigate to the comment on either the `Conversation` tab
or `Files changed` tab and add an additional line comment below it.


**Tips:**

```
- Pull request comments support the same formatting as regular comments on GitHub,
such as @mentions, emoji, and references.
- You can add reactions to comments in pull requests in the Files changed tab.
```

-----------
------------



## Adding line comments to a pull request


We talked about it in previous slides.
I think you remember this image. You can add line comments as part of reviewing process

hover-comment-icon.gif


**Note: Anyone watching the pull request or repository will receive a notification of your comment.**


----------

## Resolving conversations


You can resolve a conversation in a pull request if you opened the pull request or if you have write access to the repository where the pull request was opened.

To indicate that a conversation on the `Files changed` tab is complete, click `Resolve conversation`.

conversation-with-resolve-button.png

The entire conversation will be collapsed and marked as resolved,
making it easier to find conversations that still need to be addressed.

resolved-conversation.png


Tips:

**To toggle between collapsing and expanding all outdated review comments in a**
**pull request, hold down `alt` and click Show outdated or Hide outdated.**



https://help.github.com/en/articles/commenting-on-a-pull-request
