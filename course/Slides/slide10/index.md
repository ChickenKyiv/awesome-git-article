####
b. Repository edition

Now you can create a file named “README.md” in your folder (through the terminal or user interface on your computer). I’m not giving you any more details about this step, nothing in particular. Open your folder and add a file as if it were a standard folder.

If you want to do something cool, copy and paste this template in your “README.md” file. You can replace information between the hooks to personalize the output.

c. Let’s share our work!

Now that you have modified your project, you need to save it. This process is called committing.

To do this, get back to your terminal. If you have closed it, go back in your folder.

When you want to save your work, four steps are required. These steps are called: “status”, “add”, “commit” and “push”. I have prepared a standard procedure for you to perform each time you want to save your work.

> Note: All the following steps must be performed within your project.
“status”: The first thing you need to do once your work is to check the files you have modified.

To do this, you can type the following command to make a list of changes appear:
`$ git status`

“git status” output in our project
“add”: With the help of the change list, you can add all files you want to upload with the following command:
`$ git add [FILENAME] [FILENAME]` [...]
In our case, we are going to add “README.md” because we want to save this file.

`$ git add README.md`
Note: If you type again “git status”, the “README.md” will appear now in green. This means that we have added the file correctly.

“commit”: Now that we have added the files of our choice, we need to write a message to explain what we have done. This message may be useful later if we want to check the change history. Here is an example of what we can put in our case.
`$ git commit -m "Added README.md with good description in it."`

“push”: You’re there, you can now put your work online! If you type the following command, all your work will be put online and visible directly on the repository page.
`$ git push origin master`

You did it! If you come back on your repository page on GitHub, you are going to your “README.md” file with a beautiful preview of it.
