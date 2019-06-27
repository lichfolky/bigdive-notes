**git Add** staging
**git Commit** snapshot
**git Push** is a shortcut to git fetch & git merge



### Start a git repo on Github
Move to the folder then Setup the folder
```
git init
```
Setup a git repo
```
git init
```
Check in all files
```
git add .
```
Commit and add all the files (m stands for message)
```
git commit -m "my message text"
```
Add the rep origin github
```
git remote add origin https://github.com/lichfolky/BigDive8Notes.git
```
Push the current branch to the remote  upstream
```
git push origin master
# or
git push --set-upstream origin master
```
remove git init (if something bad happens)
```
rm -rf .git
```
to see the git repository status
```
git status
```

### Ignore files
in the main folder, create a .gitignore file.
```
touch .gitignore
```
If the files are already checked in (added)
```
git rm --cached FILENAME
```
Create a global .gitignore
~/.gitignore_global
```
git config --global core.excludesfile ~/.gitignore_global
```
the rules are regex
> es:  
> .DS_Store  
> \*.class

the dot hide the file!
  to see it:
> ls -al

### Config global user data
```
git config --global user.email
git config --global user.name "Your Name"
```
After doing this, you may fix the identity used for this commit with:

`git commit --amend --reset-author`

### undo changes

**git checkout -- filename** can be used to undo change  
**git stash** -> undo but save the state  
**git reset --hard** super reset

you can undo commits!
____

### Contribute to an existing repository
```
# download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git

# change into the `repo` directory
cd repo

# create a new branch to store any new changes
git branch my-branch

# switch to that branch (line of development)
#git checkout my-branch

# make changes, for example, edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md

# take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

# push changes to github
git push --set-upstream origin my-branch



 take a snapshot of the staging area
git commit -m "add README to initial commit"

 provide the path for the repository you created on github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

create a git ignore file
$ touch ~/.gitignore
$ git config --global core.excludesFile ~/.gitignore
(Alt + 5 ~)

blame?

fork, branch?
