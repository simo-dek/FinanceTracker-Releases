# FinanceTracker — Download e aggiornamenti

Questo repository contiene esclusivamente pacchetti Windows/macOS e feed di aggiornamento.

## Installazione

Scarica il pacchetto per il tuo sistema dalla pagina [Releases](https://github.com/simo-dek/FinanceTracker-Releases/releases).

- **Windows x64:** esegui il file `-Setup.exe`. Per aggiornare una copia già installata non occorre disinstallarla.
- **Mac:** estrai lo ZIP e copia l’app in Applicazioni. La disponibilità del pacchetto Mac dipende dal completamento della firma e della notarizzazione.

Le versioni dotate di aggiornamenti integrati controllano automaticamente le nuove uscite.
Puoi anche usare **Impostazioni → Aggiornamenti → Controlla aggiornamenti**.
Il download e l’installazione richiedono la scelta dell’utente. Non serve un account GitHub.

I documenti Excel devono essere conservati fuori dalla cartella del programma.

## Verifica degli aggiornamenti

Gli aggiornamenti sono firmati Ed25519 e verificati dall’app prima dell’installazione.
Le chiavi private di firma e le credenziali di pubblicazione non sono contenute qui.
I manifest SHA-256 sono allegati ai pacchetti.

Feed separati consentono di pubblicare Windows e Mac in momenti diversi:

- `appcast-windows.xml`
- `appcast-macos.xml`

La presenza dei feed non indica che sia già disponibile un pacchetto: consultare le Releases.
