# smiths-project

If faced any issue with denied permission delete git credentials in keychain and do ssh again, or remove security credentials if you're using windows.(Google)

## Set these defaults first before initializing a git repository.

```bash
# Set your global Git username
git config --global user.name "Your Name"
# Set your global Git email address
git config --global user.email "Your Email"
# Configure Git to use the "simple" push strategy
git config --global push.default simple
# Create a Git alias for 'checkout'
git config --global alias.co checkout
# Set the default branch name for new repositories to 'main'
git config --global init.defaultBranch main
# Initialize a new Git repository with the 'main'
```

## To initialize repository

```bash
git init -b main
# Connect your local repository to a remote repository
git remote add origin your_git_repo_link
# Stage all changes in your working directory
git add .
# Create an initial commit with a descriptive message
git commit -am "initial commit"
# Push your local 'main' branch to the 'main' branch on the remote repository
git push -u origin main
```

# Git Branch Commands and Use Cases

Git branches are used in version control systems like Git to manage and organize development workflows. They allow developers to work on different features, bug fixes, or experiments concurrently without affecting the main codebase. Here's why and when Git branches are commonly used:

- Isolation: Git branches allow for isolated work on different tasks.<br>
- Parallel Development: Multiple branches enable concurrent feature development.<br>
- Bug Fixing: Branches are used to isolate and fix bugs.<br>
- Experimentation: Developers can use branches for testing and experimentation.<br>
- Collaboration: Branches facilitate collaboration and code reviews in a team environment.<br>

## Table of Contents

1. [Create a New Branch](#create-a-new-branch)
2. [Switch to a Branch](#switch-to-a-branch)
3. [List Branches](#list-branches)
4. [Delete a Branch](#delete-a-branch)
5. [Rename a Branch](#rename-a-branch)
6. [Merge Branches](#merge-branches)
7. [Rebase Branches](#rebase-branches)
8. [Push a Branch](#push-a-branch)
9. [Pull Changes from a Remote Branch](#pull-changes-from-a-remote-branch)
10. [Track a Remote Branch](#track-a-remote-branch)

---

## Create a New Branch

Use this command to create a new branch with the specified name. This allows you to start working on a new feature or bug fix without affecting the main development branch.

```bash
git branch <branch_name>
```

## Switch to a Branch

Use this command to switch to an existing branch. You'll start working in the context of that branch, allowing you to make changes specific to it.

```bash
git checkout <branch_name>

```

## List Branches

This command lists all local branches in your Git repository, showing you the current branch with an asterisk.

```bash
git branch
```

## Delete a Branch

Use this command to delete a branch once you've merged its changes into another branch. The -d flag stands for "delete."

```bash
git branch -d <branch_name>
```

## Rename a Branch

This command allows you to rename the current branch to the specified new name.

```bash
git branch -m <new_branch_name>
```

## Merge Branches

Use this command to merge changes from the specified branch into your current branch. It combines the work from both branches.

- Note: Before merging, you should update your local development/master branch. This is because your teammates might have merged into the parent branch while you were working on your branch.
- Command to fetch updates
  `bash
     git pull or git fetch
    `
  If there are no conflicts while pulling the updates, you can merge your branch into the parent branch.

```bash
git merge <branch_name>
```

## Rebase Branches

Rebasing is an alternative to merging that allows you to integrate changes from one branch onto another by applying each commit from your branch onto the branch you're rebasing onto.

```bash
git rebase <branch_name>
```

## Push a Branch

This command pushes the changes from your local branch to the remote repository, creating or updating the branch on the remote.

```bash
git push origin <branch_name>
```

## Pull Changes from a Remote Branch

Use this command to fetch and merge changes from a remote branch into your current branch.

```bash
git pull origin <branch_name>
```

## Track a Remote Branch

This command sets up a tracking relationship between your local branch and the corresponding remote branch. It allows you to use git pull and git push without specifying the remote branch each time.

```bash
git branch --set-upstream-to=origin/<branch_name>
```

# Status
It returns the following information about your branch:

* Your current branch name.
* Whether your current branch is up to date or not.
* Number of commits that your branch is behind its remote branch.
* Changes that are staged and to be committed.
* Changes that are not staged for commit.
* Un-tracked files.

```bash
git status
```
