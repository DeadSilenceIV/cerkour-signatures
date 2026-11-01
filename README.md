# cerkour-signatures

Signed descriptor packs for the Cerkour tools, published by CI. Clients fetch
`pack/manifest.txt`, check its ECDSA P-256 signature against keys compiled into
the DLL, then fetch `pack/<seq>/<name>.json` and check each size and SHA-256.

`revoked.txt` is a copy of the publisher's revocation list, for transparency;
clients only act on the `revoke` lines inside the signed manifest.
