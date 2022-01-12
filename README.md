# GitHub-Test-Repo
This repo is used for practicing using GitHub. Part of The Complete Web Development Bootcamp by Angela Yu


Flow of Local Git files:
1. The git initialised Working Directory
2. The Staging area (where you can add the files you want git to track from the Working Directory)
3. The Local Repository (Where all the save points and located of the Working Directory) 


Start with `git init` in terminal to initialise git in the working directory


Staging Area: A middle ground where you can decide which files you want to commit to the master/main or any other branch of the repository. 
To see what files are currently in the staging area, run `git status` in the terminal
To add files/folders to the staging area, run `git add {file/folder path}`. To add all the files in the working directory, run `git add .`
To remove all files from the staging area, run `git rm —cached -r .` (`-r` is a flag that means recursive)
To remove a particular file from the staging area, run `git restore —staged {filename}`


Committing Changes is finalising all the files you want to add in the staging area and creating a savepoint. To do this, run `git commit`. To add a message to the commit use the `-m` flag like this `git commit -m “message”` (Use present tense in message as per convention)
You can see all the commits you’ve made by using `git log`
You can compare a current non committed file with its last committed save-point by running `git diff {filename}`  
You can revert back a file to the latest save point in your Working Directory (with the help of the Local Repository) by running `git checkout {filename}`   


Adding the Local Repository to a remote server on GitHub:
Add a repository from your account from the GitHub web client.
Follow the Command Line instructions given in the Quick Setup window:
`git remote add origin {repository link}` (`origin` is the name of the remote repo)
Push the changes to the remote repo:
`git push -u origin master` (`-u` links the remote and local repositories)


GitIgnore Files: Files which contain sensitive or irrelevant information which you don’t want to push onto the remote repository.
Make a file in the working directory called `.gitignore` . Type all the file names, separated by newline characters, which you want to ignore while committing to git into the `.gitignore` file.
Tips:
1. You can use `#` sign to add comments in the .gitignore files
2. You can use `*` symbol as a wild card to ignore all the files of a particular extension (ex- `*.txt`)


Cloning a repository from GitHub: Copying a remote repository and all its save points into our local device
To do this:
1. Copy the link of the remote repo from the GitHub Web Client by navigating to the repository and clicking on the “Code” button
2. Run `git clone {repo link}` in the terminal


Branching repositories: To simultaneously work on a part of the repo without affecting the main/master branch. 
To made a branch, run `git branch {branch name}`
To check what branches you have, run `git branch` (the `*` sign in the output denotes what branch you are on right now) 
To switch branches, run `git checkout {branch name}`
You can edit your files here and also commit them locally and push them to the remote repository by running `git push -u origin {branch name}`



Merging repositories: When we merge the master branch and some other branch of the repo to bring the changes made to the other branch into the main branch.
To do this:
1. Make sure you’re in the master branch
2. Run `git merge {name of branch to be merged}`
3. This opens a vim file in the terminal so that you can add a merge message. This is optional.
4. Type `:q!` in the vim window if you don’t want to include a merge message 
