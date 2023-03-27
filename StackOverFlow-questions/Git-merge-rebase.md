### What's the difference between Git merge, rebase, and interactive rebase?

Git **merge** is a command used to join two or more branches together. It combines multiple commits into a single commit, preserving the history of the project.

The simplest way is to merge the main branch with the feature branch using the following code:
```
git checkout feature
git merge main
```
Git **rebase** is a form of a merge, but with rewriting the project’s history. Rebasing rewrites the commit history by making fresh commits for each commit in the original branch.

To use the rebase option, run the following commands:
```
git checkout feature
git rebase main
```
Finally, **interactive rebase** allows you to edit and reorder commits before pushing them to a remote repository. This goes up a notch above the rebase and offers complete control over the branch’s commit history. 

To start an interactive rebasing session, provide the `i` option to the `git rebase` command:

git checkout feature
git rebase -i main

This will open a text editor that shows all the commits that are going to be transferred:
```
pick 33d5b7a Message for commit #1
pick 9480b3d Message for commit #2
pick 5c67e61 Message for commit #3
```

You can change the history of a branch by altering the pick command and arranging the entries differently. For instance, you can use the `fixup` command to compress the entries into a single commit.
```
pick 33d5b7a Message for commit #1
fixup 9480b3d Message for commit #2
pick 5c67e61 Message for commit #3
```
