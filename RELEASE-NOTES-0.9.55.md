# InkVault 0.9.55

Memory. InkVault used to carry the whole of your session for as long as it was
open. It doesn't any more.

## What this fixes

- **Closing a document actually closes it.** Every PDF you opened stayed fully
  loaded in memory for the rest of the session, even after its window was gone.
  On a large textbook that was around 45 MB per document, never given back —
  which is why a morning's reading could leave the app sitting on hundreds of
  megabytes. Measured on a 4,273-page book: six open-and-close cycles used to
  climb to +348 MB and stay there; now it returns to where it started each time.
- **The search box no longer costs anything until you search.** The text it
  matches against was built for your entire library at launch and kept for the
  whole session, whether or not you ever typed in it. It is now built on the
  first keystroke and released when you stop searching. Searching finds exactly
  what it found before — the same matching, unchanged.
- **Notes and ⌘F text are released with the document they belong to**, instead
  of accumulating for every document opened.
- **Fixed: ⌘F could find nothing in a large book.** The reader took its copy of
  the page text a moment before that text was ready, and never looked again.

## Smaller things

- InkVault answers the system when the Mac is short of memory, handing back what
  it can rebuild.
- The built-in health log stops rewriting itself every thirty seconds when
  nothing has happened, and records what the app's memory is actually made of —
  so a future problem can be explained rather than guessed at.
- Video playback was measured for the same problem and did not have it; nothing
  was changed there.
- The Acknowledgements screen no longer lists eight libraries the Mac app does
  not include.

## Notes

This is a beta build. Keep your own backups of anything you cannot afford to
lose, and do not use InkVault for clinical, legal or other professional
decisions.
