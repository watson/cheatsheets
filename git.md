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
