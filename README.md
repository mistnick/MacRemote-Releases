# MacRemote Releases

Download MacRemote installers from the [Releases page](https://github.com/mistnick/MacRemote-Releases/releases).

## Install

MacRemote 0.1.0 is for Apple Silicon Macs running macOS 14 or later.

1. Download `MacRemote-0.1.0-arm64.dmg` from the latest release.
2. Open the disk image and drag **MacRemote** to **Applications**.
3. Launch MacRemote and grant Screen Recording and Accessibility permissions when prompted.

The installer is signed with Developer ID and notarized by Apple. Verify the downloaded image with the SHA-256 file attached to the release:

```sh
shasum -a 256 -c MacRemote-0.1.0-arm64.dmg.sha256
```

This is an early access build for pilot testing. The source repository is private.
