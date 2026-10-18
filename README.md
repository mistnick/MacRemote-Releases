# MacRemote Releases

Download installers from the [Releases page](https://github.com/mistnick/MacRemote-Releases/releases).

## Install

MacRemote is for Apple Silicon Macs running macOS 14 or later.

1. Download the latest `MacRemote-*-arm64.dmg` asset.
2. Open the disk image and drag **MacRemote** to **Applications**.
3. Launch MacRemote and grant Screen Recording and Accessibility permissions when prompted on the Mac being shared.

Stable DMG releases through 0.1.5 are signed with Developer ID and notarized by Apple. The 0.2.0 prerelease app and DMG are Developer ID signed, but are not notarized; its optional host-service PKG has no installer signature. Each release includes a SHA-256 file; after downloading both assets into the same folder, run the matching command, for example:

```sh
shasum -a 256 -c MacRemote-0.1.2-arm64.dmg.sha256
```

These are early access builds for pilot testing. The source repository is private.

## 0.2.0 prerelease

[MacRemote 0.2.0 Early Access](https://github.com/mistnick/MacRemote-Releases/releases/tag/v0.2.0) introduces the optional machine service and LoginWindow/Aqua agent, plus the administration backend and web viewer. Read [the release notes](RELEASE_NOTES-0.2.0.md) before installing. Update the backend before activating machine enrollment. The public pilot backend is not deployed by publishing this release.

Use the optional `MacRemote-HostService-0.2.0-arm64-unsigned.pkg` asset to install or update the service; use the DMG for the ordinary client. Download the service guide from the release assets. Real LoginWindow capture and input, installation, reboot and rollback remain unverified on physical Macs. FileVault preboot is excluded. The stable updater skips this prerelease.
