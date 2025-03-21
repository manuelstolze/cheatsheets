# Git

This README serves as a quick reference guide for common Git commands and workflows. It covers everything from initializing a repository to advanced topics like rebasing and stashing. Use this cheat sheet to speed up your development process and keep Git commands at your fingertips.

## Table of Contents
- [Configuration](#configuration)
- [Basic Commands](#basic-commands)
- [Committing Changes](#committing-changes)
- [Branching and Merging](#branching-and-merging)
- [Remote Repositories](#remote-repositories)
- [Stashing](#stashing)
- [Rebasing](#rebasing)
- [Resetting and Reverting](#resetting-and-reverting)
- [Additional Tips](#additional-tips)

---

## Configuration

Set your user details and default editor so your commits are properly attributed.

```bash
# Set your global username and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Optionally, set your preferred text editor (e.g., nano)
git config --global core.editor "nano"
```

---

## Basic Commands

Initialize a new repository or clone an existing one.

```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone <repository-url>
```

---

## Committing Changes

Check the status, stage files, and commit your changes.

```bash
# Check repository status
git status

# Stage specific file(s) or all changes
git add <file>
git add .

# Commit staged changes with a message
git commit -m "Your commit message"

# For tracked files, stage and commit in one step
git commit -am "Your commit message"
```

---

## Branching and Merging

Work with branches to manage features and fixes.

```bash
# List existing branches
git branch

# Create a new branch
git branch <branch-name>

# Create and switch to a new branch
git checkout -b <branch-name>

# Switch to an existing branch
git checkout <branch-name>

# Merge a branch into the current branch
git merge <branch-name>

# Delete a branch (after merging)
git branch -d <branch-name>
```

---

## Remote Repositories

Manage your connections to remote repositories.

```bash
# Add a remote repository
git remote add origin <repository-url>

# List remote repositories
git remote -v

# Push changes to a remote repository (set upstream)
git push -u origin <branch-name>

# Pull changes from a remote repository
git pull origin <branch-name>
```

---

## Stashing

Temporarily save changes you’re not ready to commit.

```bash
# Save uncommitted changes
git stash

# List stashed changes
git stash list

# Apply the latest stash and remove it from the stash list
git stash pop

# Remove a specific stash (if needed)
git stash drop
```

---

## Rebasing

Rebase your branch to create a linear history or clean up commits.

```bash
# Rebase current branch onto master
git rebase master

# Interactive rebase to edit, squash, or reorder commits (last 3 commits example)
git rebase -i HEAD~3
```

---

## Resetting and Reverting

Undo changes using reset or revert commands.

```bash
# Reset to a specific commit, keeping changes staged (--soft)
git reset --soft <commit-hash>

# Reset to a specific commit, unstaging changes (--mixed)
git reset --mixed <commit-hash>

# Reset to a specific commit and discard changes (--hard)
git reset --hard <commit-hash>

# Revert a commit by creating a new commit that undoes its changes
git revert <commit-hash>
```

---

## Additional Tips

- View a compact, graphical commit history:
  ```bash
  git log --oneline --graph --decorate
  ```
- See what has changed in your working directory:
  ```bash
  git diff
  ```
- Get help on any Git command:
  ```bash
  git help <command>
  ```

---

*This cheat sheet is intended as a quick reference guide. For more details, check out the [Pro Git book](https://git-scm.com/book/en/v2) or the [official Git documentation](https://git-scm.com/docs).*

Happy coding!

#resource #cheatsheet

