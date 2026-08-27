# InkVault 0.9.14

A bug-fix release. Twenty-odd defects found by going through sync, annotations,
the PDF pipeline, both readers and the importer, and verifying each one against
the code before changing anything.

## Your work is safer

- **A device that could not reach iCloud could mint a second library key.** The
  check for "does a library already exist up there?" could not tell a failed
  check from an empty cloud, and an empty cloud is what causes a new key to be
  created. Two keys means two libraries that never reconcile, while sync goes on
  reporting success. A device that cannot reach iCloud now waits.
- **A library that failed to load could delete published originals.** The
  document sweep learned to refuse this after a scare; the sweep that removes
  published *files* never got the same guard, though it decides the same way.
- **"Delete Video, Keep Audio & Transcript" destroyed the audio on iPhone and
  iPad.** The import extracted an audio track, transcribed it, and then filed
  the document against the video instead, so the one file it kept was the one
  it deleted. Videos already imported that way are handled safely.
- **The last stroke before you put the pen away could be lost.** Ink is written
  a fraction of a second after the pen lifts; turning markup off inside that
  window dropped the canvas before the write.
- **Restoring a backup could be undone by the next sync**, which was still
  holding the library from before the restore.
- **Edits to a document imported on another device were silently rejected** for
  the first few syncs, which is why annotations sometimes needed a close and
  reopen before they showed up.

## The small reader caught up with the big one

Opening a document beside your notes now behaves like opening it full screen:
inserted blank sheets appear (they never did in short documents, or on first
open), another device's handwriting is downloaded rather than only read from
what happened to be cached, and ink is drawn at the right size after zooming.

## Faster

Importing no longer freezes the app while it works: copying a large video,
turning a photo into a page, and re-encoding rotated photos have all moved off
the main thread.

## Also fixed

- Search results and Find in long books scrolled to the wrong page, or moved
  nowhere while the match counter advanced.
- Inserting a blank sheet after scrolling threw you back to where the book was
  opened.
- The rotate button in photo import was wrong for photos taken in portrait.
- A book whose PDF carries a token three-line outline no longer has that outline
  permanently suppress the chapters InkVault recovered itself.
- With three devices writing on one page, the third device's handwriting could
  disappear, and erasures aimed at it were dropped.
- A sheet somebody else had written on came back everywhere except the device it
  was deleted from.
- Annotation downloads no longer retry for ever when there is nothing to fetch,
  and say what happened when they fail.
