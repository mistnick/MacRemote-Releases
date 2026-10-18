MacRemote 0.1.5 fixes clicks and pointer movement on the remote desktop.

- Fixed an AppKit exception in the viewer: mouse clicks and movement were reading scroll-only event properties and failing before input could be sent to the remote Mac.
- Scroll fields are now read only from scroll events; pointer button fields are read only from mouse events.
- Added an AppKit regression test covering left and right clicks, releases, movement, dragging, scrolling, coordinate mapping in an offset view, and view-only permissions. The test creates events without posting input to the system.
- Apple Silicon; macOS 14 or later. Source commit: `cffd907`.
- Developer ID signed, accepted by Apple notarization, and verified with a stapled ticket.

Install this update on the Mac used to view and control the remote desktop. Open the DMG and drag MacRemote into Applications, replacing the previous version. The Mac being controlled must authorize MacRemote in System Settings > Privacy & Security > Accessibility.

This remains an early access release. A physical two-Mac end-to-end check and the full hardware/network validation matrix remain incomplete.
