


#### Initialize the central repository

Git Workflow: Initialize Central Bare Repository

First, someone needs to create the central repository on a server.

If it’s a new project, you can initialize an empty repository.

Otherwise, you’ll need to import an existing Git or SVN repository.

Central repositories should always be bare repositories (they shouldn’t have a working directory), which can be created as follows:

`ssh user@host git init --bare /path/to/repo.git`

Be sure to use a valid SSH username for user, the domain or IP address of your server for host, and the location where you'd like to store your repo for `/path/to/repo.git`. Note that the **.git** extension is conventionally appended to the repository name to indicate that it’s a bare repository.
