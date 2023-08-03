# GIT

Its an distributed version control system, which means each every person has a copy of each repo. It saves the changes made by different people on the same project.

## Installing GIT

Download and install git using the link -

https://git-scm.com/downloads

## GIT bash

It's like a terminal which behaves like UNIX. Which can also be used as a terminal.

Once you open the git bash you can set an default user and user email using the commands :

git config --global user.name (your name)

git config --global user.email (your email)

to check weather its been set run the following commands-

git config --global user.name

git config --global user.email 

### Initializing the  Repository

To make a repo one can type the following command:

git init

which will result in initializing an empty git repository

('ls -lart' command shows all the hidden folders )

### Types of Files

Untracked - We are not tracking this file using git. This is the first stage in which the files are present.

Unmodified- After the file is staged it moves into this area and now is a part of git.

Modified- Once the file is in the git one can modify its contents and once they are modified the file must be sent to staging area.

Staged- This area is where we put files that are to be committed

The image below shows the way this system works-



![image-20230803162911876](C:\Users\achin\AppData\Roaming\Typora\typora-user-images\image-20230803162911876.png)

### Adding Files to the git

Make a folder and open git bash in it, to initialize a repository type the following command-

git init

now make a HTML file named index.html in that folder and in git bash type the following-

git status

once this command is given in the git bash it'll show that html file is in untracked area to move it to the staging area :

git add index.html

note: if there were more than one file that had to be moved in staging area one can use the command "git add -A" which will move all the untracked files to the staging area.

After the files have been moved to the staging area one has to commit them using 

git commit

which will open an vim editor: to operate that one must first type "I" and then type the name of that commit for eg-"Initial commit or First commit". To exit that vim editor press esc and type ":wq".

alternatively to avoid getting into vim editor mode one can also use the command:

git commit -m "The message you want to type along with your commit"

One can clear the terminal using "clear" command

## GIT commands

### GIT checkout 

Suppose you made a mistake in the program and saved it but didn't commit that change to git. So the work of a checkout command is to match your file code with the code that is already present on the git repo one can easily revert back the changes made to their file that is in untracked area using checkout command:

In case of corruption of multiple files one can use 

git checkout -f

to revert back changes of all the effected files.

### Git Log 

git log

This command can be used to check how many commits have been made in the repository. If the commits are in a large number then one can use 

git log -p -"the number of commits you want to see"

and it will give the difference between the commits.

### GIT diff

git diff

It compares the untracked file to the staging area of that particular file. Once you add that change to the staging area it no longer shows the difference. Now to compare the staging area and last commit -

 git diff  --staged

and to revert those changes one can always use "git checkout -f" 

### Directly Committing 

git commit -a -m "commit message that you want to type"

Skipped staging area and directly committing to the repo.

### LS

LS function is used to list all the files present in the repository 

### Touch

touch "name of the file along with the doc type"

Touch function is used in git to create new files in the system. These files further are to be placed on repo by using commit.

### GIT rm

git rm "the name of the file you want to remove from the repo"

rm command is used to remove the file from the repo as well as from the system. To remove the file from the repo but not from the system one can used --cached command.

git rm --cached 

### GIT ignore

touch .gitignore

gitignore file is created so that one can ignore the unwanted files that are present in the repo. To do that simply open the file in an editor and type in the file name that you want to ignore along with the doc type. For eg if you want to ignore a log file named "Mylog.log" simply type the name into that gitignore file you've created and if one wants to ignore all the log files use "*.log" to ignore all the log files.

Similarly if user wants only to ignore only one particular file then one should type "/mylogs.log" into the gitignore folder. hence the other files named mylogs.log will not be ignored.

## Branches

git branch "name of the branch which you want to create"

Branching is to create a copy of all the data for other users to work on modify and commit. The main branch is called master by default. To go in the branch that user created one should use the command:

git checkout "name of the branch"

Suppose user made a branch feature and added better features on that particular branch and now want to add those features to the master branch. Therefore, one must merge the feature branch with the master branch.

git merge "name of the branch"

To make a branch and simultaneously switch to it user has to use:

git checkout -b "name of the branch" 

## Pushing to Git hub

One can push their repo to git hub by making a repo in git and then using command 

git push origin master

note: here one can upload any branch to the repo user must rename the branch master to the desired branch name.



