 
 GitHub provides free access to a Git server for public and private repositories.

 If we want to make a change to a remote branch, what must we do? Pull the remote branch, merge it with the local branch, then push it back to its origin
 What’s the main difference between git fetch and git pull? 
git fetch fetches remote updates but doesn't merge; git pull fetches remote updates and merges.git pull instantly merges while git fetch only retrieves remote updates.

Assuming no merge conflicts, which type of merge does git pull perform automatically? Fast-forward merge As long as there are no conflicts, Git will move the current branch tip up to the target branch tip and combine histories of both commits.

#### cheats

**git remote** Lists remote repos
**git remote -v** List remote repos verbosely
**git remote show <name>** 	
Describes a single remote repo
**git remote update** Fetches the most up-to-date objects
**git fetch** Downloads specific objects
**git branch -r** Lists remote branches; can be combined with other branch arguments to manage remote branches


git remote update will fetch the contents of all remote branches and allow us to merge the contents ourselves.
If you want to see more information about a particular remote branch, you can use the git remote show command. Don't forget the commit ID!
git fetch will download remote updates, such as objects and refs, from the remote branch.
An explicit merge creates a new merge commit. This alters the commit history and explicitly shows where a merge was executed.
git pull automatically merges the remote branch with the current branch.
continue here https://www.coursera.org/learn/introduction-git-github/lecture/n3GnN/the-pull-merge-push-workflow