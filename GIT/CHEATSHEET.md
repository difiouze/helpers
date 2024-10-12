# Git Cheatsheet

##### Configuring Git
- `git config --global user.name "[name]"`
  - Set the name that will be associated with your commits.
  
- `git config --global user.email "[email]"`
  - Set the email that will be associated with your commits.
  
- `git config --global alias.[alias] [command]`
  - Create a shortcut for a Git command (e.g., `git log --graph --oneline`).
  
- `git config --global core.editor [editor]`
  - Set the default text editor for commit messages (e.g., `vi`).
  
- `git config --global --edit`
  - Open the global config file in a text editor for manual editing.
---
##### Initializing and Cloning
- `git init`
  - Initialize an empty Git repository in the current directory.
  
- `git init [directory]`
  - Create an empty Git repository in the specified directory.
  
- `git clone [url]`
  - Clone a remote Git repository from the URL into a local directory.
  
- `git clone [url] [directory]`
  - Clone a remote Git repository into the specified local directory.
---
##### Examining Logs
- `git log`
  - Show the commit history for the current branch.
  
- `git log --stat`
  - Show file stats (files changed, insertions, deletions) for each commit.
  
- `git log --oneline`
  - Show a condensed summary of commits in one line each.
  
- `git log --graph --decorate`
  - Draw a best-guess graph of commits with branch names.
  
- `git diff`
  - Show unstaged file differences compared to the current index.
  
- `git diff --cached`
  - Show differences between staged changes and the last commit.
  
- `git show [commit1] [commit2]`
  - Show changes between two commits.
  
- `git show [commit]`
  - Show changes made in the specified commit.
---
##### Versioning Files
- `git add [file]`
  - Stage file changes to be committed.
  
- `git commit -m "[message]"`
  - Commit the staged snapshot with a commit message.
  
- `git rm [file]`
  - Remove a file from the staging index and working directory.
  
- `git mv [file] [newpath]`
  - Move or rename a file in Git and stage the change.
---
##### Branching and Merging
- `git branch`
  - List all the branches in the current repository.
  
- `git branch [branch]`
  - Create a new branch with the name `[branch]`.
  
- `git checkout [branch]`
  - Switch to the current branch `[branch]`.
  
- `git checkout -b [branch]`
  - Create a new branch and switch to it.
  
- `git merge [branch]`
  - Merge the history of `[branch]` into the current branch.
  
- `git branch -d [branch]`
  - Delete the local branch `[branch]`.
---
##### Retrieving and Updating Repositories
- `git fetch [remote]`
  - Fetch branches and commits from the remote repository.
  
- `git pull [remote]`
  - Fetch remote changes and directly merge them into the local repository.
  
- `git pull --rebase [remote]`
  - Fetch remote changes and rebase onto the local branch.
  
- `git push [remote] [branch]`
  - Push the local branch to the remote repository.
  
- `git push --all [remote]`
  - Push all local branches to the remote repository.
  
- `git push --tags [remote]`
  - Push all local tags to the remote repository.
---
##### Rewriting Git History
- `git rebase [branch]`
  - Rebase the current branch onto `[branch]`.
  
- `git rebase -i [commit]`
  - Interactively rebase the current branch onto `[commit]`.
  
- `git reflog`
  - Show the history of Git commands for the current repository.
  
- `git reset --hard [commit]`
  - Clear the staging area and rewrite the working tree from the specified commit.
---
##### Remote Repositories
- `git remote add [name] [url]`
  - Create a remote connection with a URL and alias `[name]`.
  
- `git fetch [remote]`
  - Fetch all branches from the remote repository.
  
- `git pull [remote]`
  - Fetch remote changes and merge them into the local repository.
  
- `git push [remote] [branch]`
  - Push the local branch to the remote repository.
---
##### Undoing Changes
- `git reset [file]`
  - Remove the file from the staging index but leave it unchanged locally.
  
- `git clean -n`
  - Show which files would be removed from the working directory. Use `-f` to execute clean.
  
- `git revert [commit]`
  - Undo changes from the specified commit by creating a new commit.
