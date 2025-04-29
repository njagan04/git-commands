<div align = "center">
  <a href="[https://medium.com/@jykroo](https://medium.com/@jykroo/git-command-reference-guide-a-complete-beginner-to-advanced-cheatsheet-df017fd1e8db)" target="_blank" style="margin-right: 50px;">
    <img src="https://img.shields.io/static/v1?message=Click%20Here%20to%20find%20it%20in%20Medium%20!!&logo=M&label=&color=12100E&logoColor=white&labelColor=&style=for-the-badge" height="40" alt="medium logo" style="vertical-align: top;" />
  </a>
</div>

## 🌱 **Repository Setup**
- **Initialize a repository : Initializes a new Git repository in the current directory.**

```bash
git init
```

- **Clone an existing repository:**
```bash
git clone <repository-url>
```


## 🔗 **Remote Repository Management**
- **Add a remote repository : Links your local repo to a remote GitHub repository.**
```bash
git remote add origin <repository-url>
```

- **View configured remotes:**
```bash
git remote -v
```

- **Remove a remote:**
```bash
git remote remove <remote-name>
```

- **Rename a remote:**
```bash
git remote rename <old-name> <new-name>
```

##
## 📂 **Staging & Committing Changes**
- **Check status of files : Shows current changes (staged, unstaged, untracked).**
```bash
git status
```
- **Stage specific file(s):**
```bash
git add <file-name>
```

- **Stage all changes:**
```bash
git add .
```

- **Unstage a file (keep changes):**
```bash
git reset HEAD <file-name>
```

- **Commit changes with a message:**
```bash
git commit -m "Commit message"
```

- **Amend the last commit (optional message change):**
```bash
git commit --amend
```

##
## 🌿 **Branching**
### **Create & Manage Branches**
- **List all branches:**
```bash
git branch
```

- **Create a new branch:**
```bash
git branch <branch-name>
```

- **Create and switch to a new branch:**
```bash
git checkout -b <branch-name>
```

- **Switch to an existing branch:**
```bash
git checkout <branch-name>
```

- **Delete a local branch:**
```bash
git branch -d <branch-name>
```

- **Force delete a local branch:**
```bash
git branch -D <branch-name>
```

- **Rename current branch:**
```bash
git branch -m <new-branch-name>
```

### **Working with Remote Branches**
- **Push a branch to remote:**
```bash
git push origin <branch-name>
```

- **Pull a specific branch:**
```bash
git pull origin <branch-name>
```

- **Fetch all remote branches:**
```bash
git fetch
```

- **Delete a remote branch:**
```bash
git push origin --delete <branch-name>
```

- **Track a remote branch:**
```bash
git checkout -b <branch-name> origin/<branch-name>
```

##
## 🔀 **Merging & Rebasing**
### **Merging**
- **Merge a branch into the current branch:**
```bash
git merge <branch-name>
```

- **Resolve conflicts (after editing conflicted files):**
```bash
git add <resolved-file>
git commit -m "Resolved merge conflict"
```

- **Abort a merge:**
```bash
git merge --abort
```

- **Delete the branch locally :**
Use -d to delete only if it's fully merged
Use -D to force delete if it's not merged (use with caution)
```bash
git branch -d <feature-xyz>
```

- **Delete the branch remotely (if pushed to GitHub): **
```bash
git push origin --delete feature-xyz
```
### **Rebasing**
- **Rebase current branch onto another branch:**
```bash
git rebase <branch-name>
```

- **Abort a rebase:**
```bash
git rebase --abort
```

- **Continue rebase after resolving conflicts:**
```bash
git rebase --continue
```

##
## 🚀 **Pushing & Pulling**
- **Push to the remote repository (current branch):**
```bash
git push origin <branch-name>
```

- **Push with upstream tracking (first-time push):**
```bash
git push --set-upstream origin <branch-name>
```

- **Pull latest changes:**
```bash
git pull origin <branch-name>
```

- **Fetch changes without merging:**
```bash
git fetch
```

- **Force push (use cautiously):**
```bash
git push --force
```

##
## 🕒 **History & Logs**
- **View commit history:**
```bash
git log
```

- **Concise commit history:**
```bash
git log --oneline
```

- **View commit history for a specific file:**
```bash
git log <file-name>
```

- **View branch history (graph):**
```bash
git log --oneline --graph --decorate --all
```

##
## 🔄 **Undoing Changes**
- **Discard changes to a file:**
```bash
git checkout -- <file-name>
```

- **Undo last commit (keep changes):**
```bash
git reset --soft HEAD~1
```

- **Undo last commit and discard changes:**
```bash
git reset --hard HEAD~1
```

- **Revert a specific commit:**
```bash
git revert <commit-hash>
```

- **Reset to a specific commit:**
```bash
git reset --hard <commit-hash>
```

##
## 🏷️ **Tags**
- **Create an annotated tag:**
```bash
git tag -a <tag-name> -m "Tag message"
```

- **List all tags:**
```bash
git tag
```

- **Push tags to remote:**
```bash
git push origin --tags
```

- **Delete a tag:**
```bash
git tag -d <tag-name>
```

- **Delete remote tag:**
```bash
git push origin :refs/tags/<tag-name>
```

##
## 📄 **.gitignore**
- **Create/Edit `.gitignore`:**
Prevents specified files/folders from being tracked.
```plaintext
node_modules/
*.log
.env
```

- **Remove a tracked file while keeping it locally:**
```bash
git rm --cached <file-name>
```

##
## 📦 **Git Large File Storage (LFS)**
- **Track large files:**
```bash
git lfs track "<file-path>"
```

- **Check tracked LFS files:**
```bash
git lfs ls-files
```

- **Push LFS-tracked files:**
```bash
git add .gitattributes
git add <file-path>
git commit -m "Track large file with LFS"
git push origin <branch-name>
```

##
## 🔧 **Miscellaneous**
- **Check current configuration:**
```bash
git config --list
```

- **Check remote repository URL:**
```bash
git remote show origin
```

- **Stash changes (temporarily save):**
```bash
git stash
```

- **List stashed changes:**
```bash
git stash list
```

- **Apply stashed changes:**
```bash
git stash apply
```

- **Clear all stashed changes:**
```bash
git stash clear
```
