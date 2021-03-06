# Github 

# What is GitHub
Github is a website that allows to upload code to a repository, Once that code has been uploaded, it can be kept track of, managed, accessed and updated by other users. 

Allowing others to collabrate on projects together, big or small, this becomes really important when working on a code project with two or more members where it becomes easier to track and know what changes have been made to the project, by who and when they were made.

# What is Version Control
Version Control is a set of software tools that help a software team manage changes made to source code over time, Version control software keeps track of any changes made to the source code each time a change is made. So when a mistake is made the code can be reverted back to a previous version or the previous versions of the code can be checked to see where the problem is coming from.

# What is Git
Git is a source control tool that allows developers to share code, back up code and track changes made to code.

# Installing Git
To set up Git on your computer, install it from the official website https://git-scm.com/

To run Git in a folder / file directory right click the folder and then press run Git Bash here

# Git commands
git clone - Creates a copy of the repository in a new directory
```
git clone
```
git add - adds new or changes files to the working directory, we can choose what files we want to add to our repository before making any commits, We must git add to our directory before doing a commit using git commit
```
git add
```
git commit - Commits changes made to the repository
```
git commit -m "Your commit message here"
```

git pull - Grabs the latest changes made to a repository
```
git pull
```
git push - Pushs the changes made to the repository
```
git push origin branchnam
```

# Creating a GitHub Account
To create a Github Account go to the website at https://github.com/

On the landing page you can press the sign up button at the top of the page or enter a username, password and an email address to create a Github Account

# Creating a Repository 
To create a repository in github, go to the home page of your github account. On the left side there is a repositories tab, press the green button on the right hand side. Enter the repository name, you can enter a description but aren't required to but I would recommend adding a description, set the repository to public or private. Choose if you want to add a README file, .gitignore and a license (not required), Once done press the create repository button to create a new repository.

# Creating a local git repository 
To create a local repository in git, First we need to create a folder in the directory where we want our repository to be, we can do this by doing the following
```git
cd ~/Desktop
mkdir myproject
cd myproject 
```

cd - will move to the directory 
mkdir - will create a directory in the target directory

Then run the git init command to create a git repository in the root of the folder
```git
myproject$ git init
```

# Adding a file to a local git repository 
We can add a file to a local git repository using git add, 
```
git add file
```
Once we added our file we can commit it using git commit

# Uploading to a Repository using Git
To upload to a repository using Git we need to do the following 

First add our github repository along with a remote name to Git so we can push any changes made to Github, We can do this using
```
git remote add origin repository link here
```
```
or git remote add repository link here
```
Example: 
```
git remote add origin git remote add origin https://github.com/emarkexe2001/Uploading-to-GitHub-using-Git.git
```
Once we have done that to push our commit to GitHub we need to use git push - But first always do a pull to make sure that make sure their are no changes in the branch before you push your commit
```
git push -u origin main
```
# Uploading to a Repository using Visual Code Studio

To upload to a Repository in Visual Studio Code, Navigate to Source Control (The third option on the Sidebar). Stage any changes made if you made a change to a file, add a commit message to the change you made. Copy the repo link and use git remote add on the terminal to add it to VS Code. Press the tick button to commit your change. Press the ... button and push using the push button.
