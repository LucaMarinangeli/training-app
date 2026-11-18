# Training

App personale per gli allenamenti: schede, timer guidato con suoni e voce, storico con calendario e progressione, peso corporeo. Tutta in italiano, installabile sul telefono come una normale app.

**App online: https://lucamarinangeli.github.io/training-app/**

## Come installarla sul telefono (Android)

1. Apri il link qui sopra in Chrome.
2. Tocca i tre puntini in alto a destra.
3. Scegli **Installa app** (oppure **Aggiungi a schermata Home**).

L'app si apre a schermo intero e funziona anche senza connessione.

## Cosa c'è dentro

- **Home:** prossimo allenamento, sequenza Upper A, Corsa, Upper B, Atletica, Upper C, Lower e riepilogo della settimana.
- **Allenamento:** serie con kg e reps, timer guidato con recuperi, spunte per l'atletica.
- **Storico:** calendario, progressione dei carichi, progressione del ritmo di corsa, esportazione in CSV.
- **Scheda:** schede modificabili. Si tocca la matita, si cambiano i valori e si riclicca la matita per salvare.
- **Corpo:** peso corporeo nel tempo.

## Dove sono salvati i dati

I dati restano nel browser del telefono (localStorage), legati all'indirizzo del sito. Aggiornare i file dell'app non li cancella. Li perdi se cancelli i dati del sito da Chrome o disinstalli l'app senza averli esportati, quindi ogni tanto usa **Esporta CSV** nello Storico.

## Backup automatico su GitHub (facoltativo)

In fondo alla scheda Storico c'è la sezione **Backup automatico su GitHub**. Con un token personale, l'app aggiorna il file `backup/allenamenti.csv` in questo repository circa 8 secondi dopo ogni modifica.

1. Su GitHub apri Settings, Developer settings, Personal access tokens, Fine-grained tokens, Generate new token.
2. In **Repository access** scegli **Only select repositories** e seleziona `training-app`.
3. In **Permissions**, **Repository permissions**, imposta **Contents** su **Read and write**.
4. Copia il token e incollalo nel campo dell'app, sul telefono. Non scriverlo mai nel codice né nel repository.

Il token resta solo nel telefono. Il repository è pubblico, quindi anche il CSV di backup è leggibile da chiunque abbia il link.

## File del repository

| File | A cosa serve |
| --- | --- |
| `index.html` | L'app completa (pagina, stile e codice in un solo file) |
| `manifest.json` | Nome, colori e icone per l'installazione |
| `sw.js` | Service worker per l'uso offline |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Icone dell'app |

## Come aggiornare l'app

1. Apri `https://github.com/LucaMarinangeli/training-app/upload/main`.
2. Clicca **choose your files** e seleziona il nuovo `index.html` (e gli altri file solo se sono cambiati). Controlla che i nomi non abbiano una cartella davanti.
3. Scegli **Commit directly to the main branch** e premi **Commit changes**.
4. Dopo circa un minuto il sito è aggiornato. Sul telefono chiudi e riapri l'app due volte per vedere la versione nuova.

Il sito è pubblicato con GitHub Pages dal ramo `main`, cartella radice.
