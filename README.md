# ThunderPEC-ng

Estensione per Thunderbird per la gestione semplificata della Posta Elettronica Certificata (PEC).

## Funzionalità

- **Apertura busta PEC** — Visualizza direttamente il messaggio originale contenuto nella busta di trasporto PEC
- **Gestione notifiche** — Collega automaticamente le ricevute (accettazione, consegna, mancata consegna) al messaggio originale con vista riassuntiva "Stato del messaggio"
- **Filtri rapidi** — Separa messaggi PEC dalle notifiche con filtri dedicati
- **Archiviazione** — Salva messaggio e relative ricevute in un file ZIP
- **Gestione account PEC** — Abilita/disabilita ThunderPEC selettivamente per singolo account, con supporto per i principali gestori PEC italiani

## Compatibilità

- **Target:** Thunderbird 140 ESR+ (Manifest V3)
- **Versione legacy:** Il branch [`legacy`](../../tree/legacy) contiene il codice originale v1.9.1 dell'estensione originale non più sviluppata (Thunderbird 3.0-60.x)

## Stato del progetto

Riscrittura in corso da estensione legacy XUL/XPCOM a moderna MailExtension.

## Installazione per sviluppo / test

**Requisiti:** Thunderbird 128 ESR o superiore.

1. Clonare il repository o scaricare il codice sorgente
2. Aprire Thunderbird e andare su **Strumenti → Componenti aggiuntivi e temi** (oppure digitare `about:addons` nella barra degli indirizzi)
3. Fare clic sull'icona ingranaggio (⚙) in alto a destra e selezionare **Installa componente aggiuntivo da file...**
4. Selezionare il file `manifest.json` nella cartella del progetto
5. Confermare l'installazione quando richiesto

Dopo l'installazione, la voce **ThunderPEC-ng** apparirà nel menu **Strumenti** di Thunderbird.

### Debug

Per visualizzare i log e gli errori dell'estensione, aprire la console degli errori con `Ctrl+Shift+J` (o **Strumenti → Console degli errori per sviluppatori**).

## Licenza

[LGPL-3.0](lgpl-3.0.txt)
