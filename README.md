# Racing Blind tracks

Track libraries for the Racing Blind iOS app. The app reads this repository when it opens,
so tracks published here reach players without an app update.

- `catalog.json` lists the libraries and their tracks.
- `tracks/` holds each track as a CSV saved from the Google Sheets track designer.

## Publishing a track

1. Save the track's CSV in `tracks/` (lowercase file name, no spaces).
2. Add it to a library in `catalog.json` with a permanent `id`, the `name` players see,
   the `file` path and `"version": 1`.
3. To change a published track, replace its CSV and raise its `version` by 1.
   Never change a track's `id`: best scores are kept under it.

`format` is the track format the app must understand (currently 1). Tracks with a newer format
than an installed app knows are skipped by that app instead of breaking it.
