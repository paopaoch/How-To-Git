# Git Docs for Beginners cc2017

GIT is a version control system. It allows developers(us) to work as a team and keep track of all our files neatly. This document outlines how to use install and use git in our project.

For Windows users, please run the commands in Windows PowerShell rather than Command Prompt. Mac users can use the terminal as usual.

_for further info please visit http://git-scm.com/_

## Install Git
Determine whether git is installed in your computer or not by running this command: <br> 
```sh
git --version
```
<br>
If git is installed the output should be: 

<br>

> git version a.b.c <br>

If your computer doesn't have `git`, you can [install git](https://docs.gitlab.com/ee/topics/git/how_to_install_git/index.html). After installing Git, run `git --version` again to check whether the installation is successful. <br>

## Configure Git
You must enter your credentials to identify yourself. The username and email address should match your github account. <br>
### Add username
```sh
git config --global user.name "your_username" 
```
<br>

### Add email address 
```sh
git config --global user.email "your_email_address@example.com"
```
<br>

### Check configuration
```sh
git config --global --list
```
<br>

## Clone a repository
When you clone a repository, the files from the repository are downloaded to your computer and a connection is made. This connection requires you to add your credentials<br>
### Clone with HTTPS
1. Open a terminal and navigate to the directory where you want to clone the files
2. Go to this git hub projects main page, press code and copy the HTTPS to the clipboard
3. Run the following command. Git creates a folder with the repository name and downloads the files in there
```sh
git clone https://github.com/{URL_OF_YOUR_PROJECT}
```
4. Enter your username and password
5. Go to the newly added directory with:

```sh
cd {PROJECT_DIRECTORY}
```
## Branches
A branch is a copy of the files in the repository at the time you create the branch. We will always work in the dev branch, so when we make a mistake, it won't immediately affect our website. We will use pull request to pull from dev branch to master branch. 

### Switching Branch
```sh
git checkout dev
```
<br>

### View the files that have changed
```sh
git status
```
<br>

### Add and commit local changes
Once you have made some changes to your file you will want to add and commit it to your local git so git keeps track of the changes for you.

1. To stage a file for commit: 
```sh
git add \<file-name OR folder-name\>
```
2. Confirm that the files have been added with `git status`
3. To commit the staged files:
```sh
git commit -m 'Some USEFUL comment'
```

## Stage and commit all changes
A very useful shortcut for doing all files and changes at the same time is: <br>
```sh
git add --all
git commit -am 'Some USEFUL comment'
```
<br>

## Send changes to github
You can push all local changes to the github repository for your team members to see with the following command:
```sh 
git push
```
<br>

NOTE that you might be prompted to do `git push --set-upstream origin dev` which you should do for the first time

NOTE2 Sometimes you cannot push because your friend has pushed something that you haven't pulled so perform git pull first then push it back up. It is advised that you work on a branch and then push that branch instead to prevent this problem.

## Unstage all changes
To unstage all files that have not been committed:
```sh
git reset
```
## Undo most recent commit 
```sh
git reset HEAD~1
```
<br>

## Final Notes

These are just the basic git hub tools, for more git hub commands, you can click [here](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html).

If you are tired of typing in the password every time for git then please follow this tutorial: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
