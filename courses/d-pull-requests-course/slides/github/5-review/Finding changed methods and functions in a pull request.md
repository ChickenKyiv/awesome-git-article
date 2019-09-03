---
id: s3review10
title: Finding changed methods and functions in a pull request
sidebar_label: Finding changed methods and functions in a pull request
---



#### You can quickly find proposed changes to a method or function in a pull request in .go, .js, .ts, .py, .php, and .rb files.





Anyone with read access to a repository can see a summary
list of the functions and methods changes in certain files of a pull request.

The summary list of methods and functions is created from these supported file types:


- Go
- JavaScript (includes Typescript, Flow, and other types of JavaScript)
- PHP
- Python
- Ruby

1. Under your repository name, click  Pull requests.

---

2. In the list of pull requests, click the pull request where you'd like to find the changed functions and methods.

---

3. On the pull request, click  `Files changed`.

---

4. To see a summary list of the changed functions and methods, click `Jump to....`




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/PR/review/jump-to-menu.png)

5. Select the changed function or method from the drop-down menu.
You can also enter the name of the function or method to filter results.




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/PR/review/filter-function-and-methods.png)


**Note: If you don't see the functions or methods you expected, confirm that your code compiles and doesn't contain errors. Only functions and methods changed in this pull request and found in .go, .js, .ts, .py, .php, and .rb files appear in the drop-down menu.**

6. You'll be redirected to the first line of the function or method you selected.




![xxx](https://raw.githubusercontent.com/ChickenKyiv/awesome-git-article/master/img/PR/review/view-selected-function-or-method.png)





https://help.github.com/en/articles/finding-changed-methods-and-functions-in-a-pull-request