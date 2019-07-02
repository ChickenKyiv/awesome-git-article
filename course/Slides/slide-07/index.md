####
b. Git installation

Now you need to install Git tools on your computer. There are different Git software, but it’s better to install the basic one to start. We will use the command line to communicate with GitHub.

Once you are more comfortable with the command line, you can download Git software with a user interface.

#### For Ubuntu:
First, update your packages:

`$ sudo apt update`
Next, install Git with apt-get:

`$ sudo apt-get install git`
Finally, verify that Git is installed correctly:

`$ git --version`

#### For MacOSX:
First, download the latest Git for Mac installer.

Next, follow instructions on your screen.

Finally, open a terminal and verify that Git is installed correctly:

`$ git --version`

#### For Windows:
First, download the latest Git for Windows installer.

Next, follow instructions on your screen (you can leave the default options).


Finally, open a terminal (example: `powershell` or g`it bash`) and verify that Git is installed correctly:

`$ git --version`



For all users:
One last step is needed to complete the installation correctly! You need to run in your terminal the following commands with your information to set a default username and email when you are going to save your work:

`$ git config --global user.name "Arthur Tkachenko"
$ git config --global user.email "example@mail.com"`
