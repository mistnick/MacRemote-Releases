# MacRemote

Install the current distribution from [GitHub Releases](https://github.com/mistnick/MacRemote-Releases/releases/latest).

## New installation

Apple Silicon and macOS 14 or later are required. Install the app from the DMG, or use the host-service PKG to install the app and its optional machine components. Follow the service guide attached to the release. Sign in to your company and explicitly authorize screen recording, input and receiver keys.

The public console is [https://mr.kelion.it/admin/](https://mr.kelion.it/admin/). Credentials are delivered privately. The first administrator must change the temporary password and configure TOTP.

The application, service, browser panel and backend share one API contract. The initial database schema requires an empty application database. API calls use access tokens. See [the release notes](RELEASE_NOTES.md).

## Artifact status

The app and DMG are Developer ID signed. The PKG named `unsigned` has no Installer signature. This distribution is not notarized. Check the attached manifest and SHA-256 files. LoginWindow capture/input and the hardware/network validation matrix still require physical validation. FileVault preboot is excluded.
