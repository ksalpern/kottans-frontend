# Things I see useful about a version controll system

- It helps to keep track of changes made to our files

- By keeping track of the changes that we make to our files, a VCS lets us know when a file changed, who changed it, and also lets us easily roll back those changes.

- By having each change tracked in the VCS, it's very easy to go back to previous versions when an issue with a change is discovered.

- One of the main benefits of a VCS is that you can see the history of how files changed and understand what changed at each step and what motivated the change.

- Diffing Files: the diff tool shows all the differences between any type of file

- Applying Changes: while diff is the command that generates the difference between two files, patch is the command that applies those differences to the original file.

- Practical Application of <ins>diff</ins> and <ins>patch</ins>: To automatically apply changes to a file, we need to run the patch command on the file that we want to modify with the diff file as input.

## More about diff, diff -u, patch

### diff

- diff is used to find differences between two files. On its own, it’s a bit hard to use; instead, use it with diff -u to find lines which differ in two files:

### diff -u

- diff -u is used to compare two files, line by line, and have the differing lines compared side-by-side in the same output.

### Patch

- Patch is useful for applying file differences. See the below example, which compares two files. The comparison is saved as a .diff file, which is then patched to the original file!
> 

# Using Git

<ins>The git directory acts as a database for all the changes tracked in Git and the working tree acts as a sandbox where we can edit the current versions of the files.</ins>

- After modifying a file, we need to stage those changes and then commit them afterwards.

- You can’t commit with an empty commit message.

## <ins>important</ins> Anatomy of a Commit Message


Commit message should look like a short description of the change (up to 50 characters), followed by one or more paragraphs giving more details of the change (if needed).

#### Answer the following questions:

1. Why is this change necessary?

2. How does it address the issue?

> Describe, at a high level, what was done to affect change. Introduce a red/black tree to increase search speed or Remove <troublesome gem X>, which was causing <specific description of issue introduced by gem> are good examples.

3. What side effects does this change have?

This is the most important question to answer, as it can point out problems where you are making too many changes in one commit or branch. One or two bullet points for related changes may be okay, but five or six are likely indicators of a commit that is doing too many things.

Your team should have guidelines and rules-of-thumb for how much can be done in a single commit/branch.

[for more details](https://thoughtbot.com/blog/5-useful-tips-for-a-better-commit-message)

