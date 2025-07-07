# 🧰 Git Cheat Sheet

A comprehensive and well-organized Git command reference for beginners and professionals. Includes essential commands, examples, explanations, and advanced workflows.

---

## 📁 Setup & Configuration

```bash
git config --global user.name "Nidhal Labri"
git config --global user.email "your.email@example.com"
git config --global color.ui auto
git config --global credential.helper cache
git config --global core.editor "code --wait"   # Example: VSCode as editor
git config --list       # View current config
```

---

## 📦 Repository Initialization & Cloning

```bash
git init                             # Initialize a new Git repo
git clone <url>                      # Clone existing repo
git clone <url> <directory>          # Clone into specific dir
git clone -b <branch> <url>          # Clone specific branch
git clone --recursive <url>          # Clone repo with submodules
```

---

## 🗂️ File Tracking & Staging

```bash
git status                           # Show file changes
git add <file>                       # Stage single file
git add .                            # Stage all files
git add -p                           # Selectively stage changes
git reset <file>                     # Unstage a file
git rm <file>                        # Remove tracked file
git mv <old> <new>                   # Rename/move file
```

---

## 💾 Committing Changes

```bash
git commit -m "message"              # Commit staged files
git commit -a -m "message"           # Add & commit tracked files
git commit                           # Open editor to commit
git commit --amend                   # Modify last commit
```

---

## 🌿 Branching

```bash
git branch                           # List branches
git branch <name>                    # Create new branch
git checkout <name>                  # Switch to branch
git checkout -b <name>               # Create & switch
git branch -d <name>                 # Delete local branch (safe)
git branch -D <name>                 # Force delete
git branch -m <old> <new>            # Rename branch
```

---

## 🔀 Merging & Rebasing

```bash
git merge <branch>                  # Merge into current
git merge --no-ff <branch>          # Merge with commit
git rebase <branch>                 # Reapply commits on base
git rebase -i HEAD~3                # Interactive rebase last 3
git rebase --abort                  # Abort rebase
git rebase --continue               # Continue after conflict
```

---

## 🌎 Remote Repositories

```bash
git remote -v                        # List remotes
git remote add origin <url>         # Add new remote
git remote show origin              # Show remote details
git remote rename old new           # Rename remote
```

---

## 📤 Push & 📥 Pull

```bash
git push                             # Push current branch
git push origin <branch>             # Push specific branch
git push -u origin <branch>          # Set upstream
git push --delete origin <branch>    # Delete remote branch

git pull                             # Fetch + merge
git fetch                            # Only fetch
git fetch origin                     # Fetch from origin
git merge origin/<branch>            # Merge fetched branch
```

---

## 🧾 Logs & History

```bash
git log                              # Show commit log
git log --oneline                    # Compact view
git log --graph --all --oneline      # All branches as graph
git log --stat                       # Show changes in commits
git log --follow <file>              # History of a file
git show <commit>                    # Show a commit’s diff
```

---

## 📊 Differences & Comparison

```bash
git diff                             # Unstaged vs working dir
git diff --staged                    # Staged vs last commit
git diff <branch1> <branch2>         # Compare branches
git diff <branch1> <branch2> <file>  # Compare file in branches
```

---

## 🧺 Stashing

```bash
git stash                            # Stash changes
git stash -u                         # Include untracked
git stash --all                      # Include ignored files
git stash list                       # Show stash list
git stash apply                      # Reapply top stash
git stash pop                        # Apply and drop
git stash drop                       # Drop top stash
git stash clear                      # Remove all stashes
git stash branch <branch>            # Create branch from stash
```

---

## ⏪ Undo & Reset

```bash
git reset HEAD <file>                # Unstage a file
git reset --hard HEAD                # Discard all changes
git reset --soft HEAD~1              # Uncommit but keep changes
git revert <commit>                  # Revert a commit safely
git checkout -- <file>               # Discard changes to file
git clean -fd                        # Delete untracked files
```

---

## 🏷️ Tags

```bash
git tag                              # List tags
git tag -a v1.0 -m "Message"         # Annotated tag
git tag -d v1.0                      # Delete local tag
git push origin v1.0                 # Push tag
git push origin --tags               # Push all tags
git push origin :refs/tags/v1.0      # Delete remote tag
```

---

## 🔍 Advanced: Bisect, Blame, Submodules

```bash
git blame <file>                     # Who changed what
git bisect start                     # Start binary search
git bisect good <commit>             # Mark good commit
git bisect bad <commit>              # Mark bad commit
git bisect reset                     # Stop bisect

git submodule add <url> <dir>        # Add submodule
git submodule update                 # Update submodules
```

---

## 🛠️ Useful Aliases

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.last 'log -1 HEAD'
```

---

## 🧠 Concepts & Glossary

| Term       | Description |
|------------|-------------|
| **HEAD**   | Current branch ref |
| **Origin** | Default remote name |
| **Master/Main** | Default branch name |
| **Staging Area** | Index where changes go before commit |
| **Tracked** | Files Git is tracking |
| **Untracked** | Files not yet added to Git |
| **Rebase** | Replay commits on another base |
| **Stash** | Temp storage for unfinished changes |
| **Commit** | A snapshot of your changes |
| **Branch** | Pointer to a specific commit |
| **Tag** | A marker for a specific commit |

---

## ⚠️ Notes

- Avoid `--force` pushing (`git push -f`) unless necessary.
- Never rewrite public history unless you are the only contributor.
- Prefer `git pull --rebase` for cleaner history when collaborating.

---

## 🧠 Contributions
Contributions, corrections, and improvements are welcome.  
Feel free to open a pull request or create an issue!

---

**Made with 💻 by Nidhal** | **[LinkedIn](https://www.linkedin.com/in/nidhal-labri/)**
