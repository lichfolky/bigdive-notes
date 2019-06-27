setup a git repo
```
git init
```
see status
```
git status
```
add the rep to github
```
git remote add origin https://github.com/lichfolky/BigDive8Notes.git
```

remove git init
```
rm -rf .git
```
add all files
```
git add .
```
To push the current branch and set the remote as upstream, use
```
git push origin master
git push --set-upstream origin master
```

git add filename //add file to the repo

git rm file //remove

git commit -m "txt" //m stands for message

git config --global user.email "" // global is for all sys

git push

git pull

to set a master source and push changes to github
```
git push --set-upstream https://github.com/lichfolky/BIGDIVE8_MyStuff.git`
```


\\ commit and adding the already added file
git commit -am "ciao"


git remote add origin git@github.com:lichfolky/BIGDIVE8_MyStuff.git

git push -u origin master

////
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

git commit --amend --reset-author
///

$ git remote rm origin
$ git remote add origin git@github.com:aplikacjainfo/proj1.git
$ git config master.remote origin
$ git config master.merge refs/heads/master


Example: Contribute to an existing repository
# download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git

# change into the `repo` directory
cd repo

# create a new branch to store any new changes
git branch my-branch

# switch to that branch (line of development)
git checkout my-branch

# make changes, for example, edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md

# take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

# push changes to github
git push --set-upstream origin my-branch

Example: Start a new repository and publish it to GitHub

# create a new directory, and initialize it with git-specific functions
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
touch README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "add README to initial commit"

# provide the path for the repository you created on github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

create a git ignore file
$ touch ~/.gitignore
$ git config --global core.excludesFile ~/.gitignore
(Alt + 5 ~)

blame?

fork, branch?
