# 0.9.37

Sharing, audited. If you have 0.9.36, update — a shared file could not be
opened at all by someone who had not turned on iCloud sync, which is most people
receiving one for the first time.

## Dragging a document onto a folder works again

It had stopped entirely on the Mac: no drag image, no drop, no error. Clicking a
card and dragging one onto a folder in the sidebar files it again, and dragging
a multiple selection still moves the whole group.

## Six fixes to sharing

**You no longer need iCloud to open a shared file.** Importing writes to your
own library, so it never needed a sync account in the first place.

**Shared handwriting can no longer go missing.** Ink that arrived in a
`.inkvault` could be dropped by the housekeeping that clears out stale
annotation claims, taking it off every device including the one that imported
it. Imported ink is now recognised as something that is still on its way rather
than something stale.

**Two documents with the same name no longer overwrite each other.** A shared
folder with two files called "Lecture 1.pdf" installed one on top of the other,
leaving both entries pointing at the same file. Imported files are now stored by
content, so identical names cannot collide and identical files are stored once.

**A document is only merged into one you already have when the files are truly
byte-identical.** The older check could fall back to a coarse comparison and
merge two unrelated documents.

**One damaged document no longer refuses the whole bundle.** It is reported on
its own, and everything else imports.

**A share that fails partway leaves nothing behind**, rather than a half-written
file with the right name sitting ready to send.

## Smaller things

The Mac share panel no longer freezes while it measures a large folder, and it
shows progress while writing one instead of appearing to do nothing until Finder
opens. iPhone and iPad no longer leave previous shared files taking up space.
