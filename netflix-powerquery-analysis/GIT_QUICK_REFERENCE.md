# Git Quick Reference Card

## Essential Git Commands

### Initial Setup (One Time Only)
```bash
# Configure your identity
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check configuration
git config --list
```

### Starting a Repository

#### New Repository
```bash
git init                          # Initialize new repository
git add .                         # Stage all files
git commit -m "Initial commit"    # First commit
git remote add origin <URL>       # Connect to GitHub
git push -u origin main           # Push to GitHub
```

#### Clone Existing Repository
```bash
git clone <repository-URL>        # Download repository
cd <repository-name>              # Enter directory
```

### Daily Workflow

```bash
# Check status
git status                        # See changed files

# Stage changes
git add <filename>                # Stage specific file
git add .                         # Stage all changes

# Commit changes
git commit -m "Description"       # Commit with message

# Push to GitHub
git push                          # Upload to GitHub

# Pull from GitHub
git pull                          # Download latest changes
```

### Branching

```bash
# Create branch
git branch <branch-name>          # Create new branch
git checkout <branch-name>        # Switch to branch
git checkout -b <branch-name>     # Create and switch

# Merge branch
git checkout main                 # Switch to main
git merge <branch-name>           # Merge branch into main

# Delete branch
git branch -d <branch-name>       # Delete local branch
```

### Viewing History

```bash
git log                           # View commit history
git log --oneline                 # Compact history
git diff                          # See unstaged changes
git diff --staged                 # See staged changes
```

### Undoing Changes

```bash
# Unstage file
git reset <filename>              # Unstage specific file
git reset                         # Unstage all

# Discard changes
git checkout -- <filename>        # Discard file changes
git restore <filename>            # Restore file (newer Git)

# Undo commit (keep changes)
git reset --soft HEAD~1           # Undo last commit

# Undo commit (discard changes)
git reset --hard HEAD~1           # Careful! Loses changes
```

### Remote Operations

```bash
# View remotes
git remote -v                     # List remotes

# Update remote URL
git remote set-url origin <URL>   # Change remote URL

# Fetch updates
git fetch                         # Download without merging
```

---

## Common Scenarios

### Scenario 1: First Upload to GitHub
```bash
cd your-project-folder
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/repo-name.git
git branch -M main
git push -u origin main
```

### Scenario 2: Daily Updates
```bash
git status                        # Check what changed
git add .                         # Stage changes
git commit -m "Update: description of changes"
git push                          # Upload to GitHub
```

### Scenario 3: Sync with GitHub
```bash
git pull                          # Download latest
# Make your changes
git add .
git commit -m "Your changes"
git push
```

### Scenario 4: Made a Mistake
```bash
# Oops, wrong commit message
git commit --amend -m "Correct message"

# Oops, forgot a file
git add forgotten-file.txt
git commit --amend --no-edit

# Oops, want to undo everything
git reset --hard HEAD
```

---

## .gitignore Patterns

```
# Ignore specific file
filename.txt

# Ignore file type
*.log
*.tmp

# Ignore folder
folder_name/
/absolute_path_folder/

# Ignore except
!important.log

# Ignore in all directories
**/debug.log
```

---

## Helpful Tips

### Commit Message Best Practices
```
Add: New feature or file
Update: Changes to existing feature
Fix: Bug fix
Remove: Deleted feature
Docs: Documentation changes
Style: Formatting changes
Refactor: Code restructuring
Test: Adding tests
```

### Check Before Committing
```bash
git status          # What's changed?
git diff            # How did it change?
git add .           # Stage everything
git status          # Verify staging
git commit -m "..."
```

### GitHub Personal Access Token
If password authentication fails:
1. Go to GitHub → Settings → Developer settings
2. Personal access tokens → Generate new token
3. Use token instead of password

---

## Emergency Commands

```bash
# See what you're about to commit
git diff --staged

# Undo last push (DANGEROUS!)
git push --force    # Only if you're sure!

# Recover deleted file
git checkout HEAD -- <filename>

# See all branches
git branch -a

# Delete remote branch
git push origin --delete <branch-name>
```

---

## Quick Troubleshooting

| Problem | Solution |
|---------|----------|
| Can't push | `git pull` first, resolve conflicts, then `git push` |
| Wrong branch | `git checkout main` |
| Large file error | Remove from staging: `git rm --cached <file>` |
| Merge conflict | Edit files, remove markers, `git add .`, `git commit` |
| Forgot to commit | `git add .` then `git commit` |

---

**Remember:** 
- Commit often with clear messages
- Pull before you push
- Use branches for experiments
- Check `git status` frequently

**When in doubt:** `git status` and `git log --oneline` are your friends!
