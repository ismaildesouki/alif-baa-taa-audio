# Alif Baa Taa audio

This repository hosts the narration audio packs for the Alif Baa Taa app, which
teaches reading Arabic. The narration is generated text to speech. Nothing else
lives here: no app code.

Each release is one set of packs, matching the app builds that bundle its
`packs.json`:

- `<pack>.<sha12>.abp`: the narration of one level (`l02` to `l12`) or of the
  word review set (`words`). The name carries the start of the file's sha256,
  so a changed pack always gets a new name.
- `packs.json`: the index of the set (sizes and sha256 of every pack).

The app downloads a pack when a learner needs it, from
`https://github.com/ismaildesouki/alif-baa-taa-audio/releases/download/<tag>/<file>`.
A release never changes once an app build points at it; new packs go into a new
release.
