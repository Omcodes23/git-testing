# Comprehensive Git Commands Cheat Sheet

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git init` | Initializes a new Git repository | `git init` |
| `git clone [url]` | Clones a repository from a URL | `git clone https://github.com/user/repo.git` |
| `git config --global user.name "[name]"` | Sets the user name for commits | `git config --global user.name "John Doe"` |
| `git config --global user.email "[email]"` | Sets the email for commits | `git config --global user.email "john.doe@example.com"` |
| `git add [file]` | Adds a file to the staging area | `git add file.txt` |
| `git add .` | Adds all files to the staging area | `git add .` |
| `git commit -m "[message]"` | Commits the staged changes with a message | `git commit -m "Initial commit"` |
| `git commit --amend` | Modifies the last commit | `git commit --amend -m "Updated commit message"` |
| `git status` | Displays the state of the working directory and staging area | `git status` |
| `git log` | Displays the commit history | `git log` |
| `git log --oneline` | Displays the commit history in a condensed format | `git log --oneline` |
| `git branch` | Lists all branches | `git branch` |
| `git branch [branch-name]` | Creates a new branch | `git branch feature-branch` |
| `git branch -d [branch-name]` | Deletes a branch | `git branch -d feature-branch` |
| `git checkout [branch-name]` | Switches to the specified branch | `git checkout feature-branch` |
| `git checkout -b [branch-name]` | Creates and switches to the specified branch | `git checkout -b feature-branch` |
| `git merge [branch-name]` | Merges the specified branch into the current branch | `git merge feature-branch` |
| `git merge --no-ff [branch-name]` | Merges without fast-forwarding | `git merge --no-ff feature-branch` |
| `git rebase [branch]` | Re-applies commits on top of another base tip | `git rebase main` |
| `git rebase -i [commit]` | Starts an interactive rebase | `git rebase -i HEAD~3` |
| `git fetch [remote]` | Fetches changes from the remote repository | `git fetch origin` |
| `git pull [remote] [branch]` | Fetches and merges changes from the remote branch into the current branch | `git pull origin main` |
| `git push [remote] [branch]` | Pushes the current branch to the remote repository | `git push origin main` |
| `git push -u [remote] [branch]` | Pushes the branch and sets the remote branch as upstream | `git push -u origin main` |
| `git remote -v` | Displays the URLs of remote repositories | `git remote -v` |
| `git remote add [name] [url]` | Adds a new remote repository | `git remote add origin https://github.com/user/repo.git` |
| `git remote set-url [name] [new-url]` | Changes the URL of a remote repository | `git remote set-url origin https://github.com/user/new-repo.git` |
| `git stash` | Stashes the changes in the working directory | `git stash` |
| `git stash apply` | Applies the stashed changes | `git stash apply` |
| `git stash pop` | Applies the stashed changes and removes them from the stash list | `git stash pop` |
| `git stash list` | Lists all stashed changes | `git stash list` |
| `git tag` | Lists all tags | `git tag` |
| `git tag [tag-name]` | Creates a new tag | `git tag v1.0.0` |
| `git tag -d [tag-name]` | Deletes a tag | `git tag -d v1.0.0` |
| `git show [object]` | Displays information about a git object (commit, tag, etc.) | `git show v1.0.0` |
| `git diff` | Shows the differences between the working directory and the index | `git diff` |
| `git diff --staged` | Shows the differences between the index and the last commit | `git diff --staged` |
| `git diff [branch1]..[branch2]` | Shows differences between two branches | `git diff main..feature-branch` |
| `git reset [file]` | Unstages a file while retaining the changes in the working directory | `git reset file.txt` |
| `git reset --soft [commit]` | Moves the branch pointer to a specified commit, preserving the changes in the staging area | `git reset --soft HEAD~1` |
| `git reset --hard [commit]` | Resets the working directory and index to the specified commit | `git reset --hard HEAD~1` |
| `git rm [file]` | Removes a file from the working directory and stages the deletion | `git rm file.txt` |
| `git mv [old-name] [new-name]` | Renames a file and stages the change | `git mv oldname.txt newname.txt` |
| `git cherry-pick [commit]` | Applies changes from a specific commit | `git cherry-pick abc123` |
| `git bisect` | Uses binary search to find the commit that introduced a bug | `git bisect start` |
| `git bisect good [commit]` | Marks a commit as good during a bisect session | `git bisect good abc123` |
| `git bisect bad [commit]` | Marks a commit as bad during a bisect session | `git bisect bad def456` |
| `git blame [file]` | Shows who modified each line of a file | `git blame file.txt` |
| `git grep [pattern]` | Searches for a pattern in the repository | `git grep "search term"` |
| `git revert [commit]` | Reverts a commit by creating a new commit | `git revert abc123` |
| `git clean -f` | Removes untracked files from the working directory | `git clean -f` |
| `git reflog` | Shows the history of the reference logs | `git reflog` |
| `git archive` | Creates an archive of files from a named tree | `git archive -o latest.zip HEAD` |
| `git gc` | Runs a garbage collection to optimize the repository | `git gc` |
| `git fsck` | Verifies the integrity of the repository | `git fsck` |
| `git worktree` | Manages multiple working trees | `git worktree add ../branch-name branch-name` |
| `git submodule add [url] [path]` | Adds a new submodule | `git submodule add https://github.com/user/repo.git submodule/path` |
| `git submodule update --init --recursive` | Initializes, updates, and clones all submodules | `git submodule update --init --recursive` |
| `git submodule foreach [command]` | Executes a command in each submodule | `git submodule foreach 'git checkout main'` |
| `git tag -a [tag-name] -m "[message]"` | Creates an annotated tag | `git tag -a v1.0.0 -m "Initial release"` |
| `git tag -s [tag-name] -m "[message]"` | Creates a signed tag | `git tag -s v1.0.0 -m "Signed release"` |
| `git describe [object]` | Describes a commit using the most recent tag reachable from it | `git describe HEAD` |
| `git ls-files` | Lists all files in the index | `git ls-files` |
| `git ls-tree [tree-ish]` | Lists the contents of a tree object | `git ls-tree HEAD` |
| `git cat-file -p [object]` | Displays the content of a git object | `git cat-file -p HEAD^{tree}` |
| `git hash-object -w [file]` | Computes and stores the object ID for a file | `git hash-object -w file.txt` |
| `git show-ref` | Displays references in the repository | `git show-ref` |
| `git symbolic-ref [name] [ref]` | Sets a symbolic ref | `git symbolic-ref HEAD refs/heads/main` |
| `git update-index --assume-unchanged [file]` | Ignores changes to a file temporarily | `git update-index --assume-unchanged file.txt` |
| `git update-ref -d [ref]` | Deletes a reference | `git update-ref -d refs/heads/feature-branch` |

For more detailed usage, you can refer to the official [Git documentation](https://git-scm.com/docs) 
