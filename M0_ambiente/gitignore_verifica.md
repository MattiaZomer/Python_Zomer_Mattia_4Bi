# Esercizio 7 - .gitignore

### git status
```bash
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        M0_ambiente/test.ipynb

nothing added to commit but untracked files present (use "git add" to track)
```

### git check-ignore -v M0_ambiente/.venv/pyvenv.cfg
```bash
.gitignore:4:.venv/     M0_ambiente/.venv/pyvenv.cfg
```