# 0.9.8

## Your books get their tables of contents back

Making a document searchable rebuilds it, and the rebuild cannot carry an
outline — so books imported on the Mac lost the contents their publisher put in
them. On this library that was 6,753 chapter entries across three books:
Davidson's alone had 5,389 and was showing 28 chapters guessed from the titles
printed at the top of each page.

The rebuild always wrote a separate copy and left the original alone, so none of
it was actually lost. InkVault now reads those contents back the first time it
opens each book, and saves the outline before rewriting anything from now on —
which is what the iPad has always done.

A book is only matched to its original if the page count still agrees, so a file
replaced since it was imported can never hand its contents to the wrong book.

## Documents that need nothing are left alone

A PDF that already carries proper text was still being rebuilt from scratch:
slower, larger, its images re-encoded a generation poorer, and its outline gone.
Those files are now untouched, byte for byte. A page that genuinely has no text
still gets one, which is what the rebuild was always for.

Pages that already carry their own text are no longer written over either. A
second invisible layer on top of a good one makes find land on the wrong words.
