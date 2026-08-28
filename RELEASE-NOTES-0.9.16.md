# InkVault 0.9.16

Foundation release. Nothing here is a new feature — this is the end of a
hardening phase that went looking for the ways InkVault could lose or
misreport your work, and closed them.

## Your work is written down in order, or you are told

Everything a reader authors beside a document — page ink, the writing inside
sticky notes, tape and cards, inserted blank sheets, and erasures — used to be
written on a concurrent queue with the failure discarded. Two saves of one page
were two threads racing for one filename, so an older drawing could land after a
newer one, and rubbing something out while a save was in flight could bring the
ink back. A full disk lost handwriting silently.

All of it now goes through one ordered lane: newest state wins, a write that
cannot land is reported and retried rather than assumed, and reading a file back
waits for the writes to it. The same discipline fixed a case where a page added
in full screen could vanish from the page grid.

## Restoring a backup can no longer leave you without a library

The old restore deleted your library and then moved the replacement in. Anything
that stopped it in between — a crash, a full disk, an unplugged drive — left
nothing. It validated only that the backup contained a folder called `Library`,
so a truncated download would pass that check after the deletion had happened.

A restore is now a transaction: the replacement is validated first, your library
is moved aside rather than deleted, and the swap is a single rename. If InkVault
dies at any point, the next launch works out which complete library to keep and
puts it back.

## A document is only "indexed" when it has actually been read

Stopping a scan was recorded as finishing it. Two documents in a real library
were marked indexed after 4 of 200 pages and 20 of 1,139. That status is also
what moves your original file to the Trash and tells your other devices the file
has been read, so both were happening for documents that had barely started.

Completeness is now the test. A stopped scan says so, keeps the pages it read,
and resumes from there. A scan interrupted by the app quitting no longer claims
to still be running.

## Under the hood

The library index had a data race that could abort the app outright, and could
apply an edit meant for one document to another. A document arriving while the
app was still loading at launch could overwrite the whole index with itself.
Both are fixed, both are covered by tests that fail against the old code.

Nine automated gates now guard this behaviour, each carrying a control that
proves it would have caught the bug it was written for.
