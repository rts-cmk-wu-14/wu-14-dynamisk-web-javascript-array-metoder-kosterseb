# Git Workflow Documentation

## Project Setup
- Started from the **main branch** of the repository:  
  `https://github.com/rts-cmk-wu-14/wu-14-dynamisk-web-javascript-array-metoder-kosterseb.git`

---

## Branching Strategy
Git branching allows you to work on new features or assignments without affecting the stable `main` branch.  
- **main** → the stable branch where final code is kept.  
- **løste_opgaver** → a feature branch created for solving the assignments.  

Workflow:  
1. Create a new branch from `main`.  
2. Make commits as progress is made.  
3. Push branch to remote repository.  
4. Merge branch back into `main` once work is complete.  
5. Push merged changes to remote `main`.  

---

## Progress & Commits

### Step 1 – Create branch
```bash
git checkout -b løste_opgaver
```
Commit messages:  
- `created branch løste_opgaver`

### Step 2 – Solve assignments one by one with commits/pushes
```bash
git add .
git commit -m "opgave 1 løst"
git push origin løste_opgaver
```
... repeated for each task.  

Commits made:  
- `opgave 1 løst`  
- `opgave 2 løst`  
- `opgave 3 løst`  
- `opgave 4 løst`  
- `opgave 5 løst`  
- `opgave 6 løst`  
- `opgave 7 løst`  
- `opgave 8 løst`  

---

## Step 3 – Merge into main

### Switch back to main branch
```bash
git checkout main
```

### Ensure main is up to date
```bash
git pull origin main
```

### Merge the work from `løste_opgaver`
```bash
git merge løste_opgaver
```
_Output:_  
```
Updating adef973..228ab14
Fast-forward
 arrays.js | 15 +++++++++++++--
 1 file changed, 13 insertions(+), 2 deletions(-)
```

### Push the merged changes to GitHub
```bash
git push origin main
```

---

## Visual Branching Model

```
main ----●-----------------------------● (228ab14)  
          \                          /
           ●--●--●--●--●--●--●--●--● (løste_opgaver)  
            (opgave 1..8 løst)  
```

- Work was developed in the **løste_opgaver** branch.  
- After all assignments were solved, it was merged back into **main**.  
- Final code now exists in `main`.  

---

✅ **Result:** All assignment solutions from `løste_opgaver` are now successfully merged into `main` and pushed to GitHub.  
