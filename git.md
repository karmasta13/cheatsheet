
### Daily git Workflow

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Create and switch to a new branch | `git checkout -b <branch_name>` |
| Check the status of your working directory | `git status` |
| Stage all changes for commit | `git add .` |
| Stage-specific files for commit| `git add <file(s)>` |
| Stage all changes, including deletions   | `git add -u` | `git add -all` |
| Commit staged changes with a descriptive message| `git commit -m "Commit message"` |
| Push commits to a remote repository| `git push origin <branch_name>` |

### Initializing a Repository

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Initialize a New Git Repository in the Current Directory | `git init` |
| Clone an Existing Repository to Your Local Machine    | `git clone <repository_url>` |


### Staging Changes

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Stage Changes for Commit                        | `git add <file(s)>` |
| Unstage Changes                                  | `git reset <file(s)>` |
| View Staged and Unstaged Changes                | `git status` |

### Branching and Merging

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| List Local Branches                             | `git branch` |
| Create a New Branch                             | `git branch <branch_name>` |
| Switch to a Different Branch                    | `git checkout <branch_name>` |
| Merge Changes from One Branch to Another        | `git merge <branch_name>` |
| Delete a Branch                                 | `git branch -d <branch_name>` |

### Inspecting and Comparing

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| View Commit History                             | `git log` |
| Show Differences Between Commits                | `git diff <commit_hash1> <commit_hash2>` |
| Show Remote Repositories                        | `git remote -v` |
| View Tags in the Repository                     | `git tag` |

### Temporary Changes

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Create a Temporary Branch (Stash Changes)       | `git stash` |
| list stack-order of stashed file changes         | `git stash list` |
| write working from top of stash stack           | `git stash pop` |
| Apply Stashed Changes                           | `git stash apply` |
| Discard Stashed Changes                         | `git stash drop` |

### Rollback and Revert

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Rollback to a Previous Commit                   | `git reset --hard <commit_hash>` |
| Revert Changes from a Specific Commit           | `git revert <commit_hash>` |
| Discard Local Changes (Caution: Irreversible)   | `git reset --hard HEAD` |

You can now use these sections in your README or documentation as needed.
