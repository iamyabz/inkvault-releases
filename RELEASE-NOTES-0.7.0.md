# InkVault 0.7.0

**Long books no longer freeze.**

Touching text in a very long book could lock the app for half a minute and use two gigabytes. The cause is iOS: PDFKit runs its own text recognition over pages as part of text selection, even when every page already has searchable text — and on a sixteen-hundred-page book it does that on the thread drawing your screen. There is no setting to turn it off.

So in books of four hundred pages or more, InkVault stops using iOS's text selection and gives you its own instead. A Copy button in the reader copies the current page's text straight from the index InkVault already built when it read the book — instantly, with none of the pause. Shorter documents keep normal selection, because the problem only appears at length.

This is a trade rather than a repair, and it is worth being plain about that: you lose dragging a selection across part of a page in a long book, and you gain a reader that does not stop for thirty seconds.
