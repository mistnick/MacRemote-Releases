MacRemote 0.1.3 adds an in-app update checker and download flow, and includes the remote pointer and viewer-startup fixes from 0.1.2.

- The Updates section checks the stable channel in MacRemote-Releases and downloads the matching Apple Silicon DMG.
- The viewer's WebRTC Metal surface forwards pointer, click, and keyboard events to the remote-control handlers.
- A local Screen Recording permission denial no longer blocks startup when the Mac is used as a viewer.
- Apple Silicon, macOS 14 or later.
- Developer ID signed and accepted by Apple notarization; ticket stapled and validated.

Open the DMG and drag MacRemote into Applications. To share a Mac, grant Screen Recording and Accessibility to MacRemote in System Settings > Privacy & Security on that Mac.

Notarization submission: `a0e1f919-e27c-4a84-b05b-1b3a5757942b`.
