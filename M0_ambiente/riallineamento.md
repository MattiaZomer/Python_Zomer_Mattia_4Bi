# Esercizio 12 - Riallineamento
Per questo esercizio partiamo dal git push che ha creato un problema
- git push
```bash
git: 'credential-vscode' is not a git command. See 'git --help'.
To https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
- git pull --no rebase
```bash
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1023 bytes | 146.00 KiB/s, done.
From https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi
   c6f22b2..5603fbd  main       -> origin/main
Merge made by the 'ort' strategy.
 README.md | 4 +++-
 1 file changed, 3 insertions(+), 1 deletion(-)
```
- git push
```bash
git: 'credential-vscode' is not a git command. See 'git --help'.
Enumerating objects: 12, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 24 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 721 bytes | 721.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi.git
   5603fbd..2ed50f0  main -> main
```
- git log --oneline --graph --decorate
```bash
*   2ed50f0 (HEAD -> main, origin/main, origin/HEAD) Merge branch 'main' of https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi
|\  
| * 5603fbd feat(README.md): modificato file README come richiesto dall'esercizio 12
* | c639678 feat(versioni.md): modifica effettuata per rompere git come richiesto dall'es. 12
|/  
* c6f22b2 fix: sistemata imprecisione nella documentazione dell'esercizio 11
```

## Come funziona questa soluzione
La chiave del problema sta nel comando ```git pull --no-rebase```. Questo comando, infatti, permette di ricevere le modifiche effettuate in remoto e di selezionare che modifiche tenere o no, per poi fare un merge, ovvero un unione tra le due versioni (in questo caso, avendo modificato file diversi, git ha fatto il processo automaticamente, senza far scegliere cosa tenere e cosa no in quanto non erano presenti conflitti). Il push che va eseguito dopo serve esclusivamente a portare il merge in remoto.