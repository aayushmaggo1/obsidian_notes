
## What is Git?

Git is a [[version control system]] - a tool that tracks changes in your project over time.  
Think of it like a timeline of snapshots: every time you [[commit]], you save a snapshot of your project so you can go back, branch off into new ideas, or collaborate safely.

- **Local repo:** Your project on your computer.
    
- **Remote repo:** A shared version of the project (e.g. on GitHub, GitLab).
    
- **Commit:** A saved snapshot of your project’s state.
    
- **Branch:** A separate line of development — like an alternate timeline of your project.
    

---

## Video Tutorial 


![[Git & Github Tutorial]]


## Initial Setup

Run these once on a new system to tell Git who you are:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check your setup:

```bash
git config --list
```

---

## Starting a Repository

Initialize a repo in an existing folder:

```bash
git init
```

Clone an existing repo:

```bash
git clone <url>
```

---

## Tracking Changes

See what’s changed:

```bash
git status
```

Add a file to the staging area:

```bash
git add <file>
```

Add everything:

```bash
git add .
```

Commit your changes:

```bash
git commit -m "Describe your changes"
```

---

## Branching & Merging

Create a new branch:

```bash
git branch <branch-name>
```

Switch branches:

```bash
git checkout <branch-name>
```

Create + switch in one step:

```bash
git checkout -b <branch-name>
```

Merge a branch into the current one:

```bash
git merge <branch-name>
```

---

## Working with Remotes

List connected remotes:

```bash
git remote -v
```

Pull updates from remote:

```bash
git pull
```

Push commits to remote:

```bash
git push origin <branch-name>
```

---

## Undo & Fix

Discard changes in a file:

```bash
git checkout -- <file>
```

Unstage a file:

```bash
git reset <file>
```

Reset to a previous commit (⚠ destructive):

```bash
git reset --hard <commit-hash>
```

---

## Everyday Workflow (Simple)

1. Make changes
    
2. `git status` → see what changed
    
3. `git add .` → stage changes
    
4. `git commit -m "Message"` → save snapshot
    
5. `git push origin main` → upload to remote
    

--------------------------------------------------------------------

## Flows

The flows depict three scenarios - 80/20 , Solo Project and Branching

![[Github Flows]]
