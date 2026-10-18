# MacRemote 0.2.0 — Early Access

## Novità

- Introduzione del backend amministrativo con API v2, migrazioni PostgreSQL, pannello React/TypeScript, inventario, deleghe, storico e telemetria.
- Viewer WebRTC integrato nel pannello, verifica delle chiavi, controllo remoto e riconnessione esplicita.
- Servizio di macchina opzionale con identità propria, LaunchDaemon e agente grafico LoginWindow/Aqua. Configurazione con autorizzazione amministrativa locale e selezione esplicita dei ricevitori consentiti.
- Comandi per stato, permessi e interruzione del servizio nell'app e nella barra dei menu.
- Pacchetto dedicato con percorsi fissi e istruzioni per attivazione, aggiornamento e rimozione.

## Installazione e aggiornamento

Apple Silicon, macOS 14 o successivo. Aggiornare il backend alla revisione di questa release **prima** di attivare il servizio di macchina.

- `MacRemote-0.2.0-arm64.dmg`: applicazione client. Aprire il DMG e copiare MacRemote in Applicazioni.
- `MacRemote-HostService-0.2.0-arm64-unsigned.pkg`: installazione opzionale dell'app e dei componenti di macchina. Usare questo pacchetto per aggiornare un Mac su cui il servizio è già installato.
- Seguire la guida del servizio allegata. I permessi Registrazione schermo e Accessibilità dell'agente vanno concessi separatamente da quelli dell'app principale.
- Prima di logout o riavvio, associare e verificare la nuova identità del servizio con una connessione locale di prova.

## Stato di verifica e limiti

Questa è una versione **Early Access per collaudo**, non una certificazione di supporto pubblico. L'app è firmata Developer ID; l'installer PKG non è firmato e gli artefatti 0.2.0 non sono notarizzati.

Sono passati 21 test Swift, test backend PostgreSQL con race detector, build TypeScript/Vite, build Docker e verifiche statiche di firma, plist e pacchetto. Non sono stati eseguiti installazione, logout, riavvio o controllo fisico della schermata di login con questa revisione. Le evidenze hardware e di rete obbligatorie per la produzione rimangono pendenti; non vengono sostituite dalla build o dalla firma.

Il servizio di macchina concede schermo, mouse e tastiera. Audio, clipboard e file restano fuori dai permessi del servizio. Login, logout e cambio utente richiedono una nuova connessione. I permessi macOS non vengono aggirati. La schermata preboot FileVault non viene condivisa.

Il backend amministrativo e il viewer web restano in fase pilota: il piano completo di MFA, gestione Keycloak, isolamento database e compatibilità browser/hardware richiede ancora completamento e collaudo. Questa release non dichiara supporto Catalina, Intel, Universal o dieci sessioni certificate.

## Correzione del canale e pubblicazione del backend

Il flag GitHub `prerelease` originariamente impostato impediva alla 0.1.5 di trovare la 0.2.0. La 0.2.0 viene ora offerta sul canale usato dal client esistente, mantenendo espliciti i limiti Early Access e la mancata notarizzazione. Il controllo di pubblicazione verifica selezione della release e URL di download.

Il nuovo backend viene pubblicato su `https://mr.kelion.it`, con console `https://mr.kelion.it/admin/`. La procedura aggiorna proxy, callback OIDC e scope Keycloak `basic`, `roles` e `api-audience`; la prova completa effettua login, letture autorizzate, controllo CSRF e logout con un account temporaneo poi eliminato. L'account `macremote-admin` richiede cambio password e configurazione TOTP; le credenziali sono conservate soltanto in un file locale privato.

Build applicazione: `dae5873c8349caba448c3048f7fd906e2943b4f0`. Backend pubblico: revisione `eb33971` o successiva, verificabile su `/healthz`.
