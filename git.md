# git cheatsheet

### Selectively stage changes (interactively)

```
git add -p
```

### See content of stash

```
git stash show -p
```

This shows a diff of what has been stashed compared to `HEAD` at the time of stashing.

### Stash only specific files

```
git stash push -- <pathspec>…
```

If the files are not tracked, add them first using `git add <pathspec>…`.

### Show commit where a file was deleted

```
git log --full-history -1 -- <pathspec>
```

This will show you the git commit message for the last (`-1`) commit where the file `<pathspec>` was touched. If this is a deleted file, it will be the commit where it was deleted.

To show the actual content of the commit in one line, do like this:

```
git show `git log --full-history -1 --pretty=format:"%h" -- <pathspec>`
```

### List files with unmerged changes

```
git diff --name-only --diff-filter=U
```

If your `git status` is way too long and you just want to see the files not yet staged, use this command.
