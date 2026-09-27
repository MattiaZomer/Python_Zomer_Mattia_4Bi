# Esercizio 11
## Sequenza dei comandi
- git add ./M0_ambiente/temporanei
- git commit -m "feat: file temporanei dell'esercizio 11"  
> aggiunto M0_ambiente/temporanei/ al .gitignore
- git ls-files M0_ambiente/temporanei
```bash
M0_ambiente/temporanei/lista.txt
M0_ambiente/temporanei/test.md
```
- git rm -r --cached M0_ambiente/temporanei
```bash
rm M0_ambiente/temporanei/lista.txt
rm M0_ambiente/temporanei/test.md
```
- git ls-files M0_ambiente/temporanei
```bash
```
- git status
```bash
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    M0_ambiente/temporanei/lista.txt
        deleted:    M0_ambiente/temporanei/test.md
```
- git commit -m "feat: rimossi i file come richiesto dall'esercizio 11 ma mantenuti in locale e documentato il processo sul file recupero.md"