#  Git Practice Repository

A hands-on Git and GitHub practice project demonstrating how to create a repository locally, connect it to GitHub, manage branches, resolve merge conflicts, and work with pull requests.

---

##  Repository Purpose

This repository was created to practice essential **Git** and **GitHub** workflows commonly used in real-world software development.

The project covers:

 Creating a local Git repository  
 Connecting local code to GitHub  
 Pushing code to a remote repository  
 Working with branches  
 Feature-based development  
 Pull requests and merging  
 Merge conflict resolution  
 Managing commits and repository history

---

##  Technologies Used

| Technology | Purpose |
|------------|---------|
| Git | Version control system |
| GitHub | Remote repository hosting |
| HTML | Sample practice files |
| Terminal / CLI | Running Git commands |

---

##  Repository Structure

```text
git-practice/
│── .gitignore
│── home.html
│── index.html
│── notes.txt
│── payment.txt
```

### Explanation of Files

#### `.gitignore`
Contains files/folders that Git should ignore and not track.

Example:

```gitignore
node_modules/
.env
```

---

#### `home.html`
Practice HTML file created to simulate a webpage structure.

Purpose:
- Learning file tracking in Git
- Practicing commits

---

#### `index.html`
Main HTML file used during branching and merge conflict resolution practice.

Purpose:
- Understanding Git tracking
- Conflict resolution practice

---

#### `notes.txt`
Contains notes and updates created locally.

Purpose:
- Testing file modification tracking
- Commit practice

---

#### `payment.txt`
Created inside a feature branch (`feature-payment`) to simulate feature development.

Purpose:
- Learning feature branch workflow
- Merge pull request practice

---

#  Git Workflow Followed

## Step 1: Create Project Locally

Create a local folder:

```bash
mkdir git-practice
cd git-practice
```

---

## Step 2: Initialize Git Repository

Initialize Git in the local project.

```bash
git init
```

This creates a hidden `.git` folder that tracks project changes.

---

## Step 3: Create Project Files

Create sample files:

```bash
touch index.html
touch home.html
touch notes.txt
```

Verify files:

```bash
ls
```

---

## Step 4: Check Git Status

Check untracked files:

```bash
git status
```

Expected output:

```text
Untracked files:
index.html
home.html
notes.txt
```

---

## Step 5: Add Files to Staging Area

Add files to Git staging:

```bash
git add .
```

Verify:

```bash
git status
```

Expected:

```text
Changes to be committed
```

---

## Step 6: Commit Files

Save changes permanently.

```bash
git commit -m "Initial commit"
```

This creates the first snapshot of the project.

---

## Step 7: Create GitHub Repository

Create a new repository in GitHub:

Repository Name:

```text
git-practice
```

Keep it:

- Public Repository
- Without README initially
- Without .gitignore
- Without license

---

## Step 8: Connect Local Repository to GitHub

Add GitHub repository URL.

```bash
git remote add origin https://github.com/your-username/git-practice.git
```

Verify remote:

```bash
git remote -v
```

Expected:

```text
origin  https://github.com/your-username/git-practice.git (fetch)
origin  https://github.com/your-username/git-practice.git (push)
```

---

## Step 9: Rename Branch to Main

Rename default branch:

```bash
git branch -M main
```

---

## Step 10: Push Local Code to GitHub

Push repository:

```bash
git push -u origin main
```

Explanation:

| Command | Purpose |
|----------|----------|
| `push` | Upload code |
| `-u` | Set upstream branch |
| `origin` | Remote repository |
| `main` | Branch name |

---

#  Branching Workflow

Branching allows independent feature development.

---

## Create Feature Branch

Create a new branch:

```bash
git checkout -b feature-payment
```

Verify branch:

```bash
git branch
```

Expected:

```text
main
* feature-payment
```

---

## Add Payment Feature

Create payment feature file:

```bash
touch payment.txt
```

Stage changes:

```bash
git add .
```

Commit:

```bash
git commit -m "Add payment feature branch"
```

---

## Push Feature Branch to GitHub

```bash
git push origin feature-payment
```

This uploads the branch to GitHub.

---

#  Pull Request Workflow

After pushing a feature branch:

1. Open GitHub repository
2. Click **Compare & Pull Request**
3. Review changes
4. Add description
5. Click **Create Pull Request**
6. Merge into `main`

Example merge message:

```text
Merge pull request #1 from praveen-coded/feature-payment
```

---

#  Merge Conflict Resolution

This repository also demonstrates conflict resolution.

A merge conflict happens when:

- Same file edited in multiple branches
- Git cannot decide which change to keep

Example conflict file:

```text
index.html
```

---

## Resolve Conflict

Pull latest changes:

```bash
git pull origin main
```

Open conflicted file.

Example:

```html
<<<<<<< HEAD
<h1>Main branch</h1>
=======
<h1>Feature branch</h1>
>>>>>>> feature-payment
```

Manually fix:

```html
<h1>Main + Feature branch</h1>
```

Then stage and commit:

```bash
git add .
git commit -m "Conflict resolved"
git push origin main
```

---

#  Git Commands Used in This Project

## Repository Commands

```bash
git init
git status
git add .
git commit -m "message"
```

---

## Branch Commands

```bash
git branch
git checkout -b feature-payment
git switch main
```

---

## Remote Repository Commands

```bash
git remote add origin URL
git remote -v
git push -u origin main
git pull origin main
```

---

## Merge Commands

```bash
git merge branch-name
```

Example:

```bash
git merge feature-payment
```

---

#  Key Concepts Learned

### 1. Version Control
Git helps track project history and revert changes.

### 2. Staging Area
Temporary place before commit.

```bash
git add .
```

---

### 3. Commit
A saved snapshot of project changes.

```bash
git commit -m "message"
```

---

### 4. Branching
Allows independent development without affecting main code.

---

### 5. Pull Requests
Used for reviewing and merging code safely.

---

### 6. Merge Conflicts
Occurs when multiple changes happen in same file.

Git requires manual resolution.

---

# 📈 Repository Learning Outcomes

After completing this repository practice, I learned:

- How to initialize a Git repository
- How to connect local project to GitHub
- How to push local code to remote repository
- How to create feature branches
- How to commit changes
- How pull requests work
- How to resolve merge conflicts
- Git collaboration workflow

---

# Repository Snapshot

Repository includes:

- **12 commits**
- **2 branches**
- Feature branch merge
- Conflict resolution
- Local-to-GitHub project deployment

---

# Author

**Praveen Kumar Chitirala**

GitHub Username:

```text
praveen-coded
```

---

##  Support

If you found this repository useful for learning Git and GitHub basics, feel free to star the repository.

Happy Coding !
