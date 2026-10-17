MacRemote 0.1.4 adds a macOS Settings window and fixes remote pointer and keyboard event routing.

- The application menu now opens Settings for connection, remote-control, and update options.
- Pointer hit testing now converts window coordinates to the remote desktop view's local coordinates, so clicks and movement reach the control surface reliably.
- Keyboard shortcuts send both key-down and key-up events to avoid stuck keys.
- Apple Silicon; macOS 14 or later.
- Developer ID signed and accepted by Apple notarization; ticket stapled and validated.
- This remains an early access release. The full macOS-version, multi-display, NAT/CGNAT, concurrency, and long-duration validation matrix is incomplete.

Open the DMG and drag MacRemote into Applications. On the Mac being shared, grant Screen Recording and Accessibility in System Settings > Privacy & Security.
