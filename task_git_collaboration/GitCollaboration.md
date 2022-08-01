## Git collaboration

GitHub provides free access to a Git server for public and private repositories.

#### Some tips using git&GitHub

1. If we want to make a **change to a remote branch** you should **pull** the remote branch, **merge** it with the local branch, then **push** it back to its origin.

2. The main **difference** between **git fetch** and **git pull**:
- git fetch **fetches** remote updates but **doesn't merge**; 
- git pull **fetches** remote updates and **merges**;
- git pull instantly merges while git fetch only retrieves remote updates.

3. As long as there are no conflicts, Git will move the current branch tip up to the target branch tip and combine histories of both commits.

4. git remote update will fetch the contents of all remote branches and allow us to merge the contents ourselves.

5. If you want to see more information about a particular remote branch, you can use the git remote show command. Don't forget the commit ID!

6. git fetch will download remote updates, such as objects and refs, from the remote branch.

7. An explicit merge creates a new merge commit. This alters the commit history and explicitly shows where a merge was executed.
git pull automatically merges the remote branch with the current branch.

8. What should you do with the <<<<<<<, =======, and >>>>>>> conflict markers when resolving a merge conflict?
- Remove all of the conflict markers and only leave the code as it should be after the merge. Conflict markers aren’t required when resolving a merge conflict.

9. To switch to a new local branchuse the command git checkout -b <branch name> . It will first create a new branch and then switch to it.

10. “git rebase refactor” moves the current branch on top of the refactor branch.This makes debugging easier and prevents three-way merges by transferring the completed work from one branch to another.

11. Rebasing instead of merging rewrites history and maintains linearity, making for cleaner code.

12. **!Always** synchronize your branches before starting any work on your own. This way, when you start changing code, you're starting from the most recent version, minimizing chances of conflicts or the need for rebasing.

13. The git pull command runs git fetch with the given parameters, then calls git merge to merge the retrieved branch heads into the current branch.

14. **git rebase** is useful for maintaining a clean, linear commit history.

15. It's common practice to keep the latest version in the master branch and the latest stable version in a separate branch.

16. Try to **make changes as small as possible**, as long as they’re self-contained.
That way, whenever you start changing code, you know that you're starting from the most recent version, and you minimize the chances of conflicts or the need for rebasing.
This lets you work on new changes, while still enabling you to fix bugs in the other branch.

17. You can also use git rebase <branchname> to change the base of the current branch to be <branchname>.

#### Cheats

**git remote**  - Lists remote repos

**git remote -v** - List remote repos verbosely

**git remote show <name>** - Describes a single remote repo

**git remote update** - Fetches the most up-to-date objects

**git fetch** - Downloads specific objects

**git branch -r** - Lists remote branches; can be combined with other branch arguments to manage remote branches

#### More tips from 2d week

1. The fixup operation will keep the original message and discard the message from the fixup commit, while squash combines them.

2. You send a pull request to the owner of the repository in order for them to incorporate it into their tree.
For instance, when you want to propose changes to someone else's project, or base your own project off of theirs.

3. **git push** with the **-f** flag forcibly replaces the old commits with the new one and forces Git to push the current snapshot to the repo as it is. This can be dangerous as it can lead to remote changes being permanently lost and is not recommended unless you're pushing fixes to your own fork (nobody else is using it) such as in the case after doing interactive rebasing to squash multiple commits into one as demonstrated.

4. The reword keyword lets us change the commit message, keeping the changes as they are, but modifying the commit message.

5. It is good manners and proper conduct to respond, even when it's simply an acknowledgement.

6. In git jargon (and elsewhere in the tech world), a nit is a minor “nitpick” about a piece of code.

7. Unclear names can make our code hard to understand.

8. If there is a specific condition that could cause a problem and we don't address it, the result could be catastrophic.

9. Tests are an important addition to our code to ensure it runs smoothly.

10. If we push a new version after making a change, old comments are marked with the "Outdated" flag.

11. By reviewing our code, we can identify where we can make our code more clear and easy to understand.

12. By comparing our code to style guidelines, we can keep our style consistent and readable.

13.  Code review can reveal cases or conditions we need to handle in our code.

14. Keywords such as closes or resolves followed by a hashtag and the issue number will tell Git to autolink to the issue with the provided ID number.
A
15. rtifacts can include compiled code, test results, logs, or any type of file generated as part of the pipeline.

16. The more time that passes until a pull-request gets reviewed, the more likely it is that there's a new commit that causes a conflict when you try to merge in the change.

17. Not only do we not know whether the original coder is going to be around to maintain those functions, we also want to avoid feature creep and unmanageable code.
T
18. he larger our project grows, the more useful an issue tracker can be for collaborating.

19. A continuous integration system will build and test our code every time there's a change.

20. When it comes to coordinating who does what and when, a common strategy for active software projects is to use an **issue tracker**.


#### Some articles to learn more:

[About the perfect code review](https://medium.com/osedea/the-perfect-code-review-process-845e6ba5c31)

[About pull request reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)

[About pull request merges](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges)

[come back to README](../README.md)