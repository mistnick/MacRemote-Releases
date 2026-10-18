# MacRemote Releases

Download installers from the [Releases page](https://github.com/mistnick/MacRemote-Releases/releases).

## Install or update

MacRemote requires Apple Silicon and macOS 14 or later.

1. In MacRemote 0.1.5, check for updates and download 0.2.0, or download `MacRemote-0.2.0-arm64.dmg` from [the release](https://github.com/mistnick/MacRemote-Releases/releases/tag/v0.2.0).
2. Open the disk image and drag MacRemote into Applications, replacing the previous copy, then reopen it.
3. Grant Screen Recording and Accessibility permissions on the Mac being shared.

For the optional machine service, use `MacRemote-HostService-0.2.0-arm64-unsigned.pkg` and the service guide attached to the release. Use the service package when updating a Mac with the service already installed.

Version 0.2.0 is offered on the channel used by the existing stable updater. It remains an Early Access build: the app and DMG are Developer ID signed, the PKG has no installer signature, and the 0.2.0 artifacts are not notarized. Stable DMGs through 0.1.5 were notarized. Real LoginWindow capture and input, reboot and rollback still require physical validation. FileVault preboot is excluded.

Each binary asset has a SHA-256 checksum file. For example:

```sh
shasum -a 256 -c MacRemote-0.2.0-arm64.dmg.sha256
```

## Public administration

The administration console is [https://mr.kelion.it/admin/](https://mr.kelion.it/admin/). The backend has been updated with web sign-in configuration. See [the 0.2.0 release notes](RELEASE_NOTES-0.2.0.md) for features, installation and validation limits. Credentials are provided privately; the source repository is private.
