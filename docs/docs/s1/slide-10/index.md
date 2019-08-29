---
id: slide10
title: Create Readme.md file locally
sidebar_label: Create Readme.md file locally
---


Now you can create a file named “README.md” in your folder (through the terminal or user interface on your computer). I’m not giving you any more details about this step, nothing in particular. Open your folder and add a file as if it were a standard folder.

If you want to do something cool, copy and paste this template in your “README.md” file. You can replace information between the hooks to personalize the output.


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/a-004-readme-content.png)


<!-- ![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/b-10-github-changes-readme-added.png) -->


c. Let’s share our work!

Now that you have modified your project, you need to save it. This process is called committing.

To do this, get back to your terminal. If you have closed it, go back in your folder.

When you want to save your work, four steps are required.

These steps are called: “status”, “add”, “commit” and “push”.

I have prepared a standard procedure for you to perform each time you want to save your work.


> Note: All the following steps must be performed within your project.




**“status”**: The first thing you need to do once your work is to check the files you have modified.

To do this, you can type the following command to make a list of changes appear:
<!-- `$ git status` -->


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/a-005-git-status.png)


Here you can see an output from your **git status** command


![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/b-09-git-status.png)


If you decide to create another file at your repository. you will see a similar message here.

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/b-03-git-status-before-commit.png)

---




**“add”**: With the help of the change list, you can add all files you want to upload with the following command:


<!-- `$ git add [FILENAME] [FILENAME]` [...] -->

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/a-006-git-add.png)


In our case, we are going to add “README.md” because we want to save this file.

<!-- `$ git add README.md` -->

![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/carbon/a-007-git-add-readme.png)

> **Note: If you type again “git status”, the “README.md” will appear now in green. This means that we have added the file correctly.**
