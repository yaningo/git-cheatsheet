# Git Commands Cheatsheet

> Collection of commands for common git operations


#### Undo latest commit
```sh
git reset --soft HEAD^
```

#### Undo the changes of a commit (creating a new commit)
```sh
git revert <commit>
```

#### Undo latest merge (before push)
```sh
git reset --merge ORIG_HEAD
```

#### Merge a branch using the version of the current branch in case of conflicts
```sh
git merge <branch> -s ours
```

#### Discard changes for a particular file after commit
```sh
git reset HEAD <file>
```

#### Unstage the current staged changes
```sh
git reset
```

#### Create, fetch a remote branch and switch to it
```sh
git checkout --track <remote>/<branch>

# Example: git checkout --track origin/feat-awesome
```

#### Remove a file from git but not from disc
```sh
git rm --cached <file>
```

#### Reapply an old commit again
```sh
git cherry-pick <commit>
```

#### Ignore the changes of a file
```sh
git update-index --assume-unchanged <file>

# Undo:
git update-index --no-assume-unchanged <file>
```

#### List all "assume-unchanged" files
```sh
git ls-files -v|grep '^h'
```

#### Display who did the latest change in each line (ignoring whitespaces)
```sh
git blame <filename> -w
```

#### Remove all local branches removed in remote
```sh
git fetch <remote> --prune

# Example: git fetch origin --prune
```

#### Remove untracked local files
```sh
git clean -f
```

#### Remove untracked local files and folders
```sh
git clean -fd
```

#### Remove remote branch
```sh
git push <remote> --delete <branch>

# Example: git push origin --delete feat-awesome
```

#### Go to an old commit
```sh
git read-tree <commit>
```

#### Use the `~/.gitignore` file to ignore globally certain files
```sh
git config --global core.excludesfile '~/.gitignore'
```
