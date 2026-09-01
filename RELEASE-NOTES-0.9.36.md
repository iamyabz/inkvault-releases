# 0.9.36

## Share a document or a folder as one file

Right-click a document — or a whole folder — and choose Share. InkVault writes a
single `.inkvault` file carrying the original files *and* everything it already
worked out about them: the text, the page index, the search vectors, and your
annotations. Whoever opens it gets a library that is searchable immediately,
instead of a folder that has to be indexed all over again on their machine.

It works between Mac, iPad and iPhone in any direction. Double-click the file,
or open it from Files, and InkVault shows you exactly what is inside before it
writes anything.

**Before you send**, the share panel tells you the honest size — deduplicated,
so a recording that is both the document and its audio is counted once — and
whether any document's original bytes are missing from this device, because
those travel as text only and the person receiving them deserves to know.

**Your handwriting travels by default**, with a visible toggle if it should not.
It arrives on the other side as a separate, removable layer that never merges
into the other person's own notes, and it reaches every device they own, not
just the one they opened the file on.

**A file they already have is enriched, not duplicated.** If someone shares
their annotated copy of a textbook you already own, you keep your copy where it
is, with your notes intact, and only their annotations are added. No second
copy of a 400 MB book.

**Vectors are only adopted when they mean something.** If the sender indexed
with a different AI model, their search vectors are meaningless in your library
rather than merely worse — so the text and annotations arrive and the document
re-indexes locally, and the import tells you that is what is happening.

Bundles verify themselves on the way in: every file is checked against its own
content hash, and a document whose text does not match its bytes is refused
rather than imported and then cited by Ask AI.
