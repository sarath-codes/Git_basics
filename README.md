# 🧠 **GIT — Detailed Notes**

---

## 🔹 1. What is Git?

**Git** is a **distributed version control system (DVCS)** used to track changes in source code during software development.

It allows multiple developers to work on the same project **simultaneously** without overwriting each other’s changes.

### ✅ Key Points:

* Tracks every change in your codebase.
* Enables collaboration between developers.
* Maintains the history of all modifications.
* Provides tools for **branching**, **merging**, and **rollback**.

---

## 🔹 2. Why Use Git?

| Feature                 | Description                                                        |
| ----------------------- | ------------------------------------------------------------------ |
| **Version Control**     | Keeps track of every version of your files.                        |
| **Collaboration**       | Multiple developers can work together efficiently.                 |
| **Backup**              | Every developer has a complete copy of the repository.             |
| **Branching & Merging** | Experiment with new ideas safely.                                  |
| **Open Source**         | Free and widely supported by tools like GitHub, GitLab, Bitbucket. |

---

## 🔹 3. Git Architecture

Git works mainly with three key areas:

1. **Working Directory** – Where you modify files.
2. **Staging Area (Index)** – Where you mark files to be committed.
3. **Repository (.git folder)** – Where Git stores all committed versions.

---

## 🔹 4. Git Lifecycle

1. **Modified** → File has been changed.
2. **Staged** → File is marked for commit.
3. **Committed** → File is saved to the repository.

---

## 🔹 5. Basic Git Commands

### 🧰 Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

👉 To check configuration for a specific repo:

```bash
git config user.name
```

---

### 🏁 Create or Clone Repositories

```bash
git init              # Create a new Git repo
git clone <url>       # Clone an existing repo
```

---

### 📂 Working with Files

```bash
git status            # Check file status
git add <file>        # Add file to staging area
git add .             # Add all files
git commit -m "message"   # Commit changes
git rm <file>         # Remove file
```

---

### 🔄 Branching and Merging

```bash
git branch                     # List branches
git branch <name>              # Create branch
git checkout <branch>          # Switch branch
git merge <branch>             # Merge branch
git branch -d <branch>         # Delete branch
```

---

### 🌐 Remote Repositories

```bash
git remote -v                  # Show remote URLs
git remote add origin <url>    # Add remote repository
git push -u origin main        # Push to remote
git pull origin main           # Pull latest changes
git fetch origin               # Download updates without merging
```

---

### ⏳ Viewing History

```bash
git log                        # Show commit history
git show <commit-id>           # Show details of a commit
git diff                       # Show unstaged changes
git diff --staged              # Show staged changes
```

---

### 🧹 Undoing Changes

```bash
git restore <file>             # Undo changes in working directory
git reset <file>               # Unstage file
git reset --hard HEAD          # Undo all changes
git revert <commit-id>         # Create new commit that reverses changes
```

---

## 🔹 6. Git Branching Concept

Branches in Git are like **parallel universes** of your project.
Each branch can have its own changes and commits.

### Common Workflow:

* `main` or `master` → Stable version.
* `feature/login` → Feature development.
* `bugfix/error` → Fix specific issues.

Merge completed features back to main.

---

## 🔹 7. GitHub Integration

GitHub is a **cloud-based hosting service** for Git repositories.

### Common Operations:

```bash
git remote add origin https://github.com/user/repo.git
git push -u origin main
git pull origin main
```

---

## 🔹 8. Git Workflow Example

1. **Initialize Repo**

   ```bash
   git init
   ```
2. **Stage and Commit**

   ```bash
   git add .
   git commit -m "Initial commit"
   ```
3. **Add Remote**

   ```bash
   git remote add origin https://github.com/username/repo.git
   ```
4. **Push Code**

   ```bash
   git push -u origin main
   ```

---

## 🔹 9. Git States Overview

| State         | Command      | Description                  |
| ------------- | ------------ | ---------------------------- |
| **Modified**  | `git status` | File changed but not staged. |
| **Staged**    | `git add`    | Ready to commit.             |
| **Committed** | `git commit` | Saved permanently.           |

---

## 🔹 10. Git File Storage (SHA-1 Hash)

Git stores each file and commit using a unique **SHA-1 hash**.
This ensures **integrity** — no data can be changed without changing the hash.

---

## 🔹 11. Git Stash (Temporary Save)

Use stash to save unfinished work temporarily:

```bash
git stash
git stash list
git stash apply
```

---

## 🔹 12. Git Tags

Used to mark **specific commits** (like releases).

```bash
git tag v1.0
git push origin v1.0
```

---

## 🔹 13. Git Merge vs. Rebase

| Merge                    | Rebase                              |
| ------------------------ | ----------------------------------- |
| Combines histories       | Moves commits on top of base branch |
| Preserves branch history | Creates a linear history            |
| Easier and safer         | Cleaner but riskier                 |

---

## 🔹 14. Git Reset vs. Revert

| Command        | Description                                   |
| -------------- | --------------------------------------------- |
| **git reset**  | Removes commits (changes history).            |
| **git revert** | Adds a new commit that undoes changes (safe). |

---

## 🔹 15. Git Best Practices

✅ Use meaningful commit messages
✅ Commit often, but logically
✅ Use `.gitignore` to avoid unnecessary files
✅ Always pull before pushing
✅ Use feature branches
✅ Don’t commit sensitive data (like passwords)

---

## 🔹 16. `.gitignore` Example

```bash
node_modules/
.env
*.log
__pycache__/
.DS_Store
```

---

## 🔹 17. Checking Git Versions & Help

```bash
git --version
git help <command>
```

---

## 🔹 18. Git Hosting Platforms

* **GitHub**
* **GitLab**
* **Bitbucket**
* **Azure Repos**

---

## 🔹 19. Advantages of Git

✅ Distributed architecture (every copy is a full backup)
✅ Fast performance
✅ Secure (SHA-1)
✅ Open-source and free
✅ Works offline

---

## 🔹 20. Common Interview Questions

1. What is the difference between Git and GitHub?
2. What are the three states of a Git file?
3. How does branching work in Git?
4. What is a merge conflict and how to resolve it?
5. Difference between `git pull` and `git fetch`?
6. Explain `git reset` vs. `git revert`.
7. How do you undo the last commit?
8. What’s the use of `.gitignore`?

