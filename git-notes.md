# Git Commands

## Configuration & Setup

### User Configuration
- `git config --global user.name "Your Name"` - Set your name
- `git config --global user.email "your.email@example.com"` - Set your email
- `git config --list` - Show all Git configurations

### Repository Initialization
- `git init` - Initialize new Git repository in current folder
- `git clone <repository-url>` - Copy remote repository to local
- `git clone https://github.com/username/repo.git` - Clone from GitHub

## Status & Information

### Checking Status
- `git status` - Show working directory status
- `git log` - Show commit history
- `git log --oneline` - Compact commit history
- `git log --graph --oneline` - Visual branch history
- `git show <commit-id>` - Show changes in specific commit

### Remote Repositories
- `git remote -v` - List remote repositories
- `git remote add origin <url>` - Add remote repository
- `git remote remove origin` - Remove remote repository

## Staging & Committing

### Staging Changes
- `git add <filename>` - Stage specific file
- `git add .` - Stage all changes in current directory
- `git add -A` - Stage all changes (including deletions)
- `git reset <filename>` - Unstage specific file

### Committing Changes
- `git commit -m "Commit message"` - Commit with message
- `git commit -am "Message"` - Add and commit tracked files
- `git commit --amend` - Modify last commit

## Pushing & Pulling

### Pushing to Remote
- `git push origin main` - Push to main branch
- `git push -u origin main` - Push and set upstream
- `git push origin <branch-name>` - Push specific branch

### Pulling from Remote
- `git pull origin main` - Pull latest from main branch
- `git fetch` - Download changes without merging
- `git fetch origin` - Fetch from remote

## Branching & Merging

### Branch Operations
- `git branch` - List all branches
- `git branch <branch-name>` - Create new branch
- `git checkout <branch-name>` - Switch to branch
- `git checkout -b <branch-name>` - Create and switch to new branch
- `git branch -d <branch-name>` - Delete branch
- `git branch -D <branch-name>` - Force delete branch

### Merging
- `git merge <branch-name>` - Merge branch into current branch
- `git merge --no-ff <branch-name>` - Merge with commit (no fast-forward)

## Undoing Changes

### Reset & Revert
- `git restore <file>` - Discard unstaged changes in file
- `git restore --staged <file>` - Unstage file
- `git reset --soft HEAD~1` - Undo commit but keep changes staged
- `git reset --hard HEAD~1` - Undo commit and discard changes
- `git revert <commit-id>` - Create new commit that undoes changes

### Stash (Temporary Storage)
- `git stash` - Save uncommitted changes temporarily
- `git stash pop` - Restore stashed changes
- `git stash list` - List all stashes
- `git stash clear` - Remove all stashes

## GitHub Specific

### Common GitHub Workflow
1. `git pull origin main` - Get latest changes
2. Make your changes
3. `git add .` - Stage changes
4. `git commit -m "Description"` - Commit changes
5. `git push origin main` - Push to GitHub

### Fork & Contribution
- Fork on GitHub website first
- `git clone your-fork-url`
- Add upstream: `git remote add upstream original-repo-url`
- Sync fork: `git fetch upstream`, `git merge upstream/main`

## File Management

### .gitignore
- Create `.gitignore` file to exclude files (keys, logs, binaries)
- Common entries: `*.pem`, `node_modules/`, `.env`, `*.log`

### Comparing Changes
- `git diff` - Show unstaged changes
- `git diff --staged` - Show staged changes
- `git diff HEAD` - Show all changes since last commit

## Project Structure Best Practices

### Commit Messages
- Use present tense: "Add feature" not "Added feature"
- First line: Short summary (50 chars max)
- Second line: Blank
- Third line: Detailed explanation

### Branch Naming
- `feature/login-page`
- `bugfix/header-overlap`
- `hotfix/critical-error`
- `docs/update-readme`

## Daily Workflow Example
```bash
mkdir new-project
cd new-project
git init
cat >> git-notes.md << 'EOF'
git pull origin main          # Get latest
git add .
git commit -m "Initial commit"
git push -u origin main
EOF
```
