# LearnMoreGit

Welcome to **LearnMoreGit**, a comprehensive guide to Git commands with clear explanations and practical examples. This README covers essential Git commands for beginners and intermediate users, focusing on real-world usage and understanding.

---

## Git Configuration (`git config`)

`git config` is used to configure Git settings such as user information, proxy settings, and signing keys. These settings help Git identify who is making commits and control other behaviors.

### Common commands:

```bash
git config --global user.name "UserName"
```
Set your Git username globally (used in commits).

```bash
git config --global user.email "Email"
```
Set your email globally.

```bash
git config --global user.signingkey sec
```
Set your GPG key for signing commits.

---

## Initialize a Git Repository (`git init`)

Starts a new Git repository by creating a `.git` directory (hidden on Unix-based systems).

### Examples:

```bash
git init
```
Initialize Git repo in current directory.

```bash
mkdir MyProject
cd MyProject
git init
```
Create a new directory and initialize a Git repo inside.

---

## Adding Files to Git (`git add`)

Stages files to be committed.

### Examples:

```bash
git add fileName
```
Add a single file to the staging area.

```bash
git add -A
```
Add all files (tracked and untracked) to staging.

```bash
git add .
```
Add all files in the current directory and subdirectories.

---

## Viewing Commit History (`git log`)

Shows the commit history.

### Examples:

```bash
git log
```
Show full commit history with details.

```bash
git log --oneline -5
```
Show the last 5 commits in a simplified one-line format.

---

## Commit Changes (`git commit`)

Save staged changes with a message.

### Examples:

```bash
git commit -m "Title"
```
Commit with a short message.

```bash
git commit -m "Title" -m "Description"
```
Commit with a title and longer description.

```bash
git commit -am "Title"
```
Commit tracked files with changes without `git add`.

---

## Check Repository Status (`git status`)

Shows the current state of the working directory and staging area.

```bash
git status
```

---

## Clean Untracked Files (`git clean`)

Remove untracked files from working directory.

```bash
git clean -f
```
Remove untracked files (use `-f` to force).

---

## Unstage a File (`git reset`)

Remove files from the staging area.

```bash
git reset fileName
```

---

## Show Differences (`git diff`)

Show changes between working directory, staging area, and commits.

### Examples:

```bash
git diff HEAD
```
Show changes since last commit.

```bash
git diff --staged
```
Show staged changes.

```bash
git diff branchName
```
Show difference between current branch and another branch.

---

## Revert Changes (`git checkout` and `git reset`)

Restore files or move HEAD pointer.

### Examples:

```bash
git checkout -- fileName
```
Revert file to last committed state.

```bash
git reset commitHash
```
Move HEAD to a specific commit, unstaging changes.

```bash
git reset --hard commitHash
```
Move HEAD and discard all changes.

---

## Branching (`git branch` and `git checkout`)

Manage branches.

### Examples:

```bash
git branch
```
List branches.

```bash
git branch branchName
```
Create a new branch.

```bash
git checkout -b branchName
```
Create and switch to new branch.

```bash
git checkout branchName
```
Switch to an existing branch.

---

## Merge Branches (`git merge`)

Merge changes from another branch into the current branch.

```bash
git merge branchName
```

---

## Remove Files (`git rm`)

Remove files from Git and filesystem.

```bash
git rm fileName
```

Restore file after accidental remove:

```bash
git checkout HEAD fileName
```

---

## Delete or Rename Branch (`git branch`)

```bash
git branch -d branchName
```
Delete branch.

```bash
git branch -M branchName
```
Rename branch (commonly used to rename default branch to `main`).

---

## Push and Pull (`git push` and `git pull`)

Synchronize with remote repositories.

```bash
git push origin master
```
Push master branch to remote `origin`.

```bash
git pull origin master
```
Fetch and merge master branch from remote.

---

## Manage Remotes (`git remote`)

Manage remote repositories.

```bash
git remote
```
List remotes.

```bash
git remote add origin url
```
Add a new remote named origin.

```bash
git remote remove remoteName
```
Remove a remote.

```bash
git remote rename oldName newName
```
Rename a remote.

---

## Show Commit or Tag Details (`git show`)

```bash
git show commitID
```
Show details of a specific commit.

```bash
git tag
```
List tags.

```bash
git tag -a tagName -m "description"
```
Create an annotated tag.

```bash
git show tagName
```
Show tag details.

---

## View File History (`git blame`)

Show line-by-line author info.

```bash
git blame fileName -L startLine,endLine
```
Show authorship info for a range of lines.

---

## Debug with Bisect (`git bisect`)

Find the commit that introduced a bug.

```bash
git bisect start
git bisect bad
git bisect good commitHash
```
Bisect between good and bad commits.

```bash
git bisect reset
```
Stop bisect and return to original state.

---

## Stashing Changes (`git stash`)

Save uncommitted changes temporarily.

```bash
git stash
```

```bash
git stash list
```

```bash
git stash pop stash@{0}
```

---

## Clone Repository (`git clone`)

Copy remote repository locally.

```bash
git clone repositoryAddress
```

---

## Cherry-pick Commits (`git cherry-pick`)

Apply a commit from another branch to the current one.

```bash
git cherry-pick commitHash
```

---

# Summary

This README provides fundamental Git commands and practical examples to help you get started and manage your projects efficiently. For detailed help, use `git help <command>` or visit the [official Git documentation](https://git-scm.com/doc).

Happy Git learning! 🚀

---

*Created by Max Base*
