# InkVault 0.9.54

The largest release since 0.9.53: a new visual design across iPhone and iPad, one
playback session that survives leaving the screen, and a long run of reliability
work on sync, folders and memory.

## Reading and playback

- **Audio and video keep playing when you navigate away.** Leaving a recording is
  no longer a pause command. Playback continues through the library, the reader,
  backgrounding and lock, with Lock Screen and Control Center controls, headphone
  and AirPods buttons, and the same position waiting when you come back.
- **Picture in Picture** from full-screen video on iPhone and iPad, with the
  player restored to the right screen when you come back.
- **Ask AI inside full-screen video** — the real Ask experience, not a second
  simplified chat, as a sheet on iPhone and beside the picture on iPad. The
  conversation survives closing and reopening it.

## The library

- **Every row carries a portrait.** Pages, slides, handwriting, canvases,
  recordings and films each get their own, drawn from the document's own
  content — never an invented cover.
- **Synced PDFs show their real first page.** A document downloaded from another
  device opened correctly but drew a grey glyph in its row; the picture was
  looking in one fewer place than the reader.
- **Book covers keep their colours in Dark Mode.** A page of print is still
  inverted so it does not glare; a cover is not.
- **Counts tell the truth.** Recordings are measured in minutes rather than
  counted as pages, and the library reports the pages it actually holds rather
  than the number a file claims.
- **Where you were.** A document you have read into shows the page you reached,
  and a collection offers it back to you under Continue. This is remembered per
  device, and is not synced.

## Search

- A result's page number or timestamp is now coloured by how good the match is:
  green for a strong one, clay for a good one, red below the confidence line.
- Results read as evidence — the source, where in it, and the quote — with
  recordings offering to play from the moment they matched.

## Reliability

- Fixed a case where a large library left hundreds of megabytes of embedding
  vectors stranded in memory on iPhone.
- A torn write to the embedding sidecar is now survivable instead of permanently
  degrading search.
- Folder reordering, nesting and moves converge correctly across devices, and a
  move is one write rather than a whole-library rewrite.
- Annotations made on one device reach the others in both directions.

## Notes

This is a beta build. Keep your own backups of anything you cannot afford to
lose, and do not use InkVault for clinical, legal or other professional
decisions.
