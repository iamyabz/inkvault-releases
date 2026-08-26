# 0.9.4

## The blank page you inserted is still there

It always was. Opening a book built a fresh reading window that knew nothing
about your inserted sheets, so the paper disappeared the moment you left and
came back. Inserting one worked, which is what made it look like it had not been
saved at all. It had: your handwriting on it was on disk, indexed, and published
the whole time.

The small reader had a second version of the same problem — it only ever showed
sheets that came from ANOTHER device, never the ones made here, which is exactly
why a page you made on the iPad turned up on the Mac and nowhere on the iPad.

## Re-indexing a book no longer throws your sheets away

A sheet has a page record so its handwriting is searchable, and the Mac's
scanner counted that record as a page of the book. The count never matched, so
every scan re-indexed the entire document, rebuilt the whole searchable PDF, and
dropped the sheet's record on the way through — then synced the loss to every
device.

## The Mac stopped showing annotations it already had

A downloaded sidecar is filed under the hash that was current when it arrived.
The moment any device published again, that name went stale and the reader could
no longer find a perfectly good copy sitting on disk — so it showed nothing at
all rather than something a minute old.

## Also

- Handwriting on an inserted sheet can now be jumped to from search. It was
  findable and then unreachable: the jump treated the sheet's key as a page
  number and clamped it to the last page of the book.
- Page totals, contents bounds and re-OCR no longer count inserted sheets as
  pages of the book.
- The last page or two of the reading window could not be reached while a sheet
  was in view.
