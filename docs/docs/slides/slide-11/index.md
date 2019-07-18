---
id: slide11
title: Useful commands for Git
sidebar_label: Useful commands for Git
---



You are still missing some essential commands as a beginner with Git. Here is a list that will be useful to you during your project.

Display the history of commits (all modifications made on the project).

`$ git log`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-log.png)

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/b-11-git-log.png)


---

Revert back all your changes since the last commit.

`$ git checkout .`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-checkout-dot.png)

---

Revert all changes on a specific file since the last commit.

`$ git checkout [FILENAME]`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-checkout-filename.png)

---

Display the last changes on a file since the last commit.

`$ git diff [FILENAME]`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-diff.png)

---

Remove all unexpected files in your project (not committed).

`$ git clean -dfx`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-clean.png)

---

Add all files and make a commit at the same time.

`$ git commit -am [MESSAGE]`

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/d-git-commit.png)

![xxx](https://github.com/ChickenKyiv/awesome-git-article/blob/master/img/carbon/b-06-git-commit.png)


---

## What’s next?

Branching logic in git
