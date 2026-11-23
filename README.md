# FinanceTracker

FinanceTracker gestisce spese, entrate, investimenti e saldi in un documento Excel sul tuo OneDrive. La dashboard mostra i risultati del mese selezionato e il riepilogo annuale.

## Download e installazione

Scarica gli allegati dalla pagina [Release ufficiali](https://github.com/simo-dek/FinanceTracker-Releases/releases). Puoi scaricarli senza un account GitHub.

**Windows x64.** Apri la release Windows più recente ed esegui il file che termina in `-Setup.exe`. Per la versione portatile scarica lo ZIP, scegli **Estrai tutto** e avvia `finance_tracker.exe` dalla cartella estratta. Conserva insieme l’eseguibile e gli altri file. Per mantenere l’installazione portatile, aggiorna manualmente lo ZIP.

**Mac.** Al momento manca un pacchetto pubblico installabile su altri Mac. Quando sarà disponibile, scegli la release macOS, verifica lo ZIP come descritto sotto, estrailo e trascina l’app in **Applicazioni**. La build attuale richiede macOS 14 o successivo e include Intel e Apple Silicon. Rimuovere la quarantena non autorizza un Mac a eseguire una build limitata a un dispositivo. Lascia attivo Gatekeeper. Se macOS segnala un’app danneggiata o potenzialmente pericolosa, interrompi l’apertura e controlla la provenienza del download.

**iPhone.** Se hai già l’app installata, puoi seguire le istruzioni OneDrive qui sotto. La navigazione mobile comprende la gestione dei movimenti e delle categorie. La schermata Patrimonio è disponibile su desktop.

## Verificare download e aggiornamenti

Scarica dalla stessa release anche il file `-SHA256SUMS.txt`. Su Windows apri PowerShell nella cartella dei download ed esegui `Get-FileHash -Algorithm SHA256 "nome-del-pacchetto"`, sostituendo il nome completo dello ZIP o dell’installer. Confronta il risultato con la riga corrispondente nel file dei checksum. Su Mac apri Terminale nella cartella dei due file ed esegui `shasum -a 256 -c "nome-del-file-SHA256SUMS.txt"`. Il risultato atteso per lo ZIP è `OK`. Se il valore è diverso, scarica nuovamente il pacchetto dalla release ufficiale.

Da **Impostazioni → Aggiornamenti → Controlla aggiornamenti** puoi cercare nuove versioni per la tua piattaforma. L’app verifica la firma Ed25519 degli aggiornamenti e ti chiede di avviare l’installazione. Su Windows l’aggiornamento integrato installa l’app nella posizione standard anche se parti da una copia portatile.

## Primo avvio e accesso a OneDrive

1. Premi **Collega Excel da OneDrive**. Accedi nella pagina Microsoft con l’account che può leggere e modificare il documento. La password viene inserita nella pagina Microsoft.
2. Per iniziare da zero, scegli **Crea nuovo**, indica cartella e nome e attendi la conferma. Riceverai un file con il modello mensile, il mese corrente e il riepilogo annuale. Se hai già un file creato con il modello FinanceTracker, seleziona il suo `.xlsx`. Un foglio Excel generico può avere un layout incompatibile.
3. Al successivo avvio ritrovi il documento collegato. Da **Impostazioni**, premi sul nome per aprirlo in Excel Online. Al primo utilizzo incolla il suo indirizzo web. Puoi correggerlo con l’icona del collegamento.

La lettura e il salvataggio richiedono una connessione a OneDrive. Per condividere soltanto l’app, invia il link a queste release. L’accesso al documento finanziario dipende dalle autorizzazioni che assegni separatamente su OneDrive.

## Registrare e consultare i movimenti

- **Mesi e dashboard.** Seleziona mese e anno per consultare totali, grafici e dettagli per categoria. I nuovi mesi utilizzano il modello del documento. Il foglio base e il riepilogo annuale sono distinti dai fogli dei singoli mesi.
- **Movimenti.** Inserisci tipo, importo, categoria, descrizione e periodo. Usa ricerca e filtri per ritrovare una voce, modificarla o eliminarla. Cambiando il periodo di un movimento esistente lo sposti nel mese scelto. Quando il mese manca, l’app lo prepara durante il salvataggio.
- **Entrate e investimenti.** Le entrate sono raggruppate in FAM ed EXTRA. Controlla il gruppo quando aggiungi una categoria. Gli investimenti hanno una classificazione dedicata.
- **Tag.** Puoi assegnare un tag alle spese e consultare i movimenti associati dalla pagina Tag. Se l’app segnala che il documento Tag richiede un aggiornamento dopo il salvataggio della spesa, riprova dalla pagina Tag.
- **Patrimonio.** Sul desktop puoi leggere e aggiornare i saldi delle voci patrimoniali del mese. Ordine e raggruppamenti seguono il foglio Excel selezionato.
- **Risultati.** I riepiloghi usano i risultati delle formule disponibili nel documento. La dicitura **Calcolato dai mesi** indica che l’app ha ricostruito il valore annuale dai mesi presenti. Excel può ricalcolare le formule all’apertura.

## Categorie e copie di sicurezza

Apri **Categorie** (su iPhone **Gestisci categorie Excel**) per aggiungere, rinominare o rimuovere una categoria. Le modifiche riguardano i mesi esistenti e il modello per quelli futuri. Prima della modifica l’app crea e verifica una copia del documento nella sottocartella **Backup categorie** accanto all’originale su OneDrive. Se la verifica fallisce, l’operazione si ferma.

Per rimuovere una categoria già utilizzata, scegli dove trasferire i movimenti e controlla il riepilogo prima della conferma. Puoi impostare una destinazione comune o assegnarla movimento per movimento. Se rimuovi Investimenti, le voci trasferite vengono riclassificate come spese.

## Salvataggi, conflitti e recupero

Il file Excel collegato è la fonte dei dati. Attendi la conferma del salvataggio prima di chiudere l’app. Su iPhone puoi continuare a navigare mentre il banner indica che OneDrive sta salvando. In caso di errore si riapre il movimento con i dati inseriti.

Se il documento è cambiato in Excel o su un altro dispositivo, l’app ferma la scrittura per proteggere le modifiche già presenti. Salva e chiudi il file in Excel, scegli **Rileggi Excel**, controlla i valori aggiornati e riprova. Se Microsoft richiede di accedere nuovamente, usa lo stesso account e verifica di avere ancora accesso al file. Prima di reinserire un movimento dopo un’interruzione, controlla se è già presente.
