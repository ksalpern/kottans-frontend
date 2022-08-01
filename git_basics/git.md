# Git та GitHub

## Useful commands

### - git init

command helps to create a new repository

### – git status

command helps to check current repository status:

$ git status

On branch master

Initial commit

Untracked files:
  (use "git add ..." to include in what will be committed)

    hello.txt


### – git commit

$ git commit -m "Initial commit."
command helps to make a new commit


### – git clone

command do repository cloning

$ git clone https://github.com/codeguida/nolink.git

A new local repository is automatically created, with the github version configured as a remote repository.

### – git pull

command helps to receive changes from the server

$ git pull origin master

From https://github.com/codeguida/nolink
 * branch            master     -> FETCH_HEAD
Already up-to-date.


### – git branch

command creates a new branch

$ git branch amazing_new_feature

This only creates a new branch, which is currently the same as master.

### – git checkout

command does transition between branches

$ git branch
  amazing_new_feature
* master

Master is the current branch and is marked with an asterisk. But we want to work on our new amazing applications, so we need to move to another branch. This is done using the git checkout command, with the parameter - a branch to which we need to go.

$ git checkout amazing_new_feature

### – git merge

command does connection of branches

$ git add feature.txt
$ git commit -m "New feature complete."

## Thanks for reading you can also check the whole article [Git for 30 minutes](https://codeguida.com/post/453)

[come back to README](../README.md)
