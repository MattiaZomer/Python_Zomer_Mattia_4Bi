# Esercizio 8 - autenticazione ssh
Ho scelto l'autenticazione ssh per il semplice motivo che sto lavorando da casa perciò è molto più comodo


### ssh -T git@github.com
```bash
Hi MattiaZomer! You've successfully authenticated, but GitHub does not provide shell access.
```

## Cambio di autenticazione
Dal momento che trovo particolarmente scomodo dover inserire ogni volta la mia password per effettuare una sincronizzazione, ho optato per un cambio di approccio: utilizzare l'account github con cui ho effettuato l'accesso su Visual Studio per effettuare l'accesso una volta sola.

Questi sono i comandi che ho utilizzato:

> git config --global credential.helper vscode  
Questo comando mi permette di dire a Git di recuperare le credenziali da VS Code


> git config --global --unset url."https://github.com/".insteadOf  
Questo comando mi permette di "pulire" Git dalle vecchie impostazioni

> git remote set-url origin https://github.com/MattiaZomer/Python_Zomer_Mattia_4Bi.git  
Questo comando permette al git di accedere al repository direttamente tramite HTTPS