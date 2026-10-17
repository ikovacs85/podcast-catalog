# Podcast Learner model catalog

The list of on-device AI models offered by the Podcast Learner app (speech recognition and
language models), read by the app from:

    https://raw.githubusercontent.com/ikovacs85/podcast-catalog/main/manifest.json

- `manifest.json`: the models, with download URLs, sizes and SHA-256 checksums.
- `manifest.json.sig`: Ed25519 signature of the exact bytes of `manifest.json`.

The app only uses a catalog whose signature matches the public key built into it, and only
installs files whose SHA-256 matches the catalog, so changing these files without the signing
key has no effect.

**Don't edit these files here.** They are generated in the app repository (`catalog/`), signed
there, and copied here with `tools/manifest/manifest_tool.py publish`.
