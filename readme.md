# Question 1 - Project Initialization & First Push

## Objective
Set up a new Git project and push it to a remote repository.

---

## Step 1: Create a New Project Folder

```bash
mkdir githerovired
cd githerovired
```

---

## Step 2: Initialize Git Repository

```bash
git init
```

This command creates a new local Git repository.

---

## Step 3: Create `app.py`

```bash
touch app.py
```

Add sample Python code inside `app.py`:

```python
print("Hello, Herovired Git!")
```

---

## Step 4: Check Git Status

```bash
git status
```

This shows:
- Untracked files
- Modified files
- Staged files

---

## Step 5: Stage the File

```bash
git add app.py
```

---

## Step 6: Commit Changes

```bash
git commit -m "First Commit Herovired"
```

---

## Step 7: Create Remote Repository

Create a new repository on GitHub.

Sample repository name:

```text
githerovired
```

---

## Step 8: Add Remote Origin

```bash
git remote add origin https://github.com/sjoshigit/githerovired.git
```

---

## Step 9: Verify Remote Configuration

```bash
git remote -v
```

Example output:

```bash
origin  https://github.com/sjoshigit/githerovired.git (fetch)
origin  https://github.com/sjoshigit/githerovired.git (push)
```

---

## Step 10: Push Code to Remote Repository

Rename branch to `main`:

```bash
git branch -M main
```

Push repository:

```bash
git push -u origin main
```

---

# Question 2 - Working with Changes & History

## Objective
Track code changes and manage commit history properly.

---

## Step 1: Modify `app.py`

Update file:

```python
print("Hello, Herovired Git!")

def hello(name):
    print(f"Hello, {name}")
```

---

## Step 2: Check Changes Before Staging

```bash
git status
```

---

## Step 3: View Differences

```bash
git diff
```

This shows line-by-line changes before staging.

---

## Step 4: Stage Specific Changes

```bash
git add -p
```

This allows staging selected changes interactively.

OR stage full file:

```bash
git add app.py
```

---

## Step 5: Commit Changes

```bash
git commit -m "Added hello function"
```

---

## Step 6: Make Another Change

Add another function:

```python
def add(a, b):
    return a + b
```

---

## Step 7: Stage All Changes

```bash
git add .
```

---

## Step 8: Commit Again

```bash
git commit -m "Added add function"
```

---

## Step 9: View Full Commit History

```bash
git log
```

---

## Step 10: View Compact One-Line History

```bash
git log --oneline
```

Example:

```bash
wxysabc Added add function
wxysabb Added hello function
```

---

# Question 3 - Branching & Feature Development

## Objective
Work with branches and manage feature development.

---

## Step 1: Create a New Branch

```bash
git branch feature-update
```

---

## Step 2: Switch to the New Branch

```bash
git checkout feature-update
```

OR:

```bash
git switch feature-update
```

---

## Step 3: Modify `app.py`

Add feature code:

```python
def multiply(a, b):
    return a * b
```

---

## Step 4: Stage and Commit Changes

```bash
git add app.py
git commit -m "Added multiply feature"
```

---

## Step 5: Switch Back to Main Branch

```bash
git checkout main
```

---

## Step 6: Merge Feature Branch into Main

```bash
git merge feature-update
```

---

## Step 7: Verify Changes are Merged

Check commit history:

```bash
git log --oneline
```

Check file content:

```bash
cat app.py
```

---

## Step 8: Delete Branch Safely

```bash
git branch -d feature-update
```

---

## Step 9: Force Delete a Dummy Branch

Create dummy branch:

```bash
git branch dummy-branch
```

Force delete:

```bash
git branch -D dummy-branch
```

---

# Question 4 - Handling Errors (Stash, Reset, Revert)

## Objective
Learn how to manage mistakes and unfinished work.

---

## Step 1: Make Changes Without Commit

Example:

```python
print("Temporary changes")
```

---

## Step 2: Stash Changes Including Untracked Files

```bash
git stash -u
```

---

## Step 3: Check Stash List

```bash
git stash list
```

Example:

```bash
stash@{0}: WIP on main
```

---

## Step 4: Apply Stashed Changes Back

```bash
git stash apply
```

---

## Step 5: Commit the Changes

```bash
git add .
git commit -m "Applied stashed changes"
```

---

## Step 6: Make Another Commit with Incorrect Code

```bash
git add .
git commit -m "Added incorrect code"
```

---

## Step 7: Undo Last Commit Using Reset

### Soft Reset

Keeps changes in working directory:

```bash
git reset --soft HEAD~1
```

### Hard Reset

Deletes commit and changes permanently:

```bash
git reset --hard HEAD~1
```

---

## Step 8: Make Another Commit

```bash
git add .
git commit -m "Added corrected code"
```

---

## Step 9: Undo Commit Using Revert

```bash
git revert HEAD
```

This creates a new commit that reverses previous changes.

---

## Step 10: Verify Commit History

```bash
git log --oneline
```

---

# Author

Git Herovired Practice Assignment README File.