# Esercizio 13 - Guida

## Procedimento ESEGUITO SU POWERSHELL
### 1 Installazione del necessario
- `winget install --id Microsoft.VisualStudioCode --exact` 
- `winget install --id Git.Git --exact`
- `code --version `
- `git --version`
- `code --install-extension ms-python.python` 
- `code --install-extension ms-toolsai.jupyter`
- **codice per testare**
    - `mkdir $HOME\Documents\prova-ambiente`
    - `cd $HOME\Documents\prova-ambiente`
    - `'print("Ambiente pronto:", 4 * 21)' | Out-File -Encoding utf8 -FilePath verifica.py`
    - `py verifica.py`
    - **OUTPUT ATTESO DELL'ULTIMA RIGA:**
    ```bash
    Ambiente pronto: 84
    ```

### 2 Configurazione di git
- `git config --global user.name "NomeCognome"`
- `git config --global user.email "nome.cognome@marconirovereto.it"`
- `git config --global init.defaultBranch main `
- `git config --global core.editor "code --wait"`
- **codice per testare**
    - `git config --list --show-origin`
    - **OUTPUT ATTESO (per ora non importa il parametro remote.origin.url):**
    ```bash
    file:C:/Program Files/Git/etc/gitconfig diff.astextplain.textconv=astextplain
    file:C:/Program Files/Git/etc/gitconfig filter.lfs.clean=git-lfs clean -- %f
    file:C:/Program Files/Git/etc/gitconfig filter.lfs.smudge=git-lfs smudge -- %f
    file:C:/Program Files/Git/etc/gitconfig filter.lfs.process=git-lfs filter-process
    file:C:/Program Files/Git/etc/gitconfig filter.lfs.required=true
    file:C:/Program Files/Git/etc/gitconfig http.sslbackend=schannel
    file:C:/Program Files/Git/etc/gitconfig core.autocrlf=true
    file:C:/Program Files/Git/etc/gitconfig core.fscache=true
    file:C:/Program Files/Git/etc/gitconfig core.symlinks=false
    file:C:/Program Files/Git/etc/gitconfig pull.rebase=false
    file:C:/Program Files/Git/etc/gitconfig credential.helper=manager
    file:C:/Program Files/Git/etc/gitconfig credential.https://dev.azure.com.usehttppath=true
    file:C:/Program Files/Git/etc/gitconfig init.defaultbranch=main
    file:$HOME/.gitconfig  core.editor="$HOME\AppData\Local\Programs\Microsoft VS Code\bin\code" --wait
    file:$HOME/.gitconfig  user.name=Nome Cognome
    file:$HOME/.gitconfig  user.email=nome.cognome@marconirovereto.it
    file:$HOME/.gitconfig  credential.helper=vscode
    file:.git/config        core.repositoryformatversion=0
    file:.git/config        core.filemode=false
    file:.git/config        core.bare=false
    file:.git/config        core.logallrefupdates=true
    file:.git/config        core.symlinks=false
    file:.git/config        core.ignorecase=true
    file:.git/config        remote.origin.url=
    file:.git/config        remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
    file:.git/config        branch.main.remote=origin
    file:.git/config        branch.main.merge=refs/heads/main
    file:.git/config        branch.main.vscode-merge-base=origin/main
    ```

### 3 Accesso a Github con HTTPS - procedimento spiegato, da non scrivere sul prompt dei comandi
**In questo repository ho impostato inizialmente la chiave ssh ma per via del fatto che questa è una guida su come cinfigurare una postazione lavorativa e non una postazione personale è meglio adottare l'accesso tramite HTTPS**
- Su GitHub aprire Settings, quindi Developer settings, quindi Personal access tokens e Fine-grained tokens, infine Generate new token.
- Assegnare un nome riconoscibile, impostare una scadenza compatibile con l'anno scolasti‐co, limitare l'accesso al solo repository del corso e concedere il permesso Contents in lettura e scrittura, che è il minimo necessario per inviare commit.
- Copiare il token al momento della generazione: GitHub lo mostra una volta sola e non è più recuperabile in seguito.
- Al primo git push verso un remoto HTTPS, Windows apre la finestra del gestore di credenziali. Inserire il nome utente GitHub e il token al posto della password. Il gestore lo memorizza e non lo richiede più.

### 4 Github e repository
- **andare su github e creare una nuova repository chiamata lab-info-4bi-cognome (senza aggiungere file README o .gitignore iniziali)**
- `cd $HOME\Documents\`
- `git clone https://github.com/NomeCognome/lab-info-4bi-cognome.git`
- `cd $HOME\Documents\`
- `git clone https://github.com/NomeCognome/lab-info-4bi-cognome.git`
- `cd .\lab-info-4bi-cognome\`
- `ni README.md`
- `mkdir M0_ambiente`
- `ni .\M0_ambiente\.gitkeep .\M0_ambiente\README.md`
- `mkdir M1_markdown_jupyter`
- `ni .\M1_markdown_jupyter\.gitkeep .\M1_markdown_jupyter\README.md`
- `mkdir M2_basi_python`
- `ni .\M2_basi_python\.gitkeep .\M2_basi_python\README.md`
- `mkdir M3_strutture_python`
- `ni .\M3_strutture_python\.gitkeep .\M3_strutture_python\README.md`
- `mkdir M4_funzioni_moduli`
- `ni .\M4_funzioni_moduli\.gitkeep .\M4_funzioni_moduli\README.md`
- `mkdir M5_gestione_file`
- `ni .\M5_gestione_file\.gitkeep .\M5_gestione_file\README.md`
- `mkdir M6_oop_python`
- `ni .\M6_oop_python\.gitkeep .\M6_oop_python\README.md`
- `mkdir M8_concorrenza_rete`
- `ni .\M8_concorrenza_rete\.gitkeep .\M8_concorrenza_rete\README.md`
- `git add -A`
- `git commit -m "feat: setup e primo commit"`
- **codice per controllare**
    - `tree /f`
    - **OUTPUT ATTESO:** 
    ```bash
    lab-info-4bi-cognome
     ├───M0_ambiente  
     │   ├───.gitkeep
     │   └───README.md
     ├───M1_markdown_jupyter 
     │   ├───.gitkeep
     │   └───README.md 
     ├───M2_basi_python
     │   ├───.gitkeep
     │   └───README.md 
     ├───M3_strutture_python
     │   ├───.gitkeep
     │   └───README.md  
     ├───M4_funzioni_moduli
     │   ├───.gitkeep
     │   └───README.md 
     ├───M5_gestione_file
     │   ├───.gitkeep
     │   └───README.md 
     ├───M6_oop_python
     │   ├───.gitkeep
     │   └───README.md 
     ├───M8_concorrenza_rete
     │   ├───.gitkeep
     │   └───README.md
     └───README.md
    ```

### 5 .gitignore
- `ni .\.gitignore`
- **incollare dentro il file appena creato questo codice**:
```text
__pycache__/
*.pyc

.venv/
venv/

.ipynb_checkpoints/

Thumbs.db
desktop.ini
*.tmp
```
- **comandi per testare**
    - `ni testtemporanei.tmp`
    - `git status`
    - `git check-ignore -v M0_ambiente\testtemporanei.tmp`
    - **OUTPUT ATTESO:**
        - git status non elenca testtemporanei.tmp
        - git check-ignore restituisce: `.gitignore:10:*.tmp    M0_ambiente\testtemporanei.tmp`

### 6 Gestione degli errori frequenti
#### py: Termine 'py' non riconosciuto come nome di cmdlet, funzione, file di script o programma eseguibile.
- **Causa:** Il terminale PowerShell è stato aperto prima del completamento dell'installazione e non ha ancora caricato la variabile d'ambiente `PATH` aggiornata, oppure Python non è stato aggiunto al percorso di ricerca durante l'installazione.
- **Rimedio:** Chiudere e riaprire la finestra del terminale; se il problema persiste, ripetere l'installazione assicurandosi di aggiungere Python al `PATH`[cite: 2].

#### fatal: not a git repository (or any of the parent directories): .git
- **Causa:** Si sta tentando di eseguire un comando Git all'interno di una cartella che non è configurata come repository Git
- **Rimedio:** Verificare la posizione corrente con `Get-Location` e spostarsi nella cartella del repository con il comando `cd <percorso>`.

#### Author identity unknown. Please tell me who you are.
- **Causa:** Manca la configurazione dell'identità dell'utente (`user.name` o `user.email`) obbligatoria per registrare i commit.
- **Rimedio:** Eseguire i comandi `git config --global user.name "NomeCognome"` e `git config --global user.email "nome.cognome@marconirovereto.it"` per poi riprovare a fare il commit.

#### fatal: refusing to merge unrelated histories
- **Causa:** Si è creato il repository su GitHub con un file iniziale e in locale con `git init`: esistono due storie indipendenti. 
- **Rimedio:** Il modo pulito di evitarlo è creare il repository remoto vuoto, come indicato nella procedura.