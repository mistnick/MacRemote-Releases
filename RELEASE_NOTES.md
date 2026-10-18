# MacRemote 0.3.0 — Early Access

La versione è definita in `VERSION`. Installare la stessa distribuzione su backend, app e componenti di macchina.

## Contenuto

- App macOS per host e ricevente, menu in topbar, consenso e associazione delle chiavi.
- Servizio di macchina opzionale con LaunchDaemon e agente grafico LoginWindow/Aqua.
- Backend Go, PostgreSQL, Keycloak, coturn e pannello React con viewer WebRTC.
- Unica API `/api`, con access token e operazioni firmate dei dispositivi sotto `/api/agent/`.
- Schema completo per un database applicativo vuoto e bootstrap esplicito del superadmin e dell’azienda iniziale.

## Installazione

Apple Silicon, macOS 14 o successivo. Il DMG contiene l’app. Il PKG del servizio installa anche i componenti di macchina in percorsi fissi. Autorizzare Registrazione schermo e Accessibilità, accedere all’azienda e associare esplicitamente le chiavi dei ricevitori.

Console pubblica: https://mr.kelion.it/admin/. Le credenziali del superadmin vengono consegnate privatamente. Al primo accesso completare cambio password, profilo e configurazione TOTP.

## Stato degli artefatti

App e componenti sono firmati Developer ID. Il PKG privo di firma Installer è indicato con `unsigned` nel nome. La distribuzione non è notarizzata. Il manifest allegato specifica versione, revisione, architettura, checksum e stato delle firme.

Il supporto operativo di LoginWindow, input reale, riavvio e cambio sessione richiede collaudo fisico. Il servizio concede schermo, mouse e tastiera; non audio, clipboard o file. Una transizione login/logout richiede una nuova connessione. FileVault preboot è escluso.

Le evidenze hardware e di capacità rimangono da produrre per questa distribuzione. Una compilazione o una firma non certificano dieci sessioni contemporanee o tutte le combinazioni macOS/browser.
