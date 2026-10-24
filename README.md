# BTNHome update distribution

This repository distributes approved BTNHome update packages. Application and
firmware source code is maintained in separate private repositories.

Release assets may include a panel APK, publisher-signed update manifests and
firmware encrypted for one enrolled controller. Controller firmware is never
published here in plaintext. Pairing keys, signing private keys, cloud secrets,
device configuration and backups must never be uploaded.

The APK installer verifies the publisher signature, enrolled controller target,
expiry, file digest, version and the existing Android application signer.
Controllers independently verify firmware update signatures before activation.

Initial releases are controlled test releases. Automatic deployment is disabled
until installation and recovery acceptance tests have been completed. Use the
release notes for compatibility and testing status.

`update-publisher.json` contains only the public verification key. It cannot sign
an update. Expired manifests are rejected and must be republished by the owner.

Do not post pairing codes, keys or personal device information in issues.
