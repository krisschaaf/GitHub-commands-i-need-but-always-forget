# GitHub-commands-i-need-but-always-forget
A collection of all useful GitHub commands i need every now and then.



### Show all commits:
```bash
git log
```

### Edit last unpushed commit:
```bash
git commit --amend
```

### Revert a commit (get the commit ID via `git log`):
```bash
git revert <commit-id>
```

### Uncommit last unpushed commit:
```bash
git reset HEAD^
```

### Remove the last commit from history (but keep content):
```bash
git reset --soft HEAD~1
```

### Remove the last commit from history (don't keep content):
```bash
git reset --hard HEAD~1
```

### Remove from the staging area:
```bash
git restore --staged .
```

### Add to the staging area:
```bash
git add .
```

### Install Git LFS:
1. Install with Homebrew:
   ```bash
   brew install git-lfs
   ```
2. Initialize Git LFS:
   ```bash
   git lfs install
   ```

### Add files to Git LFS (for large files):
1. Track a directory with Git LFS:
   ```bash
   git lfs track <path-to-directory>
   ```
2. Stage and commit the `.gitattributes` file:
   ```bash
   git add .gitattributes
   git commit -m "Add tracking of files..."
   ```

### Add files to Git as well, if already tracked:
1. Add the files:
   ```bash
   git add <files>
   ```
2. Commit and push:
   ```bash
   git commit -m "Add files to LFS"
   git push
   ```
