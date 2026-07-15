# Git
git-Basic




# Git Basics for Developers & ==DevOps==

Git is a version control system used to track code changes.

---

# 1. ==Clone==
====
Used to download a repository from GitHub/GitLab.

## Command

```
git clone https://github.com/user/project.git
```

## Example

```
git clone https://github.com/spring-projects/spring-petclinic.git
```

This creates a local copy.

---

# 2. Commit

A commit saves changes into Git history.

## Step-by-Step

### Check Changes

```
git status
```

### Add Files

```
git add file.txt
```

Add all files:

```
git add .
```

### Commit

```
git commit -m "Added login feature"
```

---

# 3. Branch

Branches allow parallel development.

## Create Branch

```
git branch feature-login
```

## Switch Branch

```
git checkout feature-login
```

## Create + Switch Together

```
git checkout -b feature-login
```

## View Branches

```
git branch
```

Current branch shows:

```
* main
```

---

# 4. Merge

Merge combines one branch into another.

## Example Workflow

### Switch to Main

```
git checkout main
```

### Merge Feature Branch

```
git merge feature-login
```

---

# Merge Conflict

Happens when same lines changed in two branches.

Example:

```
<<<<<<< HEAD
Hello Main=======
Hello Feature
>>>>>>> feature-login
```

Fix manually, then:

```
git add .git commit
```

---

# 5. Pull Request (PR)

Pull Request = request to merge code into main branch.

Mostly used in:

- GitHub
- GitLab
- Bitbucket

## Typical Flow

```
1. Create branch
2. Make changes
3. Commit
4. Push branch
5. Create Pull Request
6. Code review
7. Merge
```

## Push Branch

```
git push origin feature-login
```

Then create PR in GitHub UI.

---

# 6. Rebase Basics

Rebase moves your branch on top of another branch.

Used for cleaner Git history.

---

## Example

### Before Rebase

```
main:A---B---C
feature:     D---E
```

### After Rebase

```
A---B---C---D---E
```

---

## Rebase Command

```
git checkout feature-login
git rebase main
```

---

# Merge vs Rebase

|Merge|Rebase|
|---|---|
|Keeps history|Cleaner history|
|Creates merge commit|No merge commit|
|Safer for beginners|Requires care|
|Good for teams|Good for clean commits|

---

# Useful Git Commands

## Pull Latest Changes

```
git pull
```

## Push Changes

```
git push
```

## Commit History

```
git log
```

Compact:

```
git log --oneline
```

---

# Complete Real Workflow

```
# Clone repo
git clone URL

# Enter project
cd project

# Create branch
git checkout -b feature-auth

# Make changes
# Add changes
git add .

# Commit
git commit -m "Added auth module"

# Push branch
git push origin feature-auth
# Create Pull Request
```

---

# Important DevOps Git Commands

```
git clone

git status

git add

git commit

git push

git pull

git branch

git checkout

git merge

git rebase

git log

git stash
```

---

# Beginner Practice

## Create Repository

```
mkdir git-practice
cd git-practice
git init
```

## Create File

```
touch app.txt
```

## Add Content

```
echo "hello" > app.txt
```

## Commit

```
git add .
git commit -m "first commit"
```


---
checkout vs switch
git strategy -TBD
git merge vs pull
git pull vs fetch
git rebase vs git merge
