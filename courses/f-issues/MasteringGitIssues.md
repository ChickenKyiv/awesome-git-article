https://guides.github.com/features/issues/


- Intro
- Milestones, Labels & Assignees

- Notifications, @mentions and references
- Search
- Overviews & Reports
- Other uses for Issues


---

Continues here


#### Labels
Labels are a great way to organize different types of issues. Issues can have as many labels as you want, and you can filter by one or many labels at once.


labels-listing
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/labels-listing.png)

#### Assignees
Each issue can have an assignee — one person that’s responsible for moving the issue forward. Assignees are selected the same way milestones are, through the grey bar at the top of the issue.




### Notifications, @mentions, and References
By using @mentions and references inside of Issues, you can notify other GitHub users & teams, and cross-connect issues to each other. These provide a flexible way to get the right people involved to resolve issues effectively, and are easy to learn and use. They work across all text fields on GitHub — they’re a part of our text formatting syntax called GitHub Flavored Markdown.



markdown-example
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/markdown-example.png)
If you’d like to learn more, have a look at Mastering Markdown.

### Notifications
Notifications are GitHub’s way to keep up to date with your Issues. You can use them to find out about new issues on repositories, or just to know when someone needs your input to move forward on an issue.

There are two ways to receive notifications: via email, and via the web. You can configure how you receive notifications in your settings. If you plan on receiving a lot of notifications, we like to recommend that you receive web + email notifications for **Participating** and web notifications for **Watching**.


notifications
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/notifications.png)

With these settings, you receive emails when people specifically mention you, then visit the web-based interface to keep up to date with repositories you’re interested in.

You can access your notifications through the notifications screen. This screen is nice for scanning many notifications at once and marking them as read or muting the thread. Try using keyboard shortcuts to speed up your workflow here — press **?** on the page to see which shortcuts are available.


notification
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/notification.png)

Muted threads won’t show up as unread again until you are specifically @mentioned again. This makes muting a great strategy for threads that you have little interest in (perhaps a sub-system that you aren’t familiar with). If you mark an issue as read, it will stay that way until someone comments on the thread again.

GitHub also syncs read/unread status for email notifications — if you read a notification in your email client, it will be marked as read in the web-based interface (make sure you allow your email client to display images if you’d like this functionality).


### @mentions
@mentions are the way that we reference other GitHub users inside of GitHub Issues. Inside of the description or any comment of the issue, include the @username of another GitHub user to send them a notification. This works very similar to how Twitter uses @mentions.

We like to use the `/cc` syntax (an abbreviation for carbon copy) to include people in issues:

> It looks like the new widget form is broken on Safari. When I try and create the widget, Safari crashes. This is reproducible on 10.8, but not 10.9. Maybe a browser bug?

> /cc @kneath @jresig

This works great if you know the specific users to include, but many times we’re working across teams and don’t really know who might be able to help us. @mentions also work for Teams within your GitHub organization. If you create a Team called browser-bugs under the @acmeinc organization, you can reference the team with @mentions:

> /cc @acmeinc/browser-bugs

This will send notifications to every member of the browser-bugs team.






### References
Often times issues are dependent on other issues, or at least relate to them and you’d like to connect the two. You can reference issues by typing in a hashtag plus the issue number.

> Hey @kneath, I think the problem started in #42

When you do this, we’ll create an event inside of issue #42 that looks something like this:

reference
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/reference.png)


Issue in another repository? Just include the repository before the name like `kneath/example-project#42.``

One of the more interesting ways to use GitHub Issues is to reference issues directly from commits. Include the issue number inside of the commit message.




commit
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/commit.png)


By prefacing your commits with “Fixes”, “Fixed”, “Fix”, “Closes”, “Closed”, or “Close” when the commit is merged into master, it will also automatically close the issue.

References make it possible to deeply connect the work being done with the bug being tracked, and are a great way to add visibility into the history of your project.


### Search
At the very top of each page is a search box that lets you search through issues.



search
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/search.png)


You can scope search results by:

Keyword, such as, all issues mentioning the sidebar

State, such as, all issues mentioning the sidebar that are closed

Assignee, such as, all issues mentioning the sidebar that were assigned to @mdo

Our Help article on searching Issues can show you other ways to search: using created/updated dates, labels, authors, comment counts, by repository owner, and more.

https://help.github.com/articles/using-search-to-filter-issues-and-pull-requests


## Overviews & Reports
Outside of the Issues section, there are two other pages that help summarize what’s going on with Issues across your repository and across all of your repositories.

### The Issue Dashboard

If you’re looking for a broader listing of all of your issues across many projects, the Issues Dashboard can be a great tool. The dashboard works very similar to the issues section, but collects issues differently:

- All issues in repositories you own and collaborate on
- Issues assigned to you
- Issues you’ve created
If you use organizations, each one has its own Issues dashboard that separates out Issues within the organization.

### Pulse
Underneath each repository is a section called Pulse — Pulse is a snapshot of everything that’s happened in the repository in the past week (or day, or past 3 months, etc).

pulse
![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/issues/pulse.png)


It’s a great way to catch up with repositories when you’ve been away and don’t want the granularity notifications offer when watching a repository.
