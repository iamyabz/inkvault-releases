# 0.9.38

**Update from any earlier version before you open a `.inkvault` anyone sends
you.** A security review found that a deliberately malformed shared file could
delete a file on your Mac or iPad. Nothing you have received is affected unless
it was crafted to do this, but the door was open and is now shut.

## Opening a shared file is safe

Every reference inside a `.inkvault` is now checked to be what it claims before
anything touches your disk. A file that names a location instead of its contents
is refused whole, before a single byte is written.

## Sharing a document whose file isn't on your device

This is allowed on purpose — the text and your notes still travel — but the
shared record used to carry the file paths from the sender's device. On the
recipient's machine those could quietly attach to one of their own files with
the same name, showing the wrong document and, if they later deleted the import,
deleting their file with it. Shared documents no longer carry any path from the
sender.

## Receiving now works where it didn't

- Opening a `.inkvault` from Files on iPhone or iPad said "That isn't an InkVault
  file". It reads correctly now.
- Opening one on a Mac without iCloud sync refused outright. It imports.
- Opening one straight after launching the app duplicated documents you already
  had instead of adding the shared notes to your copy.
- Opening a large one froze the app while it was checked.

## Shared handwriting stays put

Ink that arrives in a shared file is the only copy on your device until it has
been backed up, and routine housekeeping could delete it. It is now protected
until it is safely stored, and it stops being re-uploaded on every sync.

## Merging into a document you already own

Adding someone's notes to a book you already have could fail outright and report
the document as damaged. It now succeeds, keeps your own index, and no longer
copies the sender's device details into your library.
