# Radio — station list + web player

Two things live here:

- **`stations.json`** — the station list the Android app fetches on launch.
  Edit it here and every installed app picks up the change next time it opens.
  **Bump `version` whenever you edit it**, or clients keep their cached copy.
- **`index.html`** — a browser version of the player, for iPhone and anything
  else that can't run the Android app.

## Fixing a dead station

1. Edit `stations.json`, change that station's `url`.
2. Increment `version` at the top of the file.
3. Commit. Done — no app rebuild needed.

## Note on HTTP-only stations

Five South African stations only stream over plain HTTP. The Android app plays
them fine, but browsers block insecure audio on a secure page, so the web player
greys them out. That is expected, not a bug.
