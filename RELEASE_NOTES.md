# MacRemote 0.3.1

Questa versione risolve il blocco di Gatekeeper durante l'apertura su macOS.

- App firmata con Developer ID, notarizzata da Apple e ticket applicato al bundle.
- DMG firmato, notarizzato e con ticket applicato.
- Verifica locale completata: Gatekeeper accetta app e DMG.
- Distribuito solo l'app DMG; il pacchetto del servizio privilegiato non è incluso in questa versione.

Requisiti: Apple Silicon, macOS 14 o successivo. La convalida fisica di LoginWindow, input, riavvio e matrice hardware resta separata dalla verifica di firma e notarizzazione.
