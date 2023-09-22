# Git Commands

_A list of my commonly used Git commands_

### Getting & Creating Projects

| Command                                                           | Description                                |
| ----------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command                            | Description                                       |
| ---------------------------------- | ------------------------------------------------- |
| `git status`                       | Check status                                      |
| `git add [file-name.txt]`          | Add a file to the staging area                    |
| `git add -A`                       | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes                                    |
| `git rm -r [file-name.txt]`        | Remove a file (or folder)                         |

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

### Inspection & Comparison

| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `git log`                                  | View changes                   |
| `git log --summary`                        | View changes (detailed)        |
| `git log --oneline`                        | View changes (briefly)         |
| `git diff [source branch] [target branch]` | Preview changes before merging |

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

- Your current branch name.
- Whether your current branch is up to date or not.
- Number of commits that your branch is behind its remote branch.
- Changes that are staged and to be committed.
- Changes that are not staged for commit.
- Un-tracked files.

```bash
git status
```
