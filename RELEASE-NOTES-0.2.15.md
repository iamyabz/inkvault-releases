## InkVault 0.2.15

### YouTube videos, on the Mac
**File ▸ Add YouTube Link…** (⇧⌘Y), or the **+** menu in your library. Paste a link and its transcript, and the video joins your library like a lecture you recorded yourself. Searchable by what was *said*, quotable in Ask AI with citations, and every citation jumps to the second it came from.

Nothing is downloaded. The video streams from YouTube inside the note, beside a transcript that highlights as it plays and seeks when you click a line.

**If you already have `yt-dlp` installed**, InkVault offers to fetch the captions for you and fills the transcript in. It only ever fetches subtitles. Never video or audio. And the button only appears when the tool is already on your Mac. Nothing to install; pasting works exactly as before.

### Search stops quietly losing its meaning
A page could hold text but no vector. Through a failed import, or by arriving from a device that had no API key. And such a page is invisible to the half of search that understands meaning rather than keywords. Worse, syncing could **erase** vectors your Mac already had, undoing repairs within hours.

Both are fixed. InkVault now also repairs any remaining gaps by itself, in the background, so this can't quietly degrade again.

### Smaller things
- Notes whose original lives on another device no longer report themselves as missing files every few minutes.
- The "waiting to upload" count no longer counts things this Mac could never upload.
