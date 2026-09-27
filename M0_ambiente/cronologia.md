## git log --oneline --graph --decorate
```bash
* c2b9381 (HEAD -> main, origin/main, origin/HEAD) feat: esercizio 8 e autenticazione finita
* f8fecb9 feat: esercizio 7 gitignore
* 128e1ea docs: aggiunti i file dell'esercizio 6 del modulo m0
* 13c06e0 feat: Esercizio 6 M0
* 8fe4d0a feat!: Esercizio 5
* 8a9dfab feat(configurazione_git.md): fatto esercizio 4
* 25c2b1d docs(esecuzione.md): fatto file per esercizio 3
* ba54680 feat(orario.py): fatto il file Python per l'esercizio numero 3
* 3f7ad15 docs(percorsi.md): aggiunta specificazione nell'esercizio 2
* 52071d6 feat: esercizio 2
* 931adce feat: finito esercizio 1
* 4c98e30 feat: inserito versioni.md
* 5965edc Initial commit
```

## git log -5 --pretty=format:"%h %ad %an %s --date=short"
```bash
c2b9381 Fri Sep 25 02:01:20 2026 +0200 Mattia Zomer feat: esercizio 8 e autenticazione finita --date=short
f8fecb9 Fri Sep 25 01:37:36 2026 +0200 Mattia Zomer feat: esercizio 7 gitignore --date=short
128e1ea Fri Sep 25 01:25:45 2026 +0200 Mattia Zomer docs: aggiunti i file dell'esercizio 6 del modulo m0 --date=short
13c06e0 Fri Sep 25 01:21:34 2026 +0200 Mattia Zomer feat: Esercizio 6 M0 --date=short
8fe4d0a Fri Sep 25 01:11:24 2026 +0200 Mattia Zomer feat!: Esercizio 5 --date=short
```

## commit 8fe4d0a
Questo commit è stato fatto con lo scopo di aggiungere l'esercizio 5 finito. Ho messo un punto esclamativo perché durante lo svoglimento dell'esercizio ho usato un metodo diverso da quello indicato nella consegna per raggiungere prima il risultato richiesto (vedi file es5-comandi.md).

## commit 13c06e0
Questo commit è stato fatto quando ho terminato l'esercizio 6 del modulo M0 ma senza aver scritto la documentazione adeguata

## commit 128e1ea
Questo commit è stato fatto per aggiungere la nuova documentazione dell'esercizio 6 al repository di Github

## commit f8fecb9
Questo commit è stato effettuato per aggiungere al repository i gitignore e i README.md richiesti dall'esercizio 7

## commit c2b9381
Questo commit è stato effettuato per aggiornare la repository aggiungendo ciò che è stato richiesto dall'esercizio 8. La dicitura "autenticazione finita" indica che in quell'esercizio ho effettuato con successo l'autenticazione tramite chiave ssh dalla mia macchina personale a casa

### Perché c'è quella parentesi "(HEAD -> main, origin/main, origin/HEAD)"
#### HEAD -> main
Significa che il lavoro che sto svolgendo in locale viene effettuato sulla base di questo commit

#### origin/main
Indica la posizione del ramo main sul server remoto e significa che questo commit è già presente sulla repository remota

#### origin/HEAD
È il puntatore predefinito del server remoto. Indica che l'etichetta origin/HEAD punta a origin/main