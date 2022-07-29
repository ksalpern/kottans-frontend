# Using Git 

## commands to get more information about our changes:

### git commit -a

Command is a shortcut to stage any changes to tracked files and commit them in one step. If the modified file has never been committed to the repo, we'll still need to use git add to track it first. So let's make a change to our example script from an earlier video and try out this new flag. We'll now modify our main function and make it call the check reboot function that we wrote before. If a reboot is pending, we'll print a message and then exit our program with an exit status of one. Since we're using the sys module, we'll need to import it.

The **-m** flag allows us to directly add the commit message to the command.

The **-a** flag lets us add and commit in the same step.

This is useful, but if we're combing through a history of changes in a repo to try and find what caused the latest outage, we'll probably also need to look at the actual lines that changed in each commit. To do this with git log, we can use the **-p** flag. The p comes from patch, because using this flag gives us the patch that was created. 

If we don't want to scroll down until we find the commit that we're actually interested in, another option is to use the **git show** command. This command takes a commit ID as a parameter, and will display the information about the commit and the associated patch. Taking the commit ID, **git show** will show information about the commit and its associated patch.

## deleting and renaming files:

### git rm

This command removes files from the working tree and from the index.

### git mv

Renames  files in the repository
> The status shows us that the file was renamed and clearly displays the old and new names.

## ls-la

We can see all(even hidden) files using this command.

## Short summary:

**git commit** -a Stages files automatically

**git log -p** Produces patch text

**git show** Shows various objects 

**git diff** Is similar to the Linux `diff` command, and can show the differences in various commits 

**git diff --staged** 	
An alias to --cached, this will show all staged files compared to the named commit

**git add -p** Allows a user to interactively review patches to add to the current commit

**git mv** Similar to the Linux `mv` command, this moves a file

**git rm** Similar to the Linux `rm` command, this deletes, or removes a file


## Git Revert

**git checkout** restores files to the latest stored snapshot, reverting any changes before staging.

**git reset** basically resets the repo, throwing away some changes.

**git commit --amend** allows us to modify and add changes to the most recent commit. 

With **git revert**, a new commit is created with inverse changes. This cancels previous changes instead of making it as though the original commit never happened. It’s a bit like an undo command.

continue [here](https://www.coursera.org/learn/introduction-git-github/lecture/0X9k7/what-is-a-branch)