# Introduction to git and GitHub
## Install git
1. Click the SSH button for your instance that was made for you when you started the lab.
1. Run the following command in your SSH window:
* sudo apt-get install git-all
3. Verify your installation with the following command:
* git --version
## Create a new repository
1. Create a directory for your project with the mkdir (make directory) command:
* mkdir myproject
2. Then open the directory with the cd (change directory) command
* cd myproject
3. Now, initialize your new git repository in the folder with the git init command
* git init
## Add a file to the repo
1. Add a new file to the project. You can use any text editor you like when you are working on your own projects, but for this lab, simply create a new file with the touch command. Replace <file name> with a name for your file:
  * touch <file name>.txt
 2. Run the ls (list) command to verify that the file was created in your project directory:
 * ls
  3. Check to see which files git knows about with the git status command:
  * git status
