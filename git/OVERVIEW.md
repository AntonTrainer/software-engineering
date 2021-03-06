# Git + Source Control

[https://realpython.com/python-git-github-intro/](https://realpython.com/python-git-github-intro/)

## Version Control system

Basically, version control is a set of tools for tracking the history of a set of files. This means you can tell Git (or any versions control (VCS)) to save your files in a certain state at any point.

Then, you can edit files, and save a new state. Saving the state is like creating a backup copy of the working directory

* This state saving is called a `commit` (oh word)

When making a commit, one adds a message that explains the changes. Git will show these changes and the full history, and is useful in pinpointing when a bug crept into the system

In addition to the logs, Git also allows you to compare files between different commits. Git also allows you to return any or all files from an earlier commit (with little effort)

## What NOT to Add to a Git Repo

**Basic rule of thumb is:**

* Only put source files into version control, never generated files
* Aka code written by hoomans, not produced output like .pyc

## Checking Out Old Code

So each commit has a hashID

```bash
# You can use:
$ git checkout 82NNMOKID8972BN3098U53209
# To check the branch out and see old files
```

## Branches

Branches provide a way to keep separate streams of development apart.

Dont always want to add chanes to master for fear of breaking everything, so do dev in branch.

To retain commits you need a branch
```bash
$ git checkout -b my_branch_name
```

After making changes, you can compare the two branches

```bash
$ git show-branch my_branch_name master
```

## Pulls

First, does a git fetch to upade all remotes/origin branches.

Then, if the branch you are on is tracking a remote branch, it does a git merge of the corresponding origin branch to your branch
