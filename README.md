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

### Metodo 1 — Estensione temporanea (sviluppo)

1. Clonare il repository o scaricare il codice sorgente
2. Aprire Thunderbird e digitare `about:debugging` nella barra degli indirizzi
3. Fare clic su **Questo Thunderbird** nella barra laterale
4. Fare clic su **Carica componente aggiuntivo temporaneo...**
5. Selezionare il file `manifest.json` nella cartella del progetto

> **Nota:** l'estensione temporanea viene rimossa al riavvio di Thunderbird.

### Metodo 2 — Pacchetto .xpi (installazione permanente)

1. Dalla cartella del progetto, creare il pacchetto:
   ```bash
   zip -r thunderpec-ng.xpi manifest.json src/ _locales/ icons/ -x ".*"
   ```
2. Aprire Thunderbird e andare su **Strumenti → Componenti aggiuntivi e temi**
3. Fare clic sull'icona ingranaggio (⚙) e selezionare **Installa componente aggiuntivo da file...**
4. Selezionare il file `thunderpec-ng.xpi` appena creato
5. Confermare l'installazione quando richiesto

Dopo l'installazione, la voce **ThunderPEC-ng** apparirà nel menu **Strumenti** di Thunderbird.

### Debug

Per visualizzare i log e gli errori dell'estensione, aprire la console degli errori con `Ctrl+Shift+J` (o **Strumenti → Console degli errori per sviluppatori**).

## Licenza

[LGPL-3.0](lgpl-3.0.txt) — Vedi [NOTICE](NOTICE) per le attribuzioni di copyright.

Questo progetto è una riscrittura dell'estensione ThunderPEC originale (v1.9.1) di thunderpec (pseudonimo).
