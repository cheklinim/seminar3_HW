# GIT INSTRUCTION
## How to work with Git.
Git - is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
![Git icon](git_image.png)
## Initialization of a new repository:
If you want to place a project under revision control, you should type the following command:

    git init

## Adding files:
If you want to add new or changed files in your working directory to the Git staging area, you should type the following command:

    git add <name of the file>

## Checking the status of the file:
If you want to check whether there exist some changes that you can add and commit (the command is extremely helpful when you are not sure whether you included something new to the file or whether you added it to Git), type:

    git status 

## Saving changes to Git:
If you want to save current amendment to the project history in Git, you should type the following command:

    git commit
It is always better to add to every your commit a massage that shows the user what was chnged comparing with the previous version of the file. You should type the same command but with addition  **-m "_some massage_"**:

    git commit -m "massage"
If you want to delete last commit, type the following command (removes first commit from the HEAD):

    git reset HEAD^

## Looking at all the commits:
To see all the versions of your project, type the following command (it will show you how each commit is named in the system and how you can refer to it while accessing the particular commit):

    git log
more user-friendly way of showing all the commits with no extra information, type:

    git log --oneline
you can also use the following command to see the tree with branches (we will talk about them later) and commits:

    git log --graph

## Accessing particular version:
If you want to return to particular version of the project you should type the following command and add the name of the commit (which you can see after typing **git log**) or the first 4 symbols:


    git checkout <name of the version>

## To see the difference:
If you want to see the difference between sets of something, you should type this command:

    git diff
By default **git diff** shows any uncommitted changes since the last commit.

For difference between two commits you should type:

    git diff <name of version> <name of version>

## Working with remote repository:
Currently your repository is located on your device and you can access it only from it. In order to turn it into a remote repository, which you and your colleges can access in any time and from anywhere, you should upload it to your GitHub account. To do this use this commands: 

    git remote add origin <URL>
URL is given to every remote repository created by you on your GitHub WebPage. You should create a repository, copy its URL and paste it in the <...> in the command.
After that you should type two more commands:

    git branch -M main

    git push -u origin main
Now everything from your local file is transfered to remote repository. But if you add something in the local one new information is not automatically transfered to the remote repository. In order to do this you should type the following command:

    git push
this command pushes your local commits to remote repository.

If something was added in your remote repository it also will not be automatically transfered to your local one. You should use the following command:

    git pull
this command pulls added information from your remote repository.

## Working with branches:
When you initialize a new repository you by default work on branch called "master" or "main", depends on the version of the programm. There your final copy of your project is usually placed. To create isolated development environments within a single repository where you can work with draft copy or any connected task or seperated parts of your project type:

    git branch <name of your new branch>
Now you have the second (side) branch. Everything that had been commited in the master branch by the moment of the creation of the side branch  also exists in your second branch. 

To check, on what branch you are currently working or what branches there exist in general, type:

    git branch
If you want to start work in your side branch, type:

    git checkout <name of your new branch>
If you want to return to your master branch, type:

    git checkout master
If you want to add your side branch to your master branch,type:

    git merge <name of your new branch>
If there exists a conflict between two branches (version) you are suggested several ways how to resolve it: to use the version from the master branch, to use the one from the side branch, to compile and etc. You should choose whatever suits you. 

When the work  with any of your side branch is done and it is no longer needed you can delete the side branch by typing the following command:

    git branch -d <name of the branch to delete>

## Creating a pull request:
If you want to add your repository to another person's repository on GitHub - to create a pull request - you should follow the steps below: 

1. access a repository you neeed
2. press the button in the upper right corner of the page called "Fork": now you have a copy of the "forked" repository in your account, which you have full access to and can work in.
3. copy the URL of the repository
4. type the command 

    git clone URL

5. create a new branch to make there our ammendments in the file
6. work only in the new branch
7. use the command git push to add your ammendments to the remote repository
8. On the GitHub page there appears the button:

    compare & pull request
9. if there is no problem merging the branches, than you can leave a comment to your work and create a pull request

    
## More tips:
* to clear the terminal, type:

    clear
* you can use arrow keys (up arrow, down arrow) to navigate through previously typed commands so not to write them again
