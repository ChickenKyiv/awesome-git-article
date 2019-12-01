I’ve been working on software development for 10 years now and along the way, 
I’ve had the opportunity to collaborate on several open source projects and also worked 
on many non-open source projects where we used Github as our version control repository, on small and large teams.

---

On my journey, I’ve followed different workflows depending on the project and today 
I want to share with you what I consider to be an effective and pragmatic workflow 
for building and maintaining good quality software that can be applied to any project.

---

The attributes of good quality software are many: robustness, testability, resilience, modularity, maintainability, usability, security, performance, scalability and more depending on the type of application you are building. On this article I’ll mainly focus on the following characteristics:


Good documentation: readme, documentation sites, and changelogs.
Well defined coding standards and conventions.
Proper versioning with semver.
Automated tests: not too many, focus on functional non-regression tests.
Developer happiness, sure!

---

To accomplish this I’m proposing a pragmatic Github flow leveraging open source 
tools that help facilitate and automate many of the tasks required to achieve this goal.

If you are working on an open source project you want to publish your project Github, 
that’s a fact. 
Git and Github have radically changed the way OSS is developed by becoming the de-facto 
common language for version control and definitive place for collaboration respectively.

The official workflow proposed by Github is called github flow and it’s very well 
documented on their website guides.github.com/introduction/flow, most open source projects 
follow this workflow with slightly different flavors.

---

The Github workflow is very flexible in the sense that it doesn’t tell you how to release 
and document changes, what merge strategy to use when accepting pull request, what tools to use, 
what commit standards to follow or what to review before accepting a pull request, that’s up you and that makes a lot a of sense since there’s no universal solution for every team’s needs.


The following is a list of recommendations based on my experience:

I work mainly ( almost exclusively ) in JavaScript, many of the tools I’ll mention are part of JS ecosystem, however, the principles apply to any language.

---

Prioritize your Issues and Track your Progress with Github Projects
In September 2016 Projects feature was launched. It is tool allows you to 
create kanban style boards to organize, prioritize and track your work at the 
repository and organization level. If you use Github issues I strongly suggest you 
make use of the feature for organizing and communicating better the priorities 
of the project and the current efforts. You can learn more on the following link 
help.github.com/articles/tracking-the-progress-of-your-work-with-project-boards

---

Classify your Issues with Tags
Github provides great filtering functionalities. If you are working on an open 
source project you want people to collaborate on your project as well as provide 
a good experience to the developers using it. By tagging your issues developers will 
able to more easily navigate the issue list, saving them time and allowing them 
to contribute with less entry friction.

---

Leverage Github Templates for Pull Request and Issues
Taking the time to write Github templates for your issues and pull request will certainly pay off; This will force or at least help developers to report bugs and request features in the standard way with all the information you need to address them.

Learn more at blog.github.com/2016–02–17-issue-and-pull-request-templates

---

Some general guidelines for bug reports:

Before submitting an issue please check that you’ve completed the following steps:

Made sure you’re on the latest version
Used the search feature to ensure that the bug hasn’t been reported before
Bug reports should contain the following information:

Summary: A brief description.
Steps to reproduce: How did you encounter the bug? Instructions to reproduce it.
Expected behavior: How did you expect it to behave?
Actual behavior: How did it actually behave?
References: Links to any related tickets or information sources.
If possible, attach visual documentation of the bug. Screenshots, video and/or animated gifs.
Pull Request General Guidelines:

Please make sure that there aren’t existing pull requests attempting to address the issue mentioned.
Check for related issues on the issue tracker.
Non-trivial changes should be discussed on an issue first.
Let us know you’re working on the issue.
Develop in a topic branch, not master.
Provide useful pull request description.
Follow project commit guidelines.
Write a good description of your PR.
Link to the Github issue in the description.
Use the Command Line
The console is your friend. In my experience learning to interact with Github from the command line is the best use of your time if you work with open source technologies. There are many nice GUIs, however, none of them will give the flexibility of the command line. There’s also tooling that will make life much simpler and a more efficient developer that is only available for the command line:

hub is a command-line wrapper for git that makes you better at GitHub. Whether you are a beginner or an experienced contributor to open-source, hub makes it easier to fetch repositories, navigate project pages, fork repos and even submit pull requests, all from the command-line. hub.github.com
tj/git-extras is a set of git utilities such as repo summary, repl, changelog population, author commit percentages and more. github.com/tj/git-extras
Follow Strict Commit Message Standards and Do Scoped Commits
Always define and follow clear commit message standards for your projects, some general guidelines are:

Commit each fix as a separate change.
Provide useful commit messages.
Provide a short commit message in the first line (50–100 character). Looking at the output of gitk or git log --onelinemight help you understand why.
Reference the git issue on the body of your commit message.
Additionally, I strongly suggest you scope your messages for a better changelog generation. When you scope your messages your changelogs can be more informative. The AngularJS commit conventions and changelog generation is a great example gist.github.com/stephenparish/9941e89d80e2bc58a153#generating-changelogmd

Define Coding Style Standards and Configure Pre-commit Hooks
Defining coding standards and enforce them through pre-commits hooks is essential for writing maintainable code. By following these standards you make sure all code looks the same regardless who wrote it, facilitating taking over and maintaining code written by someone else.

My recommended setup is Prettier and StandardJS, however, that’s a matter of preference, there are many others and you can also configure a custom one, as long as you follow a coding standard you will benefit.

typicode/husky is a great tool to configure pre-commit hooks.

Configure Automated Tests and Checks on Pull Requests
Automated functional tests, security and code style checks against every pull request are highly desirable, you don’t want to do it manually. A continuous integration server such as TravisCI can be quickly configured to run these test automatically against the topic branch every time a pull request is submitted and Github can be configured to prevent the developer from merging pull requests that don’t pass these test. If these automated tests fail Github will display a message on the pull request for the requester to fix them.

Learn more at docs.travis-ci.com/user/pull-requests
