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

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        M0_ambiente/recupero.md
```
- git add .\.gitignore
- git add .\M0_ambiente\recupero.md
- git commit -m "feat: rimossi i file come richiesto dall'esercizio 11 ma mantenuti in locale e documentato il processo sul file recupero.md"
- git ls-files .\M0_ambiente\temporanei
```bash
```
- ls .\M0_ambiente\temporanei
```bash
    Directory: C:\Users\tango\Desktop\Programmazione\Compiti\Python_Zomer_Mattia_4Bi\M0_ambiente\temporanei


Mode                 LastWriteTime         Length Name                                                                                                                              
----                 -------------         ------ ----                                                                                                                              
-a----        27/09/2026     23:05              0 lista.txt                                                                                                                         
-a----        27/09/2026     23:05              0 test.md
```

## Come mai .gitignore non agisce sui file già creati
Il file .gitignore non è retroattivo, cioè non va a modificare i vecchi commit eliminando la traccia di determinate modifiche o file. Il file infatti agisce esclusivamente sui file cosiddetti "untracked" ovvero file di cui non sono ancora presenti commit. Perciò se si crea un file, si fa il commit di quest'ultimo e solo DOPO lo si aggiunge nel gitignore, verrà comunque tracciato.