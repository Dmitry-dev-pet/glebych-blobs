# Encrypted application data

This repository contains opaque ciphertext objects and encrypted-key envelopes.
It contains no plaintext documents or private decryption keys.

`current.json` selects an immutable descriptor in `snapshots/`. Objects in
`blobs/` are named by the SHA-256 of their ciphertext. Updating this repository
does not redeploy the consuming application.

Format: AES-256-GCM data encryption with RSA-OAEP-SHA-256 key wrapping.
Document names and source provenance are inside the encrypted manifest.
