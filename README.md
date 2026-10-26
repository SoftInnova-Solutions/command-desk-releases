# CommandDesk

App per Mac di SoftInnova: salva i comandi da terminale, li lancia con un clic e mostra con un LED quali processi sono vivi. Qui ci sono solo le versioni pubblicate; il codice sta in un repository privato.

Serve un Mac con chip Apple (M1 o successivi).

## Installazione (la prima volta)

1. Scarica **[CommandDesk.dmg](https://github.com/SoftInnova-Solutions/command-desk-releases/releases/latest/download/CommandDesk.dmg)**.
2. Apri il file scaricato e trascina **CommandDesk** sulla cartella **Applicazioni**.
3. Apri CommandDesk da Applicazioni. macOS lo blocca: l'app è firmata da SoftInnova ma non è notarizzata da Apple. È normale e succede solo questa volta. Chiudi l'avviso.

   ![Avviso di macOS alla prima apertura](docs/apri-comunque-1.png)

4. Apri **Impostazioni di Sistema → Privacy e sicurezza**, scorri fino a **Sicurezza** e premi **Apri comunque** accanto a CommandDesk. Conferma con la password del Mac o con Touch ID.

   ![Il pulsante «Apri comunque» in Privacy e sicurezza](docs/apri-comunque-2.png)

5. Nella finestra che compare premi di nuovo **Apri comunque**.

   ![La conferma finale](docs/apri-comunque-3.png)

Il pulsante «Apri comunque» resta disponibile per circa un'ora dopo il tentativo di apertura: se non lo trovi, riprova ad aprire CommandDesk e torna in Privacy e sicurezza.

## Aggiornamenti

CommandDesk controlla da sola se c'è una versione nuova (all'avvio e ogni 6 ore) e la scarica in silenzio. Quando è pronta, in fondo alla finestra compare **«0.x.y pronta · Aggiorna»**:

- **Aggiorna e riavvia** la installa subito, dopo averti mostrato cosa verrà fermato;
- altrimenti si installa da sola la prossima volta che esci con **⌘Q**.

Non serve riscaricare il DMG e non serve più «Apri comunque». CommandDesk non si riavvia mai senza che tu lo chieda. Un clic sul numero di versione mostra le novità.

## Primo avvio

Il catalogo è vuoto. Se un collega ti ha mandato un file `.commanddesk`, importalo con **Importa file…**: arrivano i comandi, mai utenti, chiavi o password.

## Se qualcosa non va

- Se «Apri comunque» non compare, in Terminale, solo per la copia scaricata da qui:
  `xattr -dr com.apple.quarantine /Applications/CommandDesk.app`
  poi riapri l'app.
- Per tutto il resto scrivi a Pasquale.
