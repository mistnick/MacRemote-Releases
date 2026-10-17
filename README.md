# MacRemote Releases

Download installers from the [Releases page](https://github.com/mistnick/MacRemote-Releases/releases).

## Install

MacRemote is for Apple Silicon Macs running macOS 14 or later.

1. Download the latest `MacRemote-*-arm64.dmg` asset.
2. Open the disk image and drag **MacRemote** to **Applications**.
3. Launch MacRemote and grant Screen Recording and Accessibility permissions when prompted on the Mac being shared.

The installer is signed with Developer ID and notarized by Apple. Each release includes a SHA-256 file; after downloading both assets into the same folder, run the matching command, for example:

```sh
shasum -a 256 -c MacRemote-0.1.2-arm64.dmg.sha256
```

These are early access builds for pilot testing. The source repository is private.
